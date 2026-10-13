Requisitos Funcionales
FR1. Gestión de acceso, usuarios y permisos
El sistema permitirá gestionar el acceso de los empleados de Turbine y controlar las funcionalidades e información disponibles para cada usuario.
FR1.1. Autenticación y recuperación de acceso.
El sistema permitirá iniciar sesión mediante correo corporativo de Turbine y contraseña, así como recuperar la contraseña mediante el correo corporativo.
FR1.2. Gestión de usuarios, roles y permisos.
Los usuarios autorizados podrán crear, modificar y desactivar cuentas internas. El sistema diferenciará entre superadministradores, administradores y usuarios operativos, aplicando los permisos correspondientes a cada uno.
Dependencias: FR1.1.
FR1.3. Asignación y delegación de clientes.
Los administradores podrán asignar clientes a usuarios operativos y delegarlos temporalmente a otros usuarios durante un periodo determinado.
Dependencias: FR1.2.
FR2. Gestión de clientes y contactos
El sistema permitirá a los usuarios autorizados gestionar la información necesaria de los clientes de Turbine y de las personas relacionadas con ellos.
FR2.1. Gestión de datos del cliente.
Los usuarios autorizados podrán crear, consultar y modificar clientes, incluyendo sus datos comerciales y fiscales, como nombre comercial, razón social, identificador fiscal, domicilio fiscal, país y moneda.
FR2.2. Gestión de contactos.
Cada empresa podrá tener una o varias personas de contacto con distintas funciones, como contacto comercial, de facturación o de cobro. Los contactos podrán marcarse como inactivos sin eliminar su información histórica.
Dependencias: FR2.1.
FR2.3. Detección y reactivación de clientes existentes.
El sistema advertirá de posibles clientes duplicados y permitirá reactivar la ficha histórica de un antiguo cliente cuando vuelva a contratar servicios, siempre que corresponda.
Dependencias: FR2.1.
FR3. Gestión de la relación comercial
El sistema permitirá mantener la información que define la relación comercial existente entre Turbine y cada cliente, diferenciándola de las facturas que posteriormente se generen.
FR3.1. Gestión del acuerdo comercial.
El sistema permitirá registrar la fecha de inicio, plan o servicio contratado, tarifa, responsable interno, condiciones de pago y documentación asociada al cliente.
FR3.2. Gestión de tarifas y revisión anual.
El superadministrador podrá configurar los rangos de facturación y sus tarifas. El sistema permitirá revisar periódicamente el rango correspondiente a cada cliente y proponer cambios que deberán ser validados antes de aplicarse.
Dependencias: FR3.1.
FR3.3. Gestión de descuentos y condiciones excepcionales.
El sistema permitirá registrar descuentos u otras excepciones económicas. Cuando la operación supere las condiciones establecidas, deberá quedar pendiente de aprobación por un usuario autorizado.
Dependencias: FR3.2.
FR4. Gestión de suscripciones y facturación recurrente
El sistema permitirá gestionar las suscripciones mensuales de los clientes y generar automáticamente las facturas recurrentes correspondientes.
FR4.1. Generación de facturación recurrente.
El sistema generará automáticamente las facturas mensuales correspondientes a las suscripciones activas.
FR4.2. Gestión del inicio y prorrateo.
Cuando corresponda, el sistema calculará la parte proporcional del primer mes y mostrará el cálculo antes de confirmar la suscripción. También permitirá configurar una fecha futura de inicio o excluir el prorrateo cuando exista una condición comercial que lo justifique.
Dependencias: FR4.1.
FR4.3. Pausa de suscripciones.
Los usuarios autorizados podrán pausar temporalmente una suscripción indicando el motivo y las fechas correspondientes. Durante la pausa no se generarán nuevas mensualidades.
FR4.4. Gestión de la baja.
Cuando la baja sea efectiva, se detendrá la generación de nuevas facturas recurrentes. Las facturas anteriores que continúen pendientes mantendrán su proceso de cobro.
Dependencias: FR4.1.
FR5. Gestión y emisión de facturas
El sistema permitirá crear, emitir, consultar y gestionar las facturas asociadas a los clientes.
FR5.1. Creación de facturas puntuales.
Los usuarios autorizados podrán crear facturas puntuales con una o varias líneas que incluyan concepto, cantidad, precio unitario, descuentos e impuestos.
FR5.2. Previsualización y validación.
Antes de emitir una factura, el sistema permitirá visualizarla y comprobará que contiene los datos obligatorios necesarios. Cuando se detecte un importe anómalo, podrá advertir al usuario antes de continuar.
Dependencias: FR5.1 o FR4.1.
FR5.3. Emisión, numeración y PDF.
Al emitir una factura se asignará una serie y numeración única y se generará el PDF correspondiente con los datos fiscales, conceptos, impuestos, totales, condiciones de pago e identidad corporativa de Turbine.
FR5.4. Ciclo de vida e histórico.
El sistema gestionará los estados necesarios de una factura y conservará el histórico y el documento emitido.
FR5.5. Modificación y rectificación.
Las facturas que todavía puedan modificarse podrán ser corregidas por usuarios autorizados. Una factura ya emitida no podrá alterarse silenciosamente y, cuando corresponda, se deberá realizar mediante el procedimiento de rectificación correspondiente.
Dependencias: FR5.3.
FR6. Gestión de comunicaciones y recordatorios
El sistema permitirá realizar y controlar las comunicaciones administrativas relacionadas con las facturas y sus pagos.
FR6.1. Envío y seguimiento de comunicaciones.
El sistema permitirá enviar facturas y otras comunicaciones mediante correo electrónico y, cuando corresponda, WhatsApp. Se registrarán el destinatario, canal, fecha y resultado del envío y podrán realizarse reintentos en caso de fallo.
FR6.2. Gestión de plantillas.
Los usuarios autorizados podrán disponer de plantillas para facturas, recordatorios y otras comunicaciones, utilizando información como empresa, número de factura, importe, vencimiento y datos de soporte.
FR6.3. Recordatorios automáticos de pago.
El sistema enviará recordatorios según una cadencia configurable y respetará las condiciones de pago particulares establecidas para cada cliente.
FR6.4. Pausa de recordatorios.
Un usuario autorizado podrá suspender temporalmente los recordatorios de una factura indicando el motivo y una fecha de revisión.
Dependencias: FR6.3.
FR7. Gestión y seguimiento de cobros
El sistema permitirá conocer y controlar el estado de los pagos asociados a las facturas sin actuar como pasarela de pago.
FR7.1. Recepción y consulta de pagos.
El sistema podrá consultar y recibir información de pagos procedente de fuentes externas o simuladas.
FR7.2. Conciliación de cobros.
El sistema intentará asociar los movimientos recibidos con sus facturas. Cuando exista una coincidencia clara podrá realizar la conciliación automáticamente y, cuando exista duda, dejará el movimiento pendiente de revisión manual.
Dependencias: FR7.1.
FR7.3. Gestión de duplicados y discrepancias.
El sistema evitará contabilizar varias veces el mismo pago y detectará diferencias entre el importe recibido y el importe pendiente antes de considerar una factura totalmente pagada.
Dependencias: FR7.2.
FR7.4. Finalización del seguimiento de cobro.
Cuando una factura quede correctamente pagada, el sistema detendrá sus recordatorios y notificará el cobro al responsable interno correspondiente.
Dependencias: FR6.3, FR7.2.
FR8. Gestión del trabajo administrativo
El sistema permitirá organizar los eventos y tareas administrativas que requieran la atención de los empleados de Turbine.
FR8.1. Notificaciones internas y tareas pendientes.
Los usuarios recibirán notificaciones sobre eventos relevantes relacionados con sus clientes y dispondrán de una pantalla de trabajo con vencimientos, impagos, conciliaciones pendientes, aprobaciones, revisiones y otras tareas.
FR8.2. Gestión de incidencias y comentarios.
Los usuarios podrán registrar incidencias asociadas a clientes o facturas, indicando responsable, estado y prioridad, así como añadir comentarios internos y mencionar a otros usuarios.
Dependencias: FR8.1.
FR9. Consulta, informes e importación de información
El sistema permitirá localizar, analizar, importar y exportar la información administrativa necesaria.
FR9.1. Búsqueda y filtrado.
El sistema permitirá buscar y filtrar clientes, contactos y facturas mediante criterios como nombre, razón social, identificador fiscal, contacto, número de factura, ubicación, sector, fecha o estado.
FR9.2. Dashboard e informes.
Los administradores podrán consultar un dashboard financiero y generar informes de facturación mensuales, trimestrales y anuales, aplicando los filtros disponibles.
FR9.3. Exportación de información.
Los usuarios podrán exportar la información a la que tengan permiso de acceso en formatos como CSV y PDF.
Dependencias: FR9.2.
FR9.4. Importación de clientes mediante CSV.
Los usuarios autorizados podrán importar clientes desde un archivo CSV. Antes de confirmar la operación se mostrará una previsualización, se podrán relacionar las columnas y se informará de errores o posibles duplicados.
FR10. Integración, configuración y trazabilidad
El sistema permitirá integrarse con otros sistemas, configurar las principales reglas de funcionamiento y mantener trazabilidad sobre las operaciones realizadas.
FR10.1. API de integración.
El sistema dispondrá de una API documentada mediante la que otros sistemas podrán consultar información autorizada sobre clientes, facturas y deudas pendientes, así como comunicar determinadas solicitudes sin saltarse las reglas de negocio de la aplicación.
FR10.2. Configuración global.
Los usuarios con permisos adecuados podrán configurar valores como tarifas, plazos de pago, cadencia de recordatorios, series de facturación, impuestos, canales y reglas de aprobación.
FR10.3. Auditoría de operaciones.
El sistema registrará las operaciones relevantes indicando, cuando corresponda, quién realizó la acción, cuándo se produjo y qué información fue modificada.
FR10.4. Seguimiento de procesos automáticos.
Los usuarios autorizados podrán consultar el resultado de procesos automáticos como la generación recurrente, los recordatorios o la conciliación, incluyendo los posibles errores producidos.