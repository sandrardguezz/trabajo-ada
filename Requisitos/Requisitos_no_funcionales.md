# REQUISITOS NO FUNCIONALES

## 1. Compatibilidad
### NFR1: Compatibilidad en sistemas operativos y navegadores:

   * **Descripción:** Debe ser compatible con los principales tipos de sistemas operativos, sin instalaciones adicionales.
   * **Criterio de aceptación:** Debe funcionar al 100% en Chrome, Firefox, Safari y Microsoft Edge.
   * **Método de verificación:** Probando en los diferentes navegadores las funcionalidades de la web.
     
### NFR2: Diseño web adaptativo:
   * **Descripción:** Debe adaptarse a las diferentes pantallas de móviles, ordenadores, tablets y portatiles.
   * **Criterio de aceptación:** Debe verse correctamente y al completo en cualquiera de los dispositivos.
   * **Método de verificación:** Probando en los diferentes dispositivos si se ve y se adapta de forma correcta.

     
## 2. Rendimiento y eficiencia
### NFR3: Rendimiento del servidor en búsquedas y consultas:
   * **Descripción:** Las consultas de la base de datos, las búsquedas globales y la navegación deben tener una baja latencia para obtener una gran fluidez de uso.
   * **Criterio de aceptación:** El 95% de las consultas y búsquedas deben ejecutarse en menos de 1 segundo, independientemente del número de usuarios presentes.
   * **Método de verificación:**

### NFR4: Procesamiento de tareas pesadas:
   * **Descripción:** Las acciones que son largas y costosas para el sistemas se deben ejecutar en segundo plano para permitir al usuario seguir actuando.
   * **Criterio de aceptación:** El programa devolverá el control al usuario en menos de medio segundo tras ejecutar la tarea, informando el avance en un indicador.
   * **Método de verificación:**


## 3. Usabilidad
### NFR5: Velocidad de operación:
   * **Descripción:** Las tareas frecuentes como añadir un nuevo cliente, deben estar estar diseñadas para hacer en pocos clics y pocos pasos.
   * **Criterio de aceptación:** Un usuario que esté familiarizado con el sistema debe dar de alta un cliente en máximo 7 clics y un tiempo menor a 2 minutos.
   * **Método de verificación:** Pruebas de uso con usuarios reales contabilizando el numero de clics y el tiempo.
     
### NFR6: Mensajes de error:
   * **Descripción:** Los errores de verificación de usuario o fallos en el sistema con una factura, deben ser en lenguaje natural no con codigo.
   * **Criterio de aceptación:** Todos las posibles excepciones que pueda lanzar el código deben ser comprensibles.
   * **Método de verificación:** Pruebas introduciendo datos erróneos o incompletos.



 
## 4. Seguridad, autenticación y control de acceso
### NFR7: Control de acceso por roles:
   * **Descripción:** Para acceder al programa deben identificarse con una cuenta de turbine verificado y tendrá una serie de permisos según el rol que tenga asignado.
   * **Criterio de aceptación:** Todos los intentos de acceso con otros dominios deben fallar. Acceso denegado a un rol que no es el asignado al usuario.
   * **Método de verificación:** Pruebas manuales probando diferentes dominios e intentando cambiar de rol a uno no asignado.

### NFR8:  Comunicaciones seguras:
   * **Descripción:**  Las contraseñas no deben ser almacenadas en texto plano (deben custodiarse de forma segura), y todas las comunicaciones del sistema deben estar cifradas.
   * **Criterio de aceptación:** Cifrado de todo el tráfico web. Las contraseñas deben estar almacenadas en base de satos seguras. Ninguna clave de API puede aparecer en un repositorio.
   * **Método de verificación:** Pruebas con aplicaciones como Wireshark para capturar el trafico. ºººººººººººººººº

### NFR9: Protección en sesiones y expiración de enlaces:
   * **Descripción:** Limitación de intentos fallidos de inicio de sesión. Los enlaces generados para acceder a documentos, deben requerir autenticación y caducidad.
   * **Criterio de aceptación:** Tras 5 intentos fallidos de introducir la contraseña se debe bloquear la cuenta. Los enlaces generados para acceder a un documento caducaran en un máximo de 15 minutos y requerirán tener activo el token de sesión.
   * **Método de verificación:** Pruebas manuales intentando entrar con contraseñas erróneas, intentos de acceso a URLs expiradas o sin iniciar sesión.

### NFR10: Seguimiento de los registros:
   * **Descripción:** El sistema tendrá un informe histórico inalterable de todas las operaciones sensibles realizadas.
   * **Criterio de aceptación:** En el registro debe aparecer la acción realizada, a quién se le realizó, la fecha, el usuario y los respectivos cambios realizados.
   * **Método de verificación:** Pruebas manuales intentando modificar los registros y comprobando si quedan constancia de todos los necesairos.


## 5.Gestión de datos:
### NFR11: Precisión de redondeo:
   * **Descripción:** Los valores numéricos deben introducirse y almacenarse con valores enteros para evitar errores en el redondeo.
   * **Criterio de aceptación:** Prohibido el uso de float o double en la base de datos.
   * **Método de verificación:** Pruebas de ejecución con decimales y revisión del diagrama DDL de la base de datos.


    
  * Facilidad para añadir y desactivar usuarios 
  * Limitación de intentos fallidos de inicio de sesión
  * Facilidad para cambiar de rol
  * Dejar constancia del receptor de las facturas y las notificaciones que se le envian a los trabajadores
  * El administrador debe poder acceder a los últimos accesos y cambios de cada uno de los usuarios
  * Debe permitir modificar el prototipo de facturas para un futuro
  * No se deben duplicar nada de los datos ni acciones si hay un fallo del sistema o una recarga
  * 

  *    * Los datos de los clientes deben quedar guardados en la base de datos todo el tiempo que seas jurídicamente posible
   * Debe cumplir con la privacidad de los datos personales y fiscales de los clientes
   * Aunque el cliente se de baja debe mantenerse los datos de este
   * La base de datos y el sistema deben soportar un alto crecimiento futuro
   * Separar los archivos temporales de los oficiales

## 5. Notificaciones
   * Las notificaciones se harán a través de WhatshApp o Email, se elegirá en la ficha del cliente
   * Si llega un cobro sin referencia clara, debe quedar pendiente de revisión manual

## 6. Documentación:
   * Debe de dejarse una API documentada para futuras modificaciones o avances
 
## 7. Factura
  * Si aumentamos numero de tipos de empresa, las facturas anteriores no deben modificarse al abrirlas una vez hayan cambiado
  * La factura tiene que permitir aceptar cualquier moneda
  * Los impuestos de la factura deben poder configurarse
  * Las facturas deben cumplir con una numeracion correlativa estandar
  * Los campos del NIF tienen que ser capaces de introducir cualquier numeración y tipo
  * La dirección no tiene que tener campos obligatorios como la provincia, porque podemos facturar en otro país
  * Las facturas no podrán ser modificadas una vez presentadas a la administración
  * Debemos tener acceso a una lista ordenada de las facturas basándonos en diferentes criterios como el cliente, la fecha, el estado del pago y el tipo de empresa
  * Cualquier cambio en la factura debe quedar registrada su traza
  * Los prorrateos deben ser enviados a revisar antes de enviarse la correspondiente factura al cliente
  
## 8. Tipos de empresas
  * Cuando el responsable aprueba el cambio del numero de tipos, debe quedar registrado quién lo aprobó, cuándo y cuál era el precio anterior y el nuevo.
