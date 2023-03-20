Actualizar la distribución de Linux

Una cosa interesante que debemos tener en cuenta es que un sistema Linux esta formado por diferentes componentes de software. Uno de ellos son los programas en espacio de usuario que hemos aprendido a instalar, eliminar y actualizar en las secciones anteriores. Sin embargo, hay otro componente software muy importante del que no hemos hablado, el kernel de Linux.

A medida que la tecnología avanza, los desarrolladores aplican parches y actualizaciones para el kernel de Linux. Estos parches pueden mejorar la seguridad, añadir funcionalidades o incluso mejorar la velocidad de funcionamiento del sistema operativo.

Si utilizas un sistema operativo Linux como Ubuntu, es una buena idea comprobar y actualizar el kernel regularmente.

Para ello, podemos seguir el siguiente proceso:

1. Comprobamos cuál es la versión actual del kernel. Para ello, ejecutamos el comando: 

uname -sr

2. Actualizamos los repositorios de paquetes:

sudo apt update

3. Actualizamos el kernel:

sudo apt dist-upgrade

4. Reiniciamos la máquina:

sudo reboot

5. Podemos comprobar la nueva versión con el comando:

uname -sr



El comando sudo apt dist-upgrade realiza también todas las funciones que incluye el comando sudo apt upgrade