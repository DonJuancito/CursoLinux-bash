Permisos en directorios
En muchas ocasiones puede resultar confusa la asignación de permisos a directorios. A continuación os dejo un pequeño resumen que podréis recordar fácilmente.

PERMISOS EN DIRECTORIOS:

El permiso de ejecución en los directorios permite acceder a los archivos dentro del directorio.

El permiso de lectura permite enumerar las entradas del directorio.

El permiso de escritura permite crear y eliminar entradas en el directorio.

Tener permiso de lectura o escritura en un directorio sin permiso de ejecución no es útil. Tener permiso de ejecución pero no de lectura es ocasionalmente útil: permite acceder a los archivos sólo si se conoce su nombre exacto, un mecanismo muy rudimentario de protección.

En la práctica los permisos útiles sobre un directorio son:

---: sin acceso

--x: puede acceder a los archivos cuyo nombre se conoce

r-x: acceso normal de sólo lectura

rwx: acceso normal de lectura y escritura