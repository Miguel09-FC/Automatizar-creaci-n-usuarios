# Automatizar la creación usuarios
## Resumen Detallado

Este conjunto de scripts PowerShell simplifica el proceso de administración de recursos humanos y Active Directory. El script de recopilación interactúa con los usuarios para obtener datos clave, los estructura en un objeto JSON y los almacena en un archivo compartido. El script de creación utiliza estos datos para automatizar la creación de usuarios en Active Directory, aplicando configuraciones específicas, como contraseñas seguras y pertenencia a grupos sectoriales. La capacidad de mover los archivos procesados a una carpeta de respaldo mejora la trazabilidad. Antes de ejecutar, es crucial personalizar las rutas según el entorno y garantizar la seguridad de las contraseñas. 

## Que se debería hacer:

En mi caso yo he transformado los scripts a ejecutables y el formulario está en una carpeta compartida que tiene acceso recursos humanos para que cuando contraten un nuevo empleado rellene el formulario, los otros dos scripts están en el servidor, que se activan con tareas programadas. El script de crear usuarios se inicia 15 minutos antes de que llegue el primer empleado a la empresa y este script monitoriza la carpeta caliente y cuando hay un archivo "json" nuevo se ejecuta y crea un nuevo usuario con los datos del archivo. El script de cierre lo que hace es cerrar el proceso de creación de usuarios 15 minutos después del cierre de la oficina.

