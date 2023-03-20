INTERFACES DE RED

Una interfaz de red es el punto de interconexión entre una computadora y una red pública o privada. Una interfaz de red es generalmente una tarjeta de interfaz de red (NIC), pero no tiene que tener una forma física. En cambio, la interfaz de red se puede implementar en software.

dev: siempre se va a referir a la interfaz completa

COMANDOS

- ip: Funcionamiento del comando ip. La herramienta principal de iproute2 es el comando «ip», con el que podremos ver y configurar direcciones IP, ver y configurar tablas de enrutamiento, ver y configurar túneles IP, y también ver y configurar la interfaz física.
- ip route: con esto veremos la tabla de rutas en nuestro sistema nos indica hacia donde se va a dirigir el trafico de red en funcion del objetivo
- sudo traceroute: nos va a decir los saltos que van pegando nuestros paquetes de red por diferens routers hasta que llegan a su objetivo
- sudo traceroute -t: tratar de comunicarme con otro servidor
 - ip link o l: obtenemos las referencias de las interfaces dadas de alta en el sistema
 - ip l show dev ens33: nos va a sacar la informacion unicamente de la interfaz que le indicamos
 - ip -s link: para obtener estadisticas de las interfaces
 - ip -s link dev ens33: para obtener estadisticas del as interfaces de una interfaz en especifico
 - ip l ls up: nos dira las interfaces que esten en funcionamiento
 - ip l set ens33 down: para dejar inactiva una de las interfaces
 - ip l ls set ens33 up: nos iniciara la interfaz que le indiquemos


EXAMINAR LA RED

COMANDOS

- ping: El comando PING, o Packet Internet Groper, de Linux es una herramienta muy querida entre los comandos Linux. Su objetivo principal es administrar el estado de conectividad de red entre una fuente y un dispositivo, con la ayuda de una red IP.
 - ping 0.0.0.0
 - ping -c 5 0.0.0.0: solo envia 5 paquetes
- nmap: Nmap es un software de código abierto que se utiliza para escanear una red y sus puertos con el objetivo de obtener información importante sobre la misma para controlar y gestionar su seguridad. Es una aplicación que se utiliza normalmente para realizar auditorías de seguridad y monitoreo de redes.
 - sudo nmap -Ss 0.0.0.0/0: que escanee los host y los puertos activos  



