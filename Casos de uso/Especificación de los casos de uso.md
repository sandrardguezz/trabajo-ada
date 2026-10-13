# ESPECIFICACIÓN DE LOS CASOS DE USO

En esta sección, se van explicar los diferentes casos de uso que hemos encontrado. Para ello se han definido las siguientes características que debemos tener en cuenta para cada caso de uso:

> -  Nombre del caso de uso
> -  Identificador
> -  Objetivo
> -  Actor o actores participantes
> -  Requisitos funcionales asociados
> -  Precondiciones
> -  Flujo Principal 
> -  Flujos Alternativos
> -  Flujos de excepción, cuando corresponda
> -  Postcondiciones

Una vez hemos visto las características, ya podemos comenzar con los diferentes casos de uso.

## CU01: Iniciar Sesión y Recuperar Acceso

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Permitir a los usuarios/administradores del sistema autenticarse mediante su correo corporativo de Turbine y contraseña, donde en caso de olvido de esta, se puede recuperar el acceso con el correo.|
|**Actores**| Superadministrador, Administrador y Usuario Operativo.|
|**Requisitos**| FR1.1|
|**Precondiciones**| El usuario/administrador debe estar previamente registrado y disponer de una cuenta activa asociada a un correo corporativo de Turbine. |
|**Postcondiciones**| El usuario obtiene el acceso a la aplicación con los permisos que tenga o en caso de recuperación, recibe un enlace/correo para restablecer su contraseña. |

#### Flujo Principal

#### Flujos Alternativos

#### Flujos de excepción

## CU02: Gestionar Usuarios, Roles y Permisos

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Permitir a los administradores crear, modificar y desactivar cuentas internas, como también asignar la gestión clientes a usuarios operativos.|
|**Actores**| Superadministrador y Administrador.|
|**Requisitos**| FR1.2, FR1.3|
|**Precondiciones**| El usuario debe haber iniciado sesión con permisos de administración, para realizar las diferentes tareas que definimos en este caso de uso. |
|**Postcondiciones**| Se actualiza la información de la cuenta interna del usuario, sus roles/permisos y permite la delegación/asignación de clientes en el sistema. |

#### Flujo Principal

#### Flujos Alternativos

#### Flujos de excepción

## CU03: Gestionar Clientes y Contactos

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Administrar los datos comerciales y fiscales de los clientes, que los administradores deben crear, teniendo cada cliente/empresa unas personas de contacto con distintas funciones y el sistema deberá advertir de clientes duplicados y antiguos que quieran volver a suscribirse.|
|**Actores**| Administrador y Usuario Operativo.|
|**Requisitos**| FR2.1, FR2.2, FR2.3|
|**Precondiciones**| El usuario debe poder acceder a la gestión de clientes. |
|**Postcondiciones**| Se actualiza la información del cliente y sus contactos, manteniendo su integridad y historia en el sistema. |

#### Flujo Principal

#### Flujos Alternativos

#### Flujos de excepción

## CU04: Importar clientes mediante CSV

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Cargar la información de clientes desde un archivo CSV con previsualización, mapeo de columnas y detección de errores o duplicados antes de confirmar la operación.|
|**Actores**| Administrador y Usuario Operativo.|
|**Requisitos**| FR9.3, FR9.4|
|**Precondiciones**| El usuario dispone de un archivo CSV con todos los clientes a importar en la aplicación. |
|**Postcondiciones**| Los clientes quedan registrados en el sistema tras resolver o confirmar la previsualización. |

#### Flujo Principal

#### Flujos Alternativos

#### Flujos de excepción

## CU05: Gestionar Acuerdos Comerciales y Tarifas

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Registrar y modificar la fecha de inicio, plan/servicio, tarifa, responsable, condiciones de pago y documentación con cada cliente, pudiendo darse descuentos o excepciones económicas mediante una aprobación.|
|**Actores**| Superadministrador, Administrador y Usuario Operativo.|
|**Requisitos**| FR3.1, FR3.2, FR3.3|
|**Precondiciones**| El cliente debe estar dado de alta en la aplicación. |
|**Postcondiciones**| El cliente obtiene un acuerdo comercial activo con unas tarifas asignadas y otras características. |

#### Flujo Principal

#### Flujos Alternativos

#### Flujos de excepción

## CU06: Gestionar Suscripciones y Pausas

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Calcular la parte proporcional del primer mes de suscripción (igual es total), pudiendo configurar fechas de facturación o excluir prorrateos. Además, se puede pausar la suscripción ofreciendo un motivo y fechas.|
|**Actores**| Administrador y Usuario Operativo.|
|**Requisitos**| FR4.2, FR4.3|
|**Precondiciones**| El cliente debe tener un acuerdo comercial validado. |
|**Postcondiciones**| La suscripción se queda activa con sus fechas o temporalmente pausada. |

#### Flujo Principal

#### Flujos Alternativos

#### Flujos de excepción

## CU07: Crear y Modificar Facturas

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Generar facturas mensuales recurrentes o puntuales (ya sea con plantillas o no), validando datos obligatorios o detectando anomalías. En caso de emisión, necesitan un procedimiento de rectificación y se genera un PDF y si no se da la emisión, pueden corregirse.|
|**Actores**| Administrador y Usuario Operativo.|
|**Requisitos**| FR4.1, FR5.1, FR5.2, FR5.3, FR5.5, FR6.2 |
|**Precondiciones**| Existen suscripciones activas o conceptos para facturación puntual, además de plantillas configuradas. |
|**Postcondiciones**| Se crea un PDF de la factura con todos los datos y queda guardado en la plataforma. |

#### Flujo Principal

#### Flujos Alternativos

#### Flujos de excepción

## CU08: Procesar y Conciliar Pagos 

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Recibir información de pagos de fuentes externas, asociar automáticamente movimientos con facturas y detectar pagos duplicados y diferencias antes de marcar la factura como pagada.|
|**Actores**| Usuario Operativo.|
|**Requisitos**| FR7.1, FR7.2, FR7.3 |
|**Precondiciones**| Existen facturas guardadas pendientes de cobro y datos de pago de fuentes externas. |
|**Postcondiciones**| La factura se marca como pagada o queda registrada por duplicación o diferencias. |

#### Flujo Principal

#### Flujos Alternativos

#### Flujos de excepción

## CU09: Enviar Recordatorios y Notificaciones y Gestionar Comunicaciones

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Enviar recordatorios automáticos de pago, quedando detenidos al pago de la factura y notificando al administrador. Además, se tendrá una pantalla con todos los avisos/tareas que queden por realizar al abrir la aplicación, pudiendo utilizar una vía de comunicación para una mayor importancia.|
|**Actores**| Usuario Operativo.|
|**Requisitos**| FR6.1, FR6.3, FR6.4, FR7.4, FR8.1, FR8.2 |
|**Precondiciones**| La factura esta registrada o pendiente de cobro. |
|**Postcondiciones**| Se envían y registran las comunicaciones o se detienen los recordatorios al realizar el pago. |

#### Flujo Principal

#### Flujos Alternativos

#### Flujos de excepción

## CU10: Procesar la baja del Cliente

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Detener la generación de facturas, cuando un cliente se da de baja. Una vez esto ocurra, se deben resolver todos los pagos de facturas y se conservará el historial del cliente.|
|**Actores**| Administrador, Usuario Operativo.|
|**Requisitos**| FR4.4, FR5.4 |
|**Precondiciones**| El cliente quiere cancelar o finalizar el contrato. |
|**Postcondiciones**| La suscripción pasa a estado de baja, deteniendo la facturación, resolviendo todos los conflictos y conservando el historial. |

#### Flujo Principal

#### Flujos Alternativos

#### Flujos de excepción

## CU11: Búsqueda y Filtrado

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Buscar y filtrar clientes, contactos y facturas mediante diferentes criterios, como el nombre, identificador fiscal, contacto, estado.|
|**Actores**| Administrador, Usuario Operativo.|
|**Requisitos**| FR9.1 |
|**Precondiciones**| El usuario ha iniciado sesión en la plataforma. |
|**Postcondiciones**| El sistema muestra una lista de filtrados siguiendo los criterios. |

#### Flujo Principal

#### Flujos Alternativos

#### Flujos de excepción

## CU12: Consultar Tablero e Informes Financieros 

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Mostrar el tablero financiero con indicadores clave y permitir la generación e exportación de informes de facturación en CSV o PDF.|
|**Actores**| Superadministrador, Administrador.|
|**Requisitos**| FR9.2, FR9.3 |
|**Precondiciones**| Existen registros de facturación guardados en el sistema. |
|**Postcondiciones**| Se visualiza el cuadro de mando actualizado o se genera la descarga del archivo del informe. |

#### Flujo Principal

#### Flujos Alternativos

#### Flujos de excepción

## CU13: Configuración Global y Auditoría del Sistema 

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Configurar parámetros globales del sistemas, gestionar la API de integración y consultar los registros de auditoría y procesos automáticos.|
|**Actores**| Superadministrador.|
|**Requisitos**| FR10.1, FR10.2, FR10.3, FR10.4 |
|**Precondiciones**| El usuario inicia sesión como Superadministrador. |
|**Postcondiciones**| Se guardan las nuevas reglas de configuración global y quedan registradas las trazas de auditoría de las acciones realizadas. |

#### Flujo Principal

#### Flujos Alternativos

#### Flujos de excepción



