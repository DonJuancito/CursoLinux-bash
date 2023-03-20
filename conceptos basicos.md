Que es linux?

- En 1969 Kenneth Thompson y Dennis Ritchie (ATT&T Bell Labs) desarrolan UNIX OS en ensamblador
- En 1971 Thompson y Ritchie crean el lenguaje de programación C y reimplementa UNIX OS proprocionando portabilidad
- ATT&T era el unico propietario de Unix, por ello, en 1983 Richard Stallman inicia el proyecto GNU (GNU´s not Unix) para crear un sistema operativo gratuito 

CONCEPTOS BÁSICOS

- Kernel: Programa informático que se encuentra en el núcleo del sistema operativo de un ordenador y tiene un control total sobre todo lo que ocurre en el sistema.
- Siempre reside en la memoria, facilita las interacciones entre los componentes de hardware y software, gestiona la ejecución de procesos, maneja interrupciones...
- Se carga en una zona separada de la memoria protegida del acceso del software de aplicación o de otras parts menos críticas del sistema operativo.
- Espacio de usuario: Los programas de aplicación (navegadores, editores de texto, reproductores de video...) utilizan una zona de memoria separada.
- esta separacion evita que los datos del usuario y los del kernel interfieran entre si y provoquen inestabilidad y lentitud.
- inodos: Un inodo es una estructura de datos que mantiene un registro de todos los archivos y directorios dentro de un sistema de archivos Linux o basado en UNIX. De modo que cada archivo y directorio en un sistema de archivos tiene un inodo asignado, que se identifica con un número entero conocido como «número de inodo».
- dentries: Las dentries de un directorio se almacenan en una tabla. Esta tabla contiene la totalidad de nombres de los ficheros que están dentro del directorio y los asocia con su correspondiente número de inodo. Por lo tanto, una dentry es un nombre que apunta hacia un inodo.
- wildcards: Los wildcards son caracteres que representan un conjunto o rango. Con ellos se construyen las expresiones regulares. Suelen denominarse también 