para idenficar si hay impresoras conectadas
(ls /dev/lp*)
para identificar dispositivos externos como discos duros usb 
(ls /dev/sd*)
para identificar un cd o un dvd
(ls /dev/sr*)

cd /var/log
sudo tail -f syslog