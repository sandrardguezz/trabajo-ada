Requisitos funcionales
1. Login de usuarios:
Permitir iniciar sesión con correo de Turbine y contraseña.
2. Gestión de usuarios:
Permitir crear y gestionar usuarios internos que vayan a utilizar la aplicación.
3. Roles de usuario:
Diferenciar entre administrador y usuario con permisos limitados. El administrador
tendrá acceso global y el resto solo a lo que tenga asignado.
4. Asignación de clientes a usuarios:
El administrador podrá asignar clientes concretos a cada usuario para limitar qué
información puede consultar o modificar.
5. Configuración avanzada del sistema:
Debe existir un usuario con permisos especiales para modificar configuraciones
globales como plazos de pago o parámetros generales.
6. Gestión de clientes:
Los usuarios con los permisos correspondientes podrán crear, consultar, modificar y
gestionar los datos de los clientes desde la aplicación web.
7. Datos fiscales y de contacto del cliente:
Guardar los datos necesarios para facturar: empresa, persona de contacto, NIF,
dirección, datos de contacto, etc.
8. Buscar y filtrar clientes:
Permitir buscar empresas o personas y filtrarlas, por ejemplo, por ubicación o
actividad de la empresa.
9. Buscar y filtrar facturas:
Poder localizar facturas por fecha, estado de pago, tipo de factura, recurrencia, etc.
10. Crear facturas puntuales:
Permitir crear una factura que se genere una única vez para un cliente.
11. Crear facturación recurrente:
Permitir indicar que una facturación debe repetirse automáticamente cada mes.
12. Generar facturas recurrentes automáticamente:
Una vez configurada una factura recurrente, el sistema debe crear las siguientes
facturas sin tener que hacerlas manualmente cada mes.
13. Primera factura proporcional:
Si un cliente empieza a mitad de mes, generar una primera factura proporcional a
los días restantes y comenzar después la facturación mensual normal.
14. Modificar el importe de una factura:
Permitir definir y modificar la cantidad que se factura al cliente cuando se crea la
factura.
15. Gestionar el precio según facturación anual:
Tener en cuenta el rango de facturación anual de cada empresa para aplicar la tarifa
mensual correspondiente.
16. Generar factura en PDF:
Crear automáticamente el documento PDF que se enviará al cliente.
17. Formato estándar de factura:
Las facturas deben incluir numeración correlativa, datos fiscales, IVA y la
información necesaria.
18. Estética corporativa:
El PDF de la factura deberá mantener la imagen corporativa de Turbine.
19. Guardar facturas:
Conservar todas las facturas generadas y asociarlas al cliente correspondiente.
20. Consultar y descargar facturas:
Los usuarios autorizados podrán consultar y descargar las facturas a las que tengan
acceso.
21. Modificar facturas:
Permitir editar facturas mientras todavía puedan modificarse. Una vez cerrado el
período correspondiente no podrán cambiarse.
22. Enviar facturas al cliente:
Enviar la factura mediante correo electrónico o WhatsApp. La aplicación no tendrá
un chat propio.
23. Incluir datos de soporte en los avisos:
Los mensajes enviados al cliente podrán incluir email y teléfono de soporte para
posibles incidencias.
24. Consultar el estado del pago:
Comprobar en un sistema externo si una factura ha sido pagada. La aplicación no
será una pasarela de pago.
25. Detectar pagos automáticamente:
Actualizar automáticamente una factura cuando el sistema detecte que ha sido
pagada.
26. Notificar el cobro al responsable:
Avisar al usuario de Turbine responsable de ese cliente cuando se detecte el pago.
27. Enviar recordatorios de pago:
Enviar recordatorios automáticos mientras una factura siga pendiente.
28. Recordatorios antes del vencimiento:
Enviar la factura y recordatorios de pago alrededor de los días 3 y 5.
29. Gestionar impagos:
Si pasa el plazo de pago, iniciar un flujo de recordatorios periódicos hasta que se
pague la factura.
30. Detener los recordatorios cuando se pague:
Cuando se detecte el pago, parar automáticamente el flujo de reclamación de esa
factura.
31. Notificar impagos al responsable:
El usuario de Turbine asignado al cliente debe recibir información sobre los impagos
y su seguimiento.
32. Gestionar la facturación cuando un cliente solicita la baja:
Cuando un cliente solicite la baja, dejar de generar nuevas facturas recurrentes.
33. Control de baja con deudas pendientes:
Un cliente no podrá completar su baja mientras tenga facturas o deudas pendientes
de pago. Una vez pagadas, podrá finalizarse la baja.
34. Consultar si un cliente tiene facturas pendientes:
Permitir consultar si un cliente mantiene alguna deuda pendiente antes de
completar procesos como una baja.
35. Mantener el historial del cliente:
Cuando un cliente deje de estar activo, conservar su información mediante borrado
lógico durante el tiempo permitido.
36. Dashboard de facturación:
Mostrar al administrador un resumen de cómo evoluciona la facturación de la
empresa.
37. Informes por períodos:
Permitir consultar informes de facturación mensuales, trimestrales y anuales.
38. Historial de actividad:
Registrar acciones importantes realizadas dentro de la aplicación, como cambios,
pagos o modificaciones de permisos.
Buenas prácticas / funcionalidades deseables
● API general para futuras integraciones:
Dejar preparada la aplicación para que en el futuro otros sistemas puedan consultar
información.
● Importación de clientes mediante CSV:
Permitir cargar información de clientes sin tener que introducirlos manualmente uno
a uno.
● Aviso automático de cambio de tarifa:
Comprobar periódicamente la facturación anual del cliente y avisar si debe cambiar
de rango.
● Auditoría detallada:
Registrar quién ha realizado cada operación, cambio de permisos o modificación
importante.
● Copias de seguridad:
Disponer de mecanismos para conservar copias de la información y movimientos de
la aplicación.