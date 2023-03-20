LA SHELL DE LINUX

El prompt: Incluye el nombre de usuario y el nombre de la maquina que estemos utilizando, tiene el directorio donde nos encontramos $ nos indica en donde podemos empezar a escribir comandos

Cuando ka shell nos dice que un comando "is hashed", significa que ya ha resuelto su ruta y la ha guardado en la hash table para acceder a ella mucho mas rapido

COMANDOS

- clear: Ayuda a limpiar la pantalla
- history: Nos muestra el historial de comandos 
que hemos utilizado
- ls: podemos listar los archivos y directorios que tenemos en la carpeta donde nos encontramos
- ls log: para visualizar el contenido de un directorio
- mkdir: podemos crear un nuevo directorio
- type: nos dice que tipo de comando es el que pongamos a continuacion
- cp: nos permite copiar ficheros y directorios
- ls -l: nos da mas informacion de la carpeta actual que estemos usando
- ls -la: nos da informacion de los ficheros y directorios disponibles en la carpeta y los que estan ocultos tambien
- ls -t: nos ordena las carpetas y los archivos por modificacion reciente
- ls -lah: nos da la misma informacion pero en un formato mas facil de leer y comprender por un humano
- help: nos permite recibir informacion de los comandos
- --help
- -h
- man: 
- whatis ls: nos dice para que sirve el comando
- info: nos sirve para ver informacion mas detallada sobre los comandos
- apropos: nos propone comandos de manera automatica de la palabra que pongamos a continuacion
- exit: nos saca de la terminal
- alias: nos ayuda para asignar un nuevo nombre a un comando
- unalias: sirve para eliminar el alias que hayamos creado
- hash: sirve para comprobar que comandos hay en la hash table
- hash -r: sirve para eliminar todas las entras de la hash table y que ningun comando aparezca como "is hashed"
- pwd: sirve para sacar en la pantalla la carpeta o directorio en el que trabajamos en el momento
- cd: sirve para movernos entre directorios
- cd -: sirve para devolvernos al fichero anterior
- pico: abre un editor de texto en la shell
- nano: abre otro director de texto parecido a pico
- vim """""
- vi """""
- emacs
- sudo apt install: nos ayuda a instalar cosas fuera de la shell
- file: nos sirve para saber que tipo de contenido que tiene un fichero  
- cat: mostrarnos por pontalla todo el contenido de un fichero
- more: nos muestra contenido del fichero de una forma mas lenta
- less: es la evolucion de more
 - si pulso q me pasa a la pagina siguiente
 - si pulso b me pasa a la pagina anterior
 - /texto para buscar algo en especifico dentro del fichero
 - si pulso n busca coincidencias en otras paginas
 - si pulso la g volvemos al comienzo del fichero
 - si pulso la G voy al final del fichero
- cp: sirve para copiar ficheros o directorios
- cp -i: nos pregunta de manera interativa si queremos sobrescribir en otro fichero lo que queremos copiar
- cp -r: nos sirve para copiar directorios
- mv: sirve para mover un fichero a otro directorio o tambien para mover los directorios
 - sirve tambien para cambiar el nombre de fichero moviendolo al mismo directorio pero con otro nombre
 - se puede hacer lo mismo con los directorios
- mv -u: sirve para no mover los ficheros y ya hay unos dentro del directorio mas recientes o actualizados
- rm: para eliminar ficheros
- rm -r: para eliminar directorios
- rm -rf: fuerza la eliminacion de lo que haya 
- find: nos permite buscar un archivo
 - se pone primero el argumento en donde queremos que lo busque
 - despues del argumentocon -name le indicamos lo que queremos buscar realmente
 - 2> /dev/null: para evitar informacion innecesaria
 - -ls: me da mas informacion de lo que buscamos
 - -name '*': esto busca cualquier cosa que tenga por delante
 - -type: se escribe al final para indicar que busque un directorio
 - -user: cuando queremos encontrar un directorio o fichero que haya sido creado por un usuario en espesifico
- !-path"/nombre de la ruta/*": excluimos todos los resultados cuya ruta comience por lo que hayamos escrito
- tree: nos permite mostrar de manera gráfica y de forma estructurada la jerarquía de los directorios de nuestro sistema operativo. El comando tree además permite listar los directorios de los dispositivos externos.
- ps: ps ("process status", estado de procesos en idioma inglés) es un comando asociado en el sistema operativo UNIX (estandarizado en POSIX y otros) que permite visualizar el estado de un Proceso (informática).
- prlimit: con esto limitamos la cantidad de memoria ram que puede consumir el proceso
- stat: El comando Stat es utilizado en el sistema Linux o Unix con el objetivo de mostrar información a detalle sobre archivos y sistemas de archivos. Con este comando podremos obtener datos de ficheros como lo relacionado con el tipo de archivo, su tamaño, permisos e inodos.
- debugfs -R "stat:
- ln -s: sirve para crear enlaces simbolicos 
- which: Hoy veremos de que se trata el comando which, para Linux, básicamente es una herramienta que permite encontrar rápidamente los archivos ejecutables de una determinada aplicación, este comando viene por defecto en la mayoría de las distribuciones GNU/Linux.
- less: ¿Qué es el comando less en Linux? Con less, puedes leer grandes archivos de texto sin saturar la pantalla de tu terminal. También puedes buscar texto y monitorear archivos en tiempo real con él. Algunas personas prefieren usar Vim para leer archivos de texto grandes.
- sed: es otro comando interesante que es posible que os resulte de utilidad en algunas ocasiones. Su función principal es reemplazar texto de un fichero. Sin embargo, puede combinarse con los comandos que hemos visto en este tema utilizando pipelines para realizar otras muchas tareas.
- id: El comando id muestra el UID y el GID del usuario especificado, además de sus grupos secundarios. Si no se especifica ningún usuario se refiere al usuario que ejecuta la orden.
- chmod: chmod, que significa "cambiar modo" (del inglés: "change mode"), es un comando asociado con el sistema operativo UNIX (estandarizados en POSIX y otros estándares) que permite la asignación de permisos de acceso a carpetas o directorios​. Para cambiar los permisos de un archivo o directorio de un servidor con sistema Linux, tienes que utilizar el comando chmod.
- umask: El UMASK en los sistemas Linux o Unix se conoce como Máscara de Usuario o también se denomina Máscara de creación de archivos de usuario. Es un permiso base o por defecto cuando se crea un nuevo archivo o carpeta en la máquina Linux

PIPELINES

- sort: El comando sort (ordenar) es un comando para ordenar líneas de archivos de texto. Permite ordenar alfabéticamente, en orden inverso, por número, por mes y también puede eliminar duplicados.
- uniq: El comando uniq suprime o informa de líneas duplicadas consecutivas que contiene un fichero o la entrada estándar.
- wc: wc (word count) es un comando utilizado en el sistema operativo Unix que permite realizar diferentes conteos desde la entrada estándar, ya sea de palabras, caracteres o saltos de líneas.
- grep: El comando grep perteneciente a la familia Unix es una de las herramientas más versátiles y útiles disponibles. Este busca un patrón que definamos en un archivo de texto. En otras palabras, con grep en Linux puedes buscar una palabra o patrón y se imprimirá la línea o líneas que la contengan.
- grep -i: ignorara las mayusculas y las minusculas
- grep -v: nos sacara las lineas que no coincidan con ese patron
- head: El comando Linux Head, al igual que el comando Linux Tail, forma parte de las herramientas esenciales de la línea de comandos. Este comando sirve principalmente para mostrar al principio de un archivo (de texto) o para reducir a lo especificado los datos mostrados por un comando de Linux.
 - -n: para modificar cuantos queremos en especifizo
- tail: El comando tail de Linux es una de las herramientas fundamentales de la línea de comandos. Principalmente, el comando se utiliza para mostrar las últimas líneas de un archivo (de texto) o para restringir la salida de un comando de Linux a un ámbito concreto.
 - -n: para modificar cuantos queremos en especifizo
 - -f: para ver en tiempo real lo que se escribe dentro del fichero
- tee: Con el comando tee, Linux ofrece la posibilidad no solo de dar salida a la entrada estándar de forma normal, sino también de escribirla en uno o más archivos. Con ello, este comando es una solución útil para guardar los resultados intermedios, archivarlos o examinarlos en busca de fuentes de error.
- adduser: Con el comando useradd podemos crear usuarios desde el terminal. Crea el usuario asolano pelado, sin contraseña, sin interprete de comandos, sin directorio de usuario. Ahora ya tenemos el usuario depruebas creado y con contraseña y ya podemos entrar al sistema con depruebas.
- exit: El uso de exit permite saber al usuario si una acción se ha realizado correctamente o no. Cuando un comando se ha ejecutado correctamente, devuelve 0. En caso contrario, devuelve otro valor.
- sudo: En otras palabras, Sudo sirve para elevar privilegios temporalmente, con el fin de ejecutar comandos o archivos que requieren permisos especiales.El comando sudo permite a los usuarios no root ejecutar otros comandos Linux que normalmente requerirían privilegios de superusuario, mientras que el archivo sudoers le indica al sistema cómo manejar el comando sudo.
 - sudo -i: nos permite crear una seccion interactiva con el usuario que tengamos creado en el fichero de sudoers
 - sudo -a: le indicamos que añada este grupo a los que ya tienen
 - sudo -G: que añada un nuevo grupo por lo general va despues de -a
   {(sudo usermod -a -G newgroup newuser)}
 - sudo -g: es para cambiar el grupo primario del usuario 
   {(sudo usermod -g newgroup newuser)} 
 - sudo -l: podemos cambiarle el nombre al usuario que pongamos a continuacion
   {(sudo usermod -l newuser2 newuser)}
 - sudo -d: sirve para cambiar el home del usuario
   {(sudo usermod -d /home/santi newuser2)} 
 - sudo -u: para cambiar el uid del usuario
   {(sudo usermod -u 250 newuser2)} 
 - sudo -L: para bloquear a un usuario
 - sudo -U: para desbloquearlo  
 - visudo: visudo, el comando que permite al administrador modificar /etc/sudoers. /etc/sudoers, el archivo de permisos que le indica a sudo qué usuarios ejecutan qué comandos.
- groupadd: Puede utilizar el mandato groupadd para crear un grupo Linux. Este mandato groupadd añade el grupo denominado staff. En sistemas Netezza HA, después de añadir el grupo Linux en un host, deberá crear el mismo grupo con el mismo valor de id de grupo en el otro host.
- usermod: El comando usermod permite modificar usuarios existentes en el sistema. Con este comando asignamos al usuario jose al grupo ministros en caso de existir.
- passwd: para cambiar la contraseña de un usuario
  {(sudo passwd newuser2)}
- delgroup: sirve para eliminar un grupo  # no se puede eliminar un grupo si el usuario lo tiene como grupo primario en ese caso se tendria que eliminar el usuario primero
  {(sudo delgroup newgroup)}   
- deluser: para eliminar un usuario
  {(sudo deluser newuser)}  
 - para eliminar un directorio de trabajo de un usuario ya eliminado se utiliza el siguiente comando
  {(sudo deluser --remove-home newuser)}  
 - para eliminar todos los directorios y ficheros usados por el usuario se utilizaria el siguiete comando
  {( sudo deluser --remove-all-files newuser)}
- strings: Muestra las cadenas de caracteres imprimibles que contengan los ficheros, útil para visualizar ficheros que no sean, o que no se sepa que son de texto plano.
- mount: nos monta un sistema de ficheros. mount es un comando de sistemas basados en Unix que se utiliza para montar dispositivos y particiones para su uso por el sistema operativo. Montar es hacer que el sistema operativo proyecte el contenido de ese dispositivo o partición en un enlace lógico (un directorio).
- umount: desmonta ficheros de nuestro fichero principal. El comando umount le permite eliminar un sistema de archivos remoto que esté montando en la actualidad. El comando umount se puede utilizar con las opciones siguientes: –V. Permite realizar pruebas.

CAMBIOS DE PROPIETARIOS Y GRUPOS

- chown: Con las opciones chown, se puede cambiar la propiedad de los archivos, directorios y enlaces. Si un usuario normal desea realizar ciertos cambios en un archivo, un superusuario puede usar comandos chown para cambiar la propiedad y permitirlos.
  {(sudo chown newuser prueba.txt)}
  para cambiar el grupo propietario
  {(sudo chown:newgroup prueba.txt)}

INTALACION

instalar desde github un directorio de metasploit
{(sudo apt install git)}
copiar la url desde la pagina
{(git clone pegar el url)}