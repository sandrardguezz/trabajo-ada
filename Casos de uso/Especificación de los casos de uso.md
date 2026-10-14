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
1. El usuario accede a la pantalla de inicio de sesión.
2. Introduce su correo corporativo de Turbine y contraseña.
3. El sistema valida las credenciales y el estado activo de la cuenta.
4. El sistema concede el acceso y redirige al usuario a su panel correspondiente según su rol.

#### Flujos Alternativos
* **Recuperación de contraseña:** El usuario hace clic en "He olvidado mi contraseña", introduce su correo y el sistema le envía un enlace de recuperación. El usuario accede al enlace, define una nueva contraseña y entra al sistema.

#### Flujos de excepción
* **Credenciales incorrectas:** El usuario introduce mal la contraseña. El sistema muestra un mensaje de error en lenguaje natural ("Usuario o contraseña incorrectos").
* **Bloqueo por seguridad:** El usuario falla la contraseña 5 veces consecutivas. El sistema bloquea temporalmente la cuenta y notifica al administrador.
* **Enlace caducado:** El usuario intenta usar un enlace de recuperación de contraseña tras más de 15 minutos. El sistema deniega el acceso y obliga a solicitar uno nuevo.

## CU02: Gestionar Usuarios, Roles y Permisos

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Permitir a los administradores crear, modificar y desactivar cuentas internas, como también asignar la gestión clientes a usuarios operativos.|
|**Actores**| Superadministrador y Administrador.|
|**Requisitos**| FR1.2, FR1.3|
|**Precondiciones**| El usuario debe haber iniciado sesión con permisos de administración, para realizar las diferentes tareas que definimos en este caso de uso. |
|**Postcondiciones**| Se actualiza la información de la cuenta interna del usuario, sus roles/permisos y permite la delegación/asignación de clientes en el sistema. |

#### Flujo Principal
1. Un administrador accede a la sección de gestión de usuarios y selecciona "Crear/Invitar usuario".
2. Introduce los datos del empleado, selecciona su rol y los clientes a su cargo.
3. El sistema guarda la configuración y envía una invitación al nuevo usuario.

#### Flujos Alternativos
* **Delegación temporal:** Un administrador edita un usuario que se va de vacaciones, selecciona las fechas de ausencia y asigna temporalmente sus clientes a otro compañero.
* **Desactivación:** Se da de baja a un usuario. Su perfil queda inactivo pero su histórico de acciones (auditoría) se mantiene.

#### Flujos de excepción
* **Violación de permisos:** Un administrador (no superadministrador) intenta asignarse a sí mismo un rol superior. El sistema bloquea la acción.
* **Dominio incorrecto:** Se intenta invitar a un usuario con un correo que no pertenece al dominio corporativo de Turbine. El sistema muestra un error y detiene el proceso.

## CU03: Gestionar Clientes y Contactos

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Administrar los datos comerciales y fiscales de los clientes, que los administradores deben crear, teniendo cada cliente/empresa unas personas de contacto con distintas funciones y el sistema deberá advertir de clientes duplicados y antiguos que quieran volver a suscribirse.|
|**Actores**| Administrador y Usuario Operativo.|
|**Requisitos**| FR2.1, FR2.2, FR2.3|
|**Precondiciones**| El usuario debe poder acceder a la gestión de clientes. |
|**Postcondiciones**| Se actualiza la información del cliente y sus contactos, manteniendo su integridad y historia en el sistema. |

#### Flujo Principal
1. El usuario accede a "Añadir cliente" e introduce los datos fiscales, comerciales y el contacto principal (optimizando clics y tiempo).
2. El sistema valida los datos obligatorios y formatos.
3. El cliente se guarda y queda disponible para asignarle acuerdos comerciales.

#### Flujos Alternativos
* **Múltiples contactos:** El usuario añade contactos adicionales al mismo cliente, especificando su rol (facturación, comercial, etc.).
* **Reactivación:** El usuario busca dar de alta un cliente inactivo. El sistema lo reconoce y permite recuperar toda su ficha histórica en lugar de crear uno nuevo.

#### Flujos de excepción
* **Cliente duplicado:** El sistema detecta que el CIF/NIF o nombre introducido ya existe en la base de datos activa. Muestra un aviso y obliga a revisar antes de permitir guardarlo.
* **Datos obligatorios faltantes:** El usuario intenta guardar sin introducir datos clave (ej. domicilio fiscal). El sistema resalta el campo en rojo con un mensaje claro y detiene el guardado.

## CU04: Importar clientes mediante CSV

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Cargar la información de clientes desde un archivo CSV con previsualización, mapeo de columnas y detección de errores o duplicados antes de confirmar la operación.|
|**Actores**| Administrador y Usuario Operativo.|
|**Requisitos**| FR9.3, FR9.4|
|**Precondiciones**| El usuario dispone de un archivo CSV con todos los clientes a importar en la aplicación. |
|**Postcondiciones**| Los clientes quedan registrados en el sistema tras resolver o confirmar la previsualización. |

#### Flujo Principal
1. El usuario sube un archivo CSV con la base de datos de clientes.
2. El sistema lee el archivo y genera una previsualización en pantalla.
3. El usuario relaciona las columnas del archivo (Nombre, CIF, Dirección) con los campos del sistema.
4. El usuario confirma y el sistema procesa la importación en segundo plano, notificando al finalizar.

#### Flujos Alternativos
* **Exclusión manual de filas:** Durante la previsualización, el usuario desmarca ciertas filas del CSV que decide no importar.

#### Flujos de excepción
* **Errores de formato de archivo:** El archivo subido no es CSV o está corrupto. El sistema aborta la operación y solicita un formato válido.
* **Errores en filas de datos:** La previsualización detecta CIFs inválidos o clientes ya existentes. El sistema marca las filas en rojo y bloquea su importación hasta que el usuario decida sobrescribir, corregir o ignorar.

## CU05: Gestionar Acuerdos Comerciales y Tarifas

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Registrar y modificar la fecha de inicio, plan/servicio, tarifa, responsable, condiciones de pago y documentación con cada cliente, pudiendo darse descuentos o excepciones económicas mediante una aprobación.|
|**Actores**| Superadministrador, Administrador y Usuario Operativo.|
|**Requisitos**| FR3.1, FR3.2, FR3.3|
|**Precondiciones**| El cliente debe estar dado de alta en la aplicación. |
|**Postcondiciones**| El cliente obtiene un acuerdo comercial activo con unas tarifas asignadas y otras características. |

#### Flujo Principal
1. El usuario selecciona un cliente y crea un nuevo acuerdo comercial.
2. Define la fecha de inicio, el servicio contratado, el responsable interno y selecciona la tarifa estándar.
3. El sistema valida, guarda y activa el acuerdo.

#### Flujos Alternativos
* **Revisión anual:** El sistema detecta un cambio en el rango de facturación del cliente y propone una nueva tarifa. El administrador la valida y se actualiza el acuerdo comercial.

#### Flujos de excepción
* **Descuento superior al umbral:** Un usuario operativo aplica un descuento excepcional. El acuerdo no se activa inmediatamente; pasa a estado "Pendiente de aprobación" y el sistema notifica al administrador/superadministrador.

## CU06: Gestionar Suscripciones y Pausas

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Calcular la parte proporcional del primer mes de suscripción (igual es total), pudiendo configurar fechas de facturación o excluir prorrateos. Además, se puede pausar la suscripción ofreciendo un motivo y fechas.|
|**Actores**| Administrador y Usuario Operativo.|
|**Requisitos**| FR4.2, FR4.3|
|**Precondiciones**| El cliente debe tener un acuerdo comercial validado. |
|**Postcondiciones**| La suscripción se queda activa con sus fechas o temporalmente pausada. |

#### Flujo Principal
1. El usuario activa una suscripción para un cliente a mitad de mes.
2. El sistema calcula automáticamente el prorrateo de los días restantes y muestra el desglose financiero.
3. El usuario confirma y la suscripción queda operativa para la generación automática de facturas.

#### Flujos Alternativos
* **Exclusión de prorrateo:** El usuario marca una casilla por una condición comercial para cobrar el mes completo, indicando al sistema que ignore el cálculo proporcional.
* **Pausar suscripción:** El usuario indica un motivo y un rango de fechas para pausar el servicio. El sistema detiene la generación de facturas durante ese periodo y reanuda automáticamente al concluir.

#### Flujos de excepción
* **Fechas incongruentes de pausa:** El usuario intenta pausar una suscripción con una fecha de fin anterior a la de inicio. El sistema rechaza la operación e informa del error temporal.

## CU07: Crear y Modificar Facturas

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Generar facturas mensuales recurrentes o puntuales (ya sea con plantillas o no), validando datos obligatorios o detectando anomalías. En caso de emisión, necesitan un procedimiento de rectificación y se genera un PDF y si no se da la emisión, pueden corregirse.|
|**Actores**| Administrador y Usuario Operativo.|
|**Requisitos**| FR4.1, FR5.1, FR5.2, FR5.3, FR5.5, FR6.2 |
|**Precondiciones**| Existen suscripciones activas o conceptos para facturación puntual, además de plantillas configuradas. |
|**Postcondiciones**| Se crea un PDF de la factura con todos los datos y queda guardado en la plataforma. |

#### Flujo Principal
1. Llega la fecha de facturación recurrente (o el usuario inicia una creación puntual).
2. El sistema consolida las líneas de servicio, conceptos, descuentos e impuestos.
3. Se asigna una serie y numeración única.
4. El sistema emite la factura, genera el PDF inalterable y la pasa a estado "Emitida".

#### Flujos Alternativos
* **Modificación previa a la emisión:** Se genera una factura en estado "Borrador". El usuario la previsualiza, ajusta un concepto y posteriormente confirma su emisión.

#### Flujos de excepción
* **Importe anómalo detectado:** El sistema detecta que la factura recurrente tiene un importe inusualmente alto respecto al mes anterior. Advierte al usuario requiriendo validación expresa antes de emitir.
* **Intento de modificación de factura emitida:** Un usuario intenta editar una factura que ya está en estado "Emitida". El sistema bloquea la acción, indicando que las modificaciones estructurales requieren una Factura Rectificativa.

## CU08: Procesar y Conciliar Pagos 

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Recibir información de pagos de fuentes externas, asociar automáticamente movimientos con facturas y detectar pagos duplicados y diferencias antes de marcar la factura como pagada.|
|**Actores**| Usuario Operativo.|
|**Requisitos**| FR7.1, FR7.2, FR7.3 |
|**Precondiciones**| Existen facturas guardadas pendientes de cobro y datos de pago de fuentes externas. |
|**Postcondiciones**| La factura se marca como pagada o queda registrada por duplicación o diferencias. |

#### Flujo Principal
1. El sistema recibe y procesa los movimientos bancarios o de pasarelas de pago externas.
2. El sistema cruza automáticamente los identificadores o importes exactos con las facturas pendientes.
3. Al existir coincidencia unívoca, el sistema marca la factura como "Pagada" y detiene los recordatorios de impago.

#### Flujos Alternativos
* **Revisión manual requerida:** El sistema encuentra un pago que podría corresponder a múltiples facturas de idéntico importe. Deja el movimiento en estado "Pendiente de conciliación" para asignación manual.

#### Flujos de excepción
* **Discrepancia de importe:** El pago recibido es inferior al total facturado. El sistema lo registra como "Pago parcial", mantiene la factura abierta y calcula la deuda restante.
* **Doble contabilización prevenida:** Se recibe por error el mismo identificador de transacción duplicado. El sistema lo detecta, rechaza el segundo registro e informa del duplicado.

## CU09: Enviar Recordatorios y Notificaciones y Gestionar Comunicaciones

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Enviar recordatorios automáticos de pago, quedando detenidos al pago de la factura y notificando al administrador. Además, se tendrá una pantalla con todos los avisos/tareas que queden por realizar al abrir la aplicación, pudiendo utilizar una vía de comunicación para una mayor importancia.|
|**Actores**| Usuario Operativo.|
|**Requisitos**| FR6.1, FR6.3, FR6.4, FR7.4, FR8.1, FR8.2 |
|**Precondiciones**| La factura esta registrada o pendiente de cobro. |
|**Postcondiciones**| Se envían y registran las comunicaciones o se detienen los recordatorios al realizar el pago. |

#### Flujo Principal
1. Una factura alcanza su fecha límite de pago sin ser conciliada.
2. El sistema, según la cadencia configurada, genera una comunicación automática utilizando la plantilla correspondiente.
3. Se envía el recordatorio por Email/WhatsApp al contacto de facturación y el evento se registra en el histórico.

#### Flujos Alternativos
* **Pausa manual de recordatorios:** Un cliente reporta una incidencia con la factura. El usuario operativo la marca como "En disputa", pausando los recordatorios automáticos y estableciendo una fecha de revisión.

#### Flujos de excepción
* **Fallo en el canal de envío:** El servidor de correo rechaza el mensaje. El sistema anota el fallo de entrega, genera una alerta en la bandeja de tareas del usuario responsable y programa un reintento.

## CU10: Procesar la baja del Cliente

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Detener la generación de facturas, cuando un cliente se da de baja. Una vez esto ocurra, se deben resolver todos los pagos de facturas y se conservará el historial del cliente.|
|**Actores**| Administrador, Usuario Operativo.|
|**Requisitos**| FR4.4, FR5.4 |
|**Precondiciones**| El cliente quiere cancelar o finalizar el contrato. |
|**Postcondiciones**| La suscripción pasa a estado de baja, deteniendo la facturación, resolviendo todos los conflictos y conservando el historial. |

#### Flujo Principal
1. El administrador inicia el proceso de baja del cliente en el sistema.
2. El sistema cancela instantáneamente cualquier generación de facturación futura recurrente.
3. El sistema verifica si existen facturas pendientes de cobro y mantiene activo su proceso de seguimiento.
4. El perfil del cliente se conserva con todo su histórico bajo el estado "Inactivo".

#### Flujos Alternativos
* **Baja programada a futuro:** El administrador configura que la baja se haga efectiva el último día del mes en curso. El sistema mantiene la operativa normal y ejecuta la baja automáticamente llegada la fecha.

#### Flujos de excepción
* **Intento de borrado de base de datos:** Un usuario intenta eliminar permanentemente el registro del cliente. El sistema deniega la acción para cumplir con las normativas de conservación de datos, forzando un borrado lógico (inactivación).

## CU11: Búsqueda y Filtrado

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Buscar y filtrar clientes, contactos y facturas mediante diferentes criterios, como el nombre, identificador fiscal, contacto, estado.|
|**Actores**| Administrador, Usuario Operativo.|
|**Requisitos**| FR9.1 |
|**Precondiciones**| El usuario ha iniciado sesión en la plataforma. |
|**Postcondiciones**| El sistema muestra una lista de filtrados siguiendo los criterios. |

#### Flujo Principal
1. El usuario introduce un término de búsqueda (ej. razón social) en la barra principal.
2. El sistema procesa la consulta de manera eficiente.
3. El sistema devuelve un listado de resultados estructurados (clientes, facturas) en menos de 1 segundo.

#### Flujos Alternativos
* **Filtros compuestos:** El usuario navega a la sección de facturas y aplica combinaciones de filtros específicos ("Estado: Impagada" + "Sector: Retail" + "Fecha: Último trimestre").

#### Flujos de excepción
* **Cero resultados:** Los criterios introducidos no coinciden con ningún registro. El sistema muestra un mensaje claro ("No hay resultados para esta búsqueda") y ofrece limpiar los filtros.
* **Restricción de visibilidad por rol:** Un usuario operativo realiza una búsqueda amplia, pero el sistema omite de los resultados a los clientes a los que no tiene permiso explícito de acceso.

## CU12: Consultar Tablero e Informes Financieros 

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Mostrar el tablero financiero con indicadores clave y permitir la generación e exportación de informes de facturación en CSV o PDF.|
|**Actores**| Superadministrador, Administrador.|
|**Requisitos**| FR9.2, FR9.3 |
|**Precondiciones**| Existen registros de facturación guardados en el sistema. |
|**Postcondiciones**| Se visualiza el cuadro de mando actualizado o se genera la descarga del archivo del informe. |

#### Flujo Principal
1. El administrador accede a la sección del dashboard de negocio.
2. El sistema carga los gráficos, métricas de ingresos e indicadores de deuda leyendo los datos consolidados.
3. El usuario visualiza la información financiera actualizada en tiempo real.

#### Flujos Alternativos
* **Generación de informe exportable:** El administrador filtra un periodo específico (ej. trimestre anterior), selecciona "Exportar" y el sistema genera un archivo PDF/CSV que se descarga en el dispositivo local.

#### Flujos de excepción
* **Petición de exportación masiva pesada:** El usuario solicita un reporte de varios años. El sistema procesa la petición asíncronamente (en segundo plano), devuelve el control de la interfaz al usuario de inmediato y avisa cuando el archivo está listo.
* **Acceso denegado:** Un usuario operativo intenta forzar la URL del dashboard financiero global. El sistema detecta la falta de permisos y lo redirige a su panel inicial.

## CU13: Configuración Global y Auditoría del Sistema 

|Propiedad|Detalle|
|:---|:---|
|**Objetivo**| Configurar parámetros globales del sistemas, gestionar la API de integración y consultar los registros de auditoría y procesos automáticos.|
|**Actores**| Superadministrador.|
|**Requisitos**| FR10.1, FR10.2, FR10.3, FR10.4 |
|**Precondiciones**| El usuario inicia sesión como Superadministrador. |
|**Postcondiciones**| Se guardan las nuevas reglas de configuración global y quedan registradas las trazas de auditoría de las acciones realizadas. |

#### Flujo Principal
1. El superadministrador accede al módulo de configuración global.
2. Modifica una variable estructural de negocio (ej. actualiza un tipo impositivo o plazo de pago por defecto).
3. El sistema aplica y guarda la nueva configuración para futuras operaciones.
4. La plataforma registra la modificación en el historial de auditoría de forma inmutable.

#### Flujos Alternativos
* **Supervisión de procesos automatizados:** El superadministrador consulta los logs de sistema para comprobar el resultado de la última generación de facturas masiva de inicio de mes, validando el éxito de la tarea.

#### Flujos de excepción
* **Intento de alteración de trazabilidad:** Cualquier usuario con permisos intenta borrar o modificar una línea del log de auditoría. El sistema bloquea el intento directamente a nivel de base de datos.
* **Impacto retroactivo evitado:** Al cambiar una configuración global sensible (como una tarifa base), el sistema aísla y protege las facturas históricas ya emitidas, impidiendo que sus valores se recalculen.


