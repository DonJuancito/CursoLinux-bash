CONCEPTO

Las señales son mensajes enviados por el sistema operativo al proceso en ejecución. También puede verse como una forma de atender eventos, es decir, permiten interrumpir la ejecución de un proceso para atender la ocurrencia de un evento.

COMANDOS

- kill: En Unix y los sistemas operativos tipo Unix, kill es un comando utilizado para enviar mensajes sencillos a los procesos ejecutándose en el sistema. Por defecto el mensaje que se envía es la señal de terminación (SIGTERM), que solicita al proceso limpiar su estado y salir. Asignado el numero 9
 - kill -20 PID: para unterrumpir el proceso en primer plano
 - kill -18 PID: para detener el proceso pero puede continuar
 - kill -STOP o -19 PID: le dice al kernel parar el proceso de cualquier forma lo para forzosamente
 - kill -2 PID: se carga el proceso en ejecucion 
 - kill -KILL PID: interrupe su funcionamiento al proceso
 - kill -TERM O -15 PID:
 - killall: manda la señal a los procesos en funcion a su nombre

 