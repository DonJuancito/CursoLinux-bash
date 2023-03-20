DEMONIOS Y SERVICIOS

 SCRIPST

 - ./apparmor status: queremos saber el estado en que se encuentra el servicio demonio en el sistema
 - ./apparmor stop: detiene un servicio 
 - ./apparmor start: arranca el servicio 

 - service apparmor status: da el estado del servicio actual
 - sudo service apparmor stop: detiene el servicio
 - sudo service apparmor restart:
 - sudo service apparmor start: inicia el servicio


 COMANDOS

 - systemctl: controla el sistema de gestion de servicios
 - systemctl stop apparmor: detiene un servicio
 - sudo systemctl status apparmor: da el estado del servicio actual por terminal
 - sudo systemctl start apparmor: arranca el servicio

 - systemctl list-units --type=service: para listar todos los servicios que tenemos en el sistema