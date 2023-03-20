la gestion de paquese corresponde con un metodo de instalar y mantener el software del sistema linux. 
Se corresponde con uno de los aspectos mas importantes y diferenciadores de una distribucion de linux. 
El software en linux cambia con mucha frecuencia. 
Compilar el codigo fuente e instalar el software cada vez que se realizan actualizaciones no es un procedimiento sencillo y practico. 
Diferentes distribuciones utilizan diferentes istemas de gestion de paquetes, hay dos tecnologias principales: 
- Estilo Debian (.deb): Debian, Ubuntu, Lunux Mint, Raspbian...
- Estilo RedHat (.rpm): Fedora, CentOS, RedHat, Open SUSE...

¿QUE ES UN PAQUETE?

se corresponde con la unidad basica de un sistema de gestión de paquetes.
Es un fichero comprimido que contiene un conjunto de ficheros relativos a una aplicación software.
Contiene metadatos.
Suele contener scripts para la instalación y desinstalación de la aplicación software.
El paquete no tiene por qué ser ceado por el desarrolador de la aplicación software.
En la mayoría de las ocasiones, el creador del paquete tiene que realizar algunas modificaciones sobre el código fuente de la aplicación para adaptarlo a una distribución 

¿QUÉ ES UN REPOSITORIO DE PAQUETES?

La mayoría de los paquetes se distribuyen a los usuarios a través de repositorios centrales.
Los repositorios son mantenidos por ca distribución de Linux.
Las distribuciones de Linus suelen tener varios repositorios centrales para soportar diferentes fases del ciclo de desarrollo de software (desarrollo, producción, software de terceros...)
Pueden añadirse repositorios de terceros para instalas software que no se encuentre en los repositorios mantenidos por la distribución de linux

¿QUÉ ES UNA DEPENDENCIA?

En muchas ocasiones las aplicaciones software comparten algunas funciones que se implementan en librerías o ficheros compartidos
Si una aplicación requiere una librería o fichero compartida se dice que tiene una dependencia
Los sistemas de gestión de paquetes proporcionan un mecanismo par resolver las dependencias e instalarlas cuando se instala un aplicación software

COMANDOS

- dpkg: El comando DPKG en Linux es una herramienta utilizada para administrar paquetes a través de su instalación, eliminación y compilación. Es el gestor de paquetes para Debian
- apt: El comando APT (Advanced Package Tool por sus siglas en inglés que traducen Herramienta Avanzada de Empaquetado) es un elemento de línea de comandos creado por el proyecto Debian con el objetivo de permitirle a los usuarios gestionar y administrar los paquetes de sus distribuciones de Linux Debian.
- sudo apt update: actualiza nuestros repositorios de paquetes
- apt-cache search openssh-server: para buscar un paquete en concreto
- sudo apt install openssh-server: para instalar un programa en concreto

INSTALACION MANUAL DE PAQUETES

- nessus: una herramienta que sirve para escaneos de debilidades
- sudo dpkg -i nessus 10.3.0: le indicamos que el paquete que le pasemos queremos instalarlo y si lo hacemos de nuevo intentara actualizarlo

ELIMINAR,LISTAR Y BUSCAR PAQUETES INSTALADOS

- sudo apt remove nessus: para eliminar el paquete que le indicamos
- sudo apt upgrade: actualiza todo el sofware a la ultima version que se encuentre disponible
- dpkg -l: nos elistar todo el software que tenemos
- dpkg -s: para buscar un paquete en concreto
  dpkg --status
  - apt show : para busquedas de paquetes
- dpkg -S: para exactamente de que paquete pertenece este fichero 

AÑADIR NUEVOS REPOSITORIOS DE PAQUETES

añadir nuevos repositorios no es una practica recomendada por lo general si queremos instalar un software en concreto o un paquete de un repositorio es mejor que descarguemos ese paquete de una manera segura en lugar de añadir ese nuevo repositorio al listado

- sudo add-apt-repository "": para añadir un nuevo repositorio
- sudo apt-key add archive-key.asc: Para importar la clave

Otra forma de añadir repositorios de paquetes
Es posible que alguno de vosotros se esté preguntando cuál es la forma ideal de añadir nuevos repositorios y por qué el comando apt-key add esta en desuso.

No es fácil encontrar buena información al respecto, por eso me gustaría dejaros por aquí un artículo que lo explica correctamente: https://askubuntu.com/a/1307181

