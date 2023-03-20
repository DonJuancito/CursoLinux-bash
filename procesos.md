PROCESOS EN LINUX

COMANDO

- ps: ps ("process status", estado de procesos en idioma inglés) es un comando asociado en el sistema operativo UNIX (estandarizado en POSIX y otros) que permite visualizar el estado de un Proceso (informática).
- ps aux: es mas utilizado que el ps
 - ps x: podemos ver todos los procesos que tenemos en el sistema
 (S): significa que el proceso esta dormido no esta corriendo en este momento esta esperando a ejecutarse esta esperando la pulsacion de una tecla
 (<): es de alta prioridad le va signar los recursos 
 (L): son procesos multi hilos
 (R): significa que el proceso esta ejecutandoce o listo para ejecutarse
- top: El comando top te permite ver las tareas del sistema que se ejecutan en tiempo real. Proporciona un buen resumen de tu sistema para verificar rápidamente si algo se destaca que pueda estar causando problemas con tu sitio web o servidor. 

INTERRUPCION DE PROCESOS

CTRL Z: para parar un proceso en ejecucion tambien lo envia a segundo plano
bg %1: activa el proceso que ya fue detenido anteriormente con el numero le pasamos el idenficador de ese job y con eso podemos ejecutarlo en segundo plano

PROCESOS EN SEGUNDO PLANO

- &: le indicamos a la shell que ejecute el comando en segundo plano
- jobs: podemos observar los procesos en segundo plano
- fg %1: lo manda a primer plano

INIT

En sistemas tipo Unix, init es el primer proceso en ejecución tras la carga del núcleo y el que a su vez genera todos los demás procesos. Se ejecuta como demonio y por lo general tiene PID 1

Las 6 etapas del proceso de arranque de Linux
¿Algunas vez te has preguntado que es lo ocurre desde que pulsas el botón de encendido de tu ordenador hasta que se carga el sistema operativo?

Las siguientes son las 6 etapas de alto nivel de un típico proceso de arranque de Linux.

BIOS: Basic input/output System executes GRUB (El sistema básico de entrada/salida ejecuta GRUB)
MBR: Master Boot Record executes GRUB (registro de arranque maestro ejecutado)
GRUB: Grand United Bootloader executes kernel (El gestor de arranque de gran unidad ejecuta el nucleo)
Kernel: Kernel executes /sbin/init (ejecuta el nucleo)
Init: init executes runlevel programs (init ejecuta programas de nivel de ejecución)
Runlevel: Runlevel programs are executed from /etc/rc.d/rc*.d/ (Los programas de nivel de ejecución se ejecutan desde /etc/rc.d/rc*.d/)

1. BIOS

BIOS significa Sistema Básico de Entrada/Salida

Realiza algunas comprobaciones de integridad del sistema

Busca, carga y ejecuta el programa cargador de arranque.

Busca el gestor de arranque en el disquete, cd-rom o disco duro. Puede pulsar una tecla (normalmente F12 o F2, pero depende de su sistema) durante el arranque de la BIOS para cambiar la secuencia de arranque.

Una vez que el programa de arranque es detectado y cargado en la memoria, la BIOS le da el control.

Así que, en términos simples, BIOS carga y ejecuta el cargador de arranque MBR.

2. MBR

MBR significa Master Boot Record.

Se encuentra en el primer sector del disco de arranque. Normalmente es /dev/hda, o /dev/sda

El MBR tiene un tamaño inferior a 512 bytes. Tiene tres componentes 1) información del cargador de arranque primario en los primeros 446 bytes 2) información de la tabla de particiones en los siguientes 64 bytes 3) comprobación de validación del mbr en los últimos 2 bytes.

Contiene información sobre GRUB (o LILO en sistemas antiguos).

Así que, en términos simples, el MBR carga y ejecuta el cargador de arranque GRUB.

3. GRUB

GRUB significa Grand Unified Bootloader.

Si tiene varias imágenes del kernel instaladas en su sistema, puede elegir cuál se ejecutará.

GRUB muestra una pantalla de bienvenida, espera unos segundos, si no introduce nada, carga la imagen del kernel por defecto como se especifica en el archivo de configuración de grub.

GRUB tiene el conocimiento del sistema de archivos (el antiguo cargador de Linux LILO no entendía el sistema de archivos).

El archivo de configuración de grub es /boot/grub/grub.conf (/etc/grub.conf es un enlace a esto)

Así que, en términos simples, GRUB sólo carga y ejecuta las imágenes del Kernel y del initrd.

4. Kernel

Monta el sistema de archivos raíz como se especifica en el "root=" en grub.conf

El Kernel ejecuta el programa /sbin/init

Como init fue el primer programa ejecutado por el Kernel de Linux, tiene el id de proceso (PID) de 1.

initrd significa Disco RAM Inicial.

El initrd es utilizado por el kernel como sistema de archivos raíz temporal hasta que el kernel es arrancado y el sistema de archivos raíz real es montado. También contiene los controladores necesarios compilados en su interior, que le ayudan a acceder a las particiones del disco duro y a otro hardware.

5. Init

Lee el archivo /etc/inittab para decidir el nivel de ejecución de Linux.

Los niveles de ejecución disponibles son los siguientes

0 - halt

1 - Modo de usuario único

2 - Multiusuario, sin NFS

3 - Modo multiusuario completo

4 - sin uso

5 - X11

6 - reinicio

Init identifica el nivel por defecto sus ficheros de configuracion y lo utiliza para cargar el resto de programas.

Ejecuta el comando runlevel en su sistema para identificar el nivel de ejecución por defecto

Típicamente, el nivel de ejecución por defecto se establece en 3 o 5.

6. Programas de nivel de ejecución

Cuando el sistema Linux está arrancando, puede ver que se inician varios servicios. Estos son los programas de nivel de ejecución, ejecutados desde el directorio de nivel de ejecución definido por su nivel de ejecución.

Dependiendo de su configuración de nivel de init por defecto, el sistema ejecutará los programas desde uno de los siguientes directorios.

Nivel de ejecución 0 - /etc/rc.d/rc0.d/

Nivel de ejecución 1 - /etc/rc.d/rc1.d/

Ejecuta el nivel 2 - /etc/rc.d/rc2.d/

Ejecutar el nivel 3 - /etc/rc.d/rc3.d/

Ejecutar el nivel 4 - /etc/rc.d/rc4.d/

Ejecutar el nivel 5 - /etc/rc.d/rc5.d/

Ejecutar el nivel 6 - /etc/rc.d/rc6.d/

Ten en cuenta que también hay enlaces simbólicos disponibles para estos directorios bajo /etc directamente. Así, /etc/rc0.d está vinculado a /etc/rc.d/rc0.d.

Bajo los directorios /etc/rc.d/rc*.d/, verá programas que comienzan con S y K.

Los programas que empiezan por S se utilizan durante el arranque. S para el arranque.

Los programas que comienzan con K se utilizan durante el apagado. K para matar.

Hay números justo al lado de S y K en los nombres de los programas. Estos son el número de secuencia en el que los programas deben ser iniciados o eliminados.

Por ejemplo, S12syslog es para iniciar el deamon del syslog, que tiene el número de secuencia 12. S80sendmail es para iniciar el demonio sendmail, que tiene el número de secuencia 80. Así, el programa syslog se iniciará antes que sendmail.



¡Bien! Pues ahora ya sabes lo que ocurre durante el arranque de un sistema operativo Linux.

¡Espero que te haya resultado interesante y nos vemos en la siguiente sección!



