¿QUÉ ES EL ENTORNO?

El entorno es un ocnjunto de informacion que se va a cargar en memoria RAM cuando nosotros nos autenticamos en el sistema cuando hacemos login y cuando abrimos una shell la informacion que se encuentra en el entorno variables de(entorno y la shell) funciones bash y los alias

COMANDOS

- printenv: nos saca por pantalla todo o parte del entorno
- set: saca por pantalla todo lo que se encuetra en el entorno 
- printenv PATH: nos saca las rutas donde estan

¿CÓMO SE ESTABLECE EL ENTORNO?

cuando nosotros hacemos login en la maquina lo que ocurre es que se van a ejecutar una serie de scripst de arranque lo que van hacer es componer el entorno van a crear y a definir las variables e entorno por defecto

SCRIPST DE ARRANQUE

fichero donde se definen variables de entorno en el sistema y para todos los usuarios
 (/etc/enviroment) {(pico /etc/environment)}
fichero para definir otras variables de entorno por norma general no debe de tocarse
 (/etc/profile) 
fichero para  otras variables de entorno que si se pueden modificar
 (/etc/profile.d)
fichero que aplica a todos los usuariosdel sitema permite definir variables de entorno que estan disponibles para programas que se ejecuten desde la shell
 (/etc/bash.bashrc)
ficheor que afecta a un usuario en particular
(/etc//profile)  

System Wide Scripts vs Session-wide Scripts
A continuación os dejo un resumen de los principales ficheros del entorno de Linux y sus características.

Ficheros con aplicación a todo el sistema (todos los usuarios del sistema)

/etc/enviroment → Fichero específico para la definición de variables de entorno. No puede contener scripts. Se ejecuta al iniciar el sistema.

/etc/profile → Permite definir variables de entorno y scripts, aunque no es apropiado modificar este fichero directamente (debe crearse un nuevo fichero en /etc/profile.d). Se ejecuta en shells con login.

/etc/profile.d → Contiene scripts que se ejecutan en shells con login.

/etc/bash.bashrc → Permite definir variables de entorno y scripts que estarán disponibles para programas iniciados desde la shell bash. Las variables que se definan en este fichero no van a estar disponibles para programas iniciados desde la interfaz gráfica. No se ejecuta en shells con login.

Ficheros con aplicación a un usuarios específico

~/.profile → Permite definir variables de entorno y scripts. Este fichero se ejecutará al iniciar la sesión de Escritorio o en una shell con login. Las variables afectan a todos los programas ejecutados desde el escritorio gráfico o desde la shell.

~/.bashrc → Permite definir variables de entorno y scripts. Se ejecuta cuando se abre la shell sin necesidad de hacer login. Es un fichero especifico de la shell bash, lo que quiere decir que las variables definidas solo afectaran a los programas ejecutados desde bash.

~/.bash_profile, ~/.bash_login → Permiten definir variables de entorno y scripts. Se ejecutan cuando se utiliza una shell con login. Son ficheros específicos de bash, lo que quiere decir que las variables definidas solo afectaran a los programas ejecutados desde bash.

MODIFICANDO EL ENTORNO

- echo $HOME: podriamos sacar el valor de cualquier variable del entorno
- HOME=/home/santi/Desktop: modificarle el valor de una variable de 
- export: nos define y exporta VARIABLE-NAME como variable en entorno al mismo tiempo que el asigna un valor. Si no usásemos el comando export , VARIABLE-NAME se mantendría como una variable normal.
- source .bashrc: forzamos a la shell para que vuelva a leer y ejecutar este fichero .bashrc

VARIABLES DE ENTORNO INTERESANTES

A continuación os dejo un listado de variables de entorno interesantes que debéis conocer.

SHELL → El nombre de la shell por defecto del usuario.

HOME → El nombre de la ruta de tu directorio personal.

LANG / LANGUAGE → Define el conjunto de caracteres y el orden de cotejo de su idioma.

PATH → Una lista separada por dos puntos de los directorios que se buscan cuando introducimos el nombre de un programa ejecutable.

PWD → El directorio de trabajo actual.

_ → Una referencia al programa /usr/bin/printenv (prueba a ejecutar el comando $_)

USER → Tu nombre de usuario.

Tened en cuenta que dependiendo de la distribución de Linux que estemos utilizando las variables de entorno que vienen definidas por defecto pueden variar.

PERSONALIZACION DE LA SHELL

- zsh: Z shell es un potente intérprete de comandos para sistemas operativos de tipo Unix, como por ejemplo los BSD o GNU/Linux.​ La primera versión de zsh fue escrita por Paul Falstad en 1990, cuando era estudiante en la Universidad de Princeton. Zsh se diseñó para poder usarse interactivamente
