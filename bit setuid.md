COMANDO

pico test_prog.c
sudo su
gcc test_prog.c -o test_prog

LIBRERIAS

#include <stdio.h>
#include <stdlib.h>
#include <sys/types.h>
#include <unistd.h>

FUNCION PRINCIPAL

int main()

FUNCIONALIDAD

{
    setuid(0);
    system("ls/home/santi");
    return 0;
}
