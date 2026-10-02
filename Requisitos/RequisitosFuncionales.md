Requisitos funcionales

1.  Login de usuarios:

 Permitir iniciar sesi├│n con correo de Turbine y contrase├▒a.

2.  Gesti├│n de usuarios:

 Permitir crear y gestionar usuarios internos que vayan a utilizar la aplicaci├│n.

3.  Roles de usuario:

 Diferenciar entre administrador y usuario con permisos limitados. El administrador
tendr├í acceso global y el resto solo a lo que tenga asignado.

4.  Asignaci├│n de clientes a usuarios:

 El administrador podr├í asignar clientes concretos a cada usuario para limitar qu├®
informaci├│n puede consultar o modificar.
5.  Configuraci├│n avanzada del sistema:

 Debe existir un usuario con permisos especiales para modificar configuraciones
globales como plazos de pago o par├ímetros generales.

6.  Gesti├│n de clientes:

 Los usuarios con los permisos correspondientes podr├ín crear, consultar, modificar y
gestionar los datos de los clientes desde la aplicaci├│n web.

7.  Datos fiscales y de contacto del cliente:

 Guardar los datos necesarios para facturar: empresa, persona de contacto, NIF,
direcci├│n, datos de contacto, etc.

8.  Buscar y filtrar clientes:

 Permitir buscar empresas o personas y filtrarlas, por ejemplo, por ubicaci├│n o
actividad de la empresa.
9.  Buscar y filtrar facturas:

 Poder localizar facturas por fecha, estado de pago, tipo de factura, recurrencia, etc.

10. Crear facturas puntuales:

 Permitir crear una factura que se genere una ├║nica vez para un cliente.

11. Crear facturaci├│n recurrente:

 Permitir indicar que una facturaci├│n debe repetirse autom├íticamente cada mes.

12. Generar facturas recurrentes autom├íticamente:

 Una vez configurada una factura recurrente, el sistema debe crear las siguientes
facturas sin tener que hacerlas manualmente cada mes.

13. Primera factura proporcional:

 Si un cliente empieza a mitad de mes, generar una primera factura proporcional a
los d├¡as restantes y comenzar despu├®s la facturaci├│n mensual normal.

14. Modificar el importe de una factura:

 Permitir definir y modificar la cantidad que se factura al cliente cuando se crea la
factura.

15. Gestionar el precio seg├║n facturaci├│n anual:

 Tener en cuenta el rango de facturaci├│n anual de cada empresa para aplicar la tarifa
mensual correspondiente.
16. Generar factura en PDF:

 Crear autom├íticamente el documento PDF que se enviar├í al cliente.

17. Formato est├índar de factura:

 Las facturas deben incluir numeraci├│n correlativa, datos fiscales, IVA y la
informaci├│n necesaria.
18. Est├®tica corporativa:

 El PDF de la factura deber├í mantener la imagen corporativa de Turbine.

19. Guardar facturas:

 Conservar todas las facturas generadas y asociarlas al cliente correspondiente.

20. Consultar y descargar facturas:

 Los usuarios autorizados podr├ín consultar y descargar las facturas a las que tengan
acceso.

21. Modificar facturas:

 Permitir editar facturas mientras todav├¡a puedan modificarse. Una vez cerrado el
per├¡odo correspondiente no podr├ín cambiarse.

22. Enviar facturas al cliente:

 Enviar la factura mediante correo electr├│nico o WhatsApp. La aplicaci├│n no tendr├í
un chat propio.

23. Incluir datos de soporte en los avisos:

 Los mensajes enviados al cliente podr├ín incluir email y tel├®fono de soporte para
posibles incidencias.

24. Consultar el estado del pago:

 Comprobar en un sistema externo si una factura ha sido pagada. La aplicaci├│n no
ser├í una pasarela de pago.

25. Detectar pagos autom├íticamente:

 Actualizar autom├íticamente una factura cuando el sistema detecte que ha sido
pagada.

26. Notificar el cobro al responsable:

 Avisar al usuario de Turbine responsable de ese cliente cuando se detecte el pago.

27. Enviar recordatorios de pago:

 Enviar recordatorios autom├íticos mientras una factura siga pendiente.

28. Recordatorios antes del vencimiento:

 Enviar la factura y recordatorios de pago alrededor de los d├¡as 3 y 5.

29. Gestionar impagos:

 Si pasa el plazo de pago, iniciar un flujo de recordatorios peri├│dicos hasta que se
pague la factura.

30. Detener los recordatorios cuando se pague:

 Cuando se detecte el pago, parar autom├íticamente el flujo de reclamaci├│n de esa
factura.

31. Notificar impagos al responsable:

 El usuario de Turbine asignado al cliente debe recibir informaci├│n sobre los impagos
y su seguimiento.

32. Gestionar la facturaci├│n cuando un cliente solicita la baja:

 Cuando un cliente solicite la baja, dejar de generar nuevas facturas recurrentes.

33. Control de baja con deudas pendientes:

 Un cliente no podr├í completar su baja mientras tenga facturas o deudas pendientes
de pago. Una vez pagadas, podr├í finalizarse la baja.
34. Consultar si un cliente tiene facturas pendientes:

 Permitir consultar si un cliente mantiene alguna deuda pendiente antes de
completar procesos como una baja.

35. Mantener el historial del cliente:

 Cuando un cliente deje de estar activo, conservar su informaci├│n mediante borrado
l├│gico durante el tiempo permitido.

36. Dashboard de facturaci├│n:

 Mostrar al administrador un resumen de c├│mo evoluciona la facturaci├│n de la
empresa.

37. Informes por per├¡odos:

 Permitir consultar informes de facturaci├│n mensuales, trimestrales y anuales.

38. Historial de actividad:

 Registrar acciones importantes realizadas dentro de la aplicaci├│n, como cambios,
pagos o modificaciones de permisos.

Buenas pr├ícticas / funcionalidades deseables

ÔùÅ  API general para futuras integraciones:

ÔùÅ

 Dejar preparada la aplicaci├│n para que en el futuro otros sistemas puedan consultar
informaci├│n.
Importaci├│n de clientes mediante CSV:
 Permitir cargar informaci├│n de clientes sin tener que introducirlos manualmente uno
a uno.

ÔùÅ  Aviso autom├ítico de cambio de tarifa:

 Comprobar peri├│dicamente la facturaci├│n anual del cliente y avisar si debe cambiar
de rango.

ÔùÅ  Auditor├¡a detallada:

 Registrar qui├®n ha realizado cada operaci├│n, cambio de permisos o modificaci├│n
importante.

ÔùÅ  Copias de seguridad:

 Disponer de mecanismos para conservar copias de la informaci├│n y movimientos de
la aplicaci├│n.


