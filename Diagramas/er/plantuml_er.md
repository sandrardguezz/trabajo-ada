@startuml

entity "Usuario" as usuario {
  * id_usuario : INT <<PK>>
  --
  * nombre : VARCHAR(100)
  * email : VARCHAR(255) <<UQ>>
  * contrasena_hash : VARCHAR(255)
  * rol : ENUM('superadmin','administrador','operativo')
  * activo : BOOLEAN
}

entity "CLIENTE" as cliente {
  * id_cliente : INT <<PK>>
  --
  * id_usuario_responsable : INT <<FK>>
  * nombre_comercial : VARCHAR(150)
  * id_fiscal : VARCHAR(30)
  * domicilio_fiscal : VARCHAR(255)
  * pais : CHAR(2)
  * moneda : CHAR(3)
    sector : VARCHAR(100)
  * estado : ENUM('activo','inactivo')
  * fecha_alta : DATE
    fecha_baja : DATE
}

entity "CONTACTO" as contacto {
  * id_contacto : INT <<PK>>
  --
  * id_cliente : INT <<FK>>
  * nombre : VARCHAR(100)
    email : VARCHAR(255)
    telefono : VARCHAR(20)
  * funcion : ENUM('comercial','facturacion','cobros')
  * activo : BOOLEAN
}

entity "SUSCRIPCION" as suscripcion {
  * id_suscripcion : INT <<PK>>
  --
  * id_cliente : INT <<FK>>
  * plan : VARCHAR(100)
  * precio_mensual_centimos : INT
  * descuento_porcentaje : DECIMAL(5,2)
  * plazo_pago_dias : INT
  * fecha_inicio : DATE
    fecha_fin : DATE
  * estado : ENUM('pendiente','activa','pausada','cancelada')
    fecha_inicio_pausa : DATE
    fecha_fin_pausa : DATE
    motivo_pausa : VARCHAR(255)
  * proximo_periodo : DATE
  * exento_prorrateo : BOOLEAN
}

entity "FACTURA" as factura {
  * id_factura : INT <<PK>>
  --
  * id_cliente : INT <<FK>>
    id_suscripcion : INT <<FK>>
    id_factura_rectificada : INT <<FK>>
  * tipo : ENUM('recurrente','puntual')
    serie : VARCHAR(10)
    numero : INT
    fecha_emision : DATE
  * fecha_vencimiento : DATE
    periodo_inicio : DATE
    periodo_fin : DATE
  * estado : VARCHAR(20)
  * base_total_centimos : INT
  * impuestos_total_centimos : INT
  * total_centimos : INT
  * moneda : CHAR(3)
  * id_fiscal_emision : VARCHAR(30)
  * domicilio_fiscal_emision : VARCHAR(255)
    recordatorios_pausados_hasta : DATE
  * num_lineas : INT
  * concepto_linea : VARCHAR(255)
  * cantidad_lineas : INT
  * precio_unitario_centimos_lineas : INT
  * descuento_porcentaje_lineas : INT
  * impuesto_porcentaje_lineas : INT
}
entity "PAGO" as pago {
  * id_pago : INT <<PK>>
  --
    id_factura : INT <<FK>>
  * fecha_pago : DATE
  * importe_centimos : INT
  * moneda : CHAR(3)
  * fuente : ENUM('banco','pasarela')
    referencia_externa : VARCHAR(100)
  * estado_conciliacion : ENUM('pendiente','conciliado','incidencia')
    fecha_conciliacion : DATE
}

entity "COMUNICACION" as comunicacion {
  * id_comunicacion : INT <<PK>>
  --
  * id_factura : INT <<FK>>
  * tipo : ENUM('envio_factura','recordatorio')
  * canal : ENUM('email','whatsapp')
  * destinatario_guardado : VARCHAR(255)
    fecha_envio : DATETIME
  * estado : ENUM('pendiente','enviado','fallido')
    descripcion_error : TEXT
}

entity "INCIDENCIA" as incidencia {
  * id_incidencia : INT <<PK>>
  --
  * id_cliente : INT <<FK>>
    id_factura : INT <<FK>>
  * id_usuario_responsable : INT <<FK>>
  * descripcion : TEXT
  * prioridad : VARCHAR(10)
  * estado : VARCHAR(20)
  * fecha_creacion : DATE
    fecha_revision : DATE
}

entity "AUDITORIA" as auditoria {
  * id_auditoria : INT <<PK>>
  --
    id_usuario : INT <<FK>>
  * fecha : DATETIME
  * accion : VARCHAR(50)
  * entidad_afectada : VARCHAR(50)
  * id_registro : INT
  * detalle_cambios : TEXT
}

entity "CONFIGURACION" as configuracion {
  * clave : VARCHAR(100) <<PK>>
  --
  * valor : VARCHAR(255)
}

usuario     ||--o{ cliente      : "responsable de"
usuario     ||--o{ incidencia   : "tiene una"
usuario     |o--o{ auditoria    : "realiza"

cliente     ||--o{ contacto     : "tiene"
cliente     ||--o{ suscripcion  : "contrata"
cliente     ||--o{ factura      : "recibe"
cliente     ||--o{ incidencia   : "tiene"

suscripcion |o--o{ factura      : "genera"

factura     |o--o{ factura
factura     |o--o{ pago         : "se cobra"
factura     ||--o{ comunicacion : "se notifica"
factura     |o--o{ incidencia   : "tiene"

@enduml
