COMANDOS

- ip addr o ip a: vamos a obtener las interfaces disponibles direccion fisica y 
direccion ipv4 que se asigna a nuestra propia maquina
- ip -6 a: para sacarnos la direccion ipv6
- sudo ip a add 192.168.239.188/24 dev ens33: para añadir una nueva direccion ipv4
-sudo ip a del 0.0.0.0./0 dev ens33: para eliminar una direccion ip concreta
 - inet 0.0.0.0./0 nos identifica dentro de la red nuestra interfaz completa y nuestra tarjeta de red
 anotacion cidr: Classless Inter-Domain Routing o CIDR (en español enrutamiento entre dominios sin clases) se introdujo en 1993 por IETF y representa la última mejora en el modo de interpretar las direcciones IP. Su introducción permitió una mayor flexibilidad al dividir rangos de direcciones IP en redes separadas. De esta manera permitió:
 - Un uso más eficiente de las cada vez más escasas direcciones IPv4.
 - Un mayor uso de la jerarquía de direcciones (agregación de prefijos de red), disminuyendo la sobrecarga de los enrutadores principales de Internet para realizar el encaminamiento.
direccion ipuv6: La Dirección de Internet Protocol versión 6 (o dirección IPv6) es una etiqueta numérica usada para identificar una interfaz de red (elemento de comunicación/conexión) de un ordenador o nodo de red participando en una red IPv6. podriamos comunicarnos con dispositivos en nuestra red o una diferente

Dirección de broadcast
Es posible que alguno de vosotros se haya fijado en la siguiente dirección ip que aparece cuando ejecutamos el comando ip a.


¿Qué es esta dirección?

Esta dirección se denomina dirección de broadcast. Cada red o subred tiene una dirección de broadcast reservada que puede ser utilizada por todos los participantes de la red para enviar tráfico de red a todos los nodos. El broadcast permiten transmitir información a todos los dispositivos y componentes de la red sin necesidad de conocer sus direcciones IP individuales. Entre otras cosas, los routers de una red local utilizan la IP de broadcast para enviar paquetes HELLO a todos los nodos de la red, switches y otros routers para descubrirlos y obtener cierta información sobre ellos.

Para el que quiera seguir profundizando sobre esto, le recomiendo que revise el siguiente enlace: https://en.wikipedia.org/wiki/Broadcast_address

