# REQUISITOS DE USUARIO
## 1. Acceso
  * El usuario debe poder acceder con un email de Turbine y contraseña.
  * El usuario debe poder recuperar su contraseña mediante un enlace que caduca.
  * El usuario debe poder usar la aplicación desde ordenador, tablet y móvil. Desde el móvil, como mínimo, podrá consultar clientes, aprobar solicitudes, ver impagos, marcar incidencias y revisar pagos.
  * No hay autorregistro, un usuario es registrado por invitación o cuenta creada desde la aplicación.
  * La sesión debe cerrarse tras un tiempo de inactividad y el usuario debe poder cerrarla manualmente.
## 2. Roles
  * El usuario puede ser superadministrador, administrador o usuario operativo o lector.
  * Cada cliente debe tener un usuario de Turbine asignado como responsable.
  * Ningún usuario puede acceder a clientes, facturas o documentos que no le correspondan, aunque entre directamente por URL.
  * Las acciones relevantes de todos los usuarios quedan registradas en la auditoría (quién, qué y cuándo).
### Rol de superadministrador
  * El superadministrador debe poder configurar el sistema (plazo de pago por defecto, cadencia de recordatorios, tabla de rangos y tarifas, series de numeración, umbrales de aprobación, dominio de correo permitido, datos fiscales y logo de Turbine, monedas, impuestos, canales de notificación y políticas de automatización).
  * Debe poder aprobar descuentos que superen el umbral configurado.
  * Debe poder crear e invitar a nuevos usuarios.
  * Consultar y filtrar la auditoría.
  * Debe poder elegir qué notificaciones recibe y el canal que se usa.
  * Tiene todas las capacidades del administrador.
  * No puede modificar ni borrar la auditoría.
### Rol de administrador.
  * Puede gestionar todos los clientes, no solo los asignados.
  * Gestiona las operaciones, clientes, facturas y aprobaciones.
  * Asignar clientes y designarlos a usuarios operativos.
  * Delegar los clientes por vacaciones.
  * Reasignar aprobaciones.
  * Aprobar cambios económicos sensibles como descuentos (siempre que no superen el umbral del superadministrador), importes modificados, vencimientos o facturas puntuales.
  * Ver bandeja de notificaciones.
  * Ver el dashboard financiero.
  * Configurar informes programados.
  * Crear o invitar a usuarios si tiene permiso para ello.
  * Desactivar usuarios.
  * Puede declarar incobrable una deuda, con motivo y aprobación.
  * Puede cerrar periodos administrativos.
  * Puede realizar acciones masivas, como reasignar los clientes de un empleado que se va.
  * No puede aprobar sus propias solicitudes cuando se exige separación de funciones.
### Rol de usuario operativo o lector
  * Ver y modificar su información operativa (CRUD sobre lo asignado).
  * Crear facturas si su permiso lo permite.
  * Seguimiento de cobros y descargar documentos.
  * Recibir notificaciones de sus clientes.
  * Preparar propuestas o solicitar descuentos.
  * Marcar facturas como "en disputa" y pausar sus recordatorios si tiene ese permiso.
  * Abrir incidecias, comentar y mencionar a compañeros.
  * Exportar solamente lo que puede ver.
  * Configurar preferencias personales (ejemplo: resumen por email).
  * No puede acceder a clientes no asignados ni darse acceso a sí mismo.
  * No puede ver el dashboard financiero global.
  * No puede cambiar tarifas globales ni crear series de facturación.
  

  
