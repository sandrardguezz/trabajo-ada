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
   * **Método de verificación:** Pruebas manuales intentando modificar los registros y comprobando si quedan constancia de todos los necesarios.


## 5.Gestión de datos:
### NFR11: Precisión de redondeo:
   * **Descripción:** Los valores numéricos deben introducirse y almacenarse con valores enteros para evitar errores en el redondeo.
   * **Criterio de aceptación:** Prohibido el uso de float o double en la base de datos.
   * **Método de verificación:** Pruebas de ejecución con decimales y revisión del diagrama DDL de la base de datos.

### NFR12: Inmutabilidad de facturas emitidas:
   * **Descripción:** Las facturas no podrán ser modificadas una vez presentadas a la administración.
   * **Criterio de aceptación:** Imposibilidad de hacer en la base de datos un DELETE o un UPDATE de una factura que está en estado "Emitida".
   * **Método de verificación:** Pruebas lanzando peticiones de modificación y borrado sobre las facturas emitidas.

### NFR13: Conservación de datos y escalabilidad de almacenamiento:
   * **Descripción:** Los datos de los clientes deben quedar guardados en la base de datos todo el tiempo que seas jurídicamente posible y deben poder soportar el crecimiento de datos a largo plazo.
   * **Criterio de aceptación:** Los clientes que están dados de baja conservan sus datos en la base de datos tanto personales como contables. Los tiempos de consultas con más de 100.000 facturas debe ser menor a 1 segundo.
   * **Método de verificación:** Pruebas de consultas a clientes inactivos. ºººººººººCOMO PRUEBO LO DE LA CANTIDAD DE FACURASººººº

### NFR14: Prevención de duplicados:
   * **Descripción:**No se deben duplicar nada de los datos ni acciones si hay un fallo del sistema o una recarga.
   * **Criterio de aceptación:** Np pueden haber recargos tras hacer estas acciones.
   * **Método de verificación:** Pruebas manuales de estas situaciones.

### NFR15: Almacenamiento diferenciado de archivos:
   * **Descripción:** Separar los archivos temporales de los oficiales y legales.
   * **Criterio de aceptación:** Eliminación automática de los archivos temporales tras un período configurable, manteniendo intactos los documentos legales y oficiales.
   * **Método de verificación:** Pruebas de limpieza y revisión de la base de datos del sistema transcurrido el teimpo indicado.
     

## 6. Mantenibilidad del sistema y documentación:
### NFR16: Flexibilidad de configuraciones:
   * **Descripción:** Las reglas globales (tarifas, impuestos, tipos de empresas, formatos de identificadores y moneda) deben ser alterados sin alterar los emitidos anteriormente.
   * **Criterio de aceptación:** La modificación de una tarifa o tipo de tarifas no afectará a las facturas anteriores.
   * **Método de verificación:** Pruebas de consultas a facturas anteriores tras haber realizado un cambio en alguna de las reglas globales.


  
  
