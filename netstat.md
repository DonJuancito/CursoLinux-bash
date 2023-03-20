COMANDOS

para instalarlo sudo apt install net-tools
- netstat: El comando netstat genera visualizaciones que muestran el estado de la red y estadísticas de protocolo. El estado de los protocolos TCP, SCTP y los puntos finales de UDP puede visualizarse en formato de tabla. También puede visualizarse información sobre la tabla de enrutamiento e información de interfaces. Nos ayuda a sacar un monton de informacion sobre la red
 - netstat -nr: saca la tabla de rutas
 - netstat -a: visualizar todas la conexiones
 - netstat -au: muestra las conexiones udp que esten establecidas o en estado de escucha
 - netstat -l: nos muestra las conexiones en estado de escucha
 - sudo netstat -pnltu: nos da todas la conexiones actuales evita sacarnos conexiones locales como hiperproceso
 - sudo netstat -pntu: nos da todas la conexiones actuales evita sacarnos conexiones locales como hiperproceso menos las que estan escuchando
 - netstat -s: saca las estadisticas de los protocolos que se estan utilizando en las diferentes interfazes