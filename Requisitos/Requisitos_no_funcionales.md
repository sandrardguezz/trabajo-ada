# REQUISITOS NO FUNCIONALES
## 1. Compatibilidad
   * Debe ser compatible con todo los tipos de SO
   * La interfaz web debe adaptarse correctamente a pantallas de ordenadores, móviles y tablets
     
## 2. Velocidad de busqueda
   * Las consultas y los accesos a los diferentes apartados deben hacerse en un tiempo muy bajo, a ser posible 1 minuto y en pocos clics
   * No quiere tener mil pantallas para acceder a una operación sencilla
   * Las acciones que son largas y costosas para el sistemas se deben ejecutar en segundo plano para permitir al usuario seguir actuando
     
## 3. Datos
   * Los datos de los clientes deben quedar guardados en la base de datos todo el tiempo que seas jurídicamente posible
   * Debe cumplir con la privacidad de los datos personales y fiscales de los clientes
   * Aunque el cliente se de baja debe mantenerse los datos de este
   * La base de datos y el sistema deben soportar un alto crecimiento futuro
   * Registro histórico inmutable de todas las acciones sensibles realizadas
   * Los datos no pueden estar en float para evitar el redondeo
   * Separar los archivos temporales de los oficiales
 
## 4. Accesibilidad
  * Facilidad para añadir y desactivar usuarios 
  * Para acceder al programa deben identificarse con una cuenta de turbineH verificado
  * Limitación de intentos fallidos de inicio de sesión
  * Las contraseñas no deben ser almacenadas en texto plano y todas las comunicaciones del sistema deben estar cifradas
  * Facilidad para cambiar de rol
  * Con el rol de administrador se debe acceder a todos los datos almacenados y hacer todas las acciones posibles
  * Con el rol de usuario, solo de debe acceder a los datos y campos seleccionados
  * Dejar constancia del receptor de las facturas y las notificaciones que se le envian a los trabajadores
  * El administrador debe poder acceder a los últimos accesos y cambios de cada uno de los usuarios
  * Debe permitir modificar el prototipo de facturas para un futuro
  * No se deben duplicar nada de los datos ni acciones si hay un fallo del sistema o una recarga
  * Los enlaces generados para acceder a documentos, deben requerir autenticación y caducidad

## 5. Notificaciones
   * Las notificaciones se harán a través de WhatshApp o Email, se elegirá en la ficha del cliente
   * Si llega un cobro sin referencia clara, debe quedar pendiente de revisión manual

## 6. Documentación:
   * Debe de dejarse una API documentada para futuras modificaciones o avances
   * Las claves de API de integraciones no deben incluirse ni en documentos fuentes ni en repositorios

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
  * Bloquear las facturas si falta un campo obligatorio, mostrando un mensaje de error de texto y no de codigo
## 8. Tipos de empresas
  * Cuando el responsable aprueba el cambio del numero de tipos, debe quedar registrado quién lo aprobó, cuándo y cuál era el precio anterior y el nuevo.
