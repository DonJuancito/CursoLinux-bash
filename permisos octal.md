PERMISOS OCTAL

chmod (1,7) fichero

000: 0 ---
001: 1 --x
010: 2 -w-
011: 3 -wx
100: 4 r--
101: 5 r-x
110: 6 rw-
111: 7 rwx

setuid: Setuid o Set User ID es un tipo de configuración de permiso de archivo en el sistema operativo Linux que permite que un usuario pueda ejecutar un archivo o programa utilizando los privilegios de root.
 - chmod 4770 fichero rwx rwx --- 

detgid: Setgid o Set Group ID es un bit que permite que un determinado proceso adquiera los privilegios del grupo al que ha sido asignado un fichero o directorio en el sistema operativo Linux.
 - chmod 2770 fichero rwx rwx ---

sticky bit: El Sticky Bit o bit adhesivo es uno de los permisos especiales de acceso utilizado en ficheros y directorios del entorno Unix y derivados como GNU/Linux. Su objetivo es que solo el usuario creador pueda eliminar o renombrar un archivo en sistemas donde todos los usuarios tienen permisos de lectura y escritura. Dentro de directorios
 - chmod 1770 directorio rwx rwx --t