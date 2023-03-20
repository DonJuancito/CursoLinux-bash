COMANDOS

- grep: El comando grep perteneciente a la familia Unix es una de las herramientas más versátiles y útiles disponibles. Este busca un patrón que definamos en un archivo de texto. En otras palabras, con grep en Linux puedes buscar una palabra o patrón y se imprimirá la línea o líneas que la contengan.

- .: para refenciar cualquier caracter
- ^: indicamos que debe de aparecer al comienzo de la linea
- $: indicamos que debe terminar al final de la linea
- []: especificamos un rango de caracteres en el patron que estemos buscando
- [^]: que no aparazca un caracter entre los corchetes
- [-]: concepto de rango

EXTENDIDO

- |: indicamos expresiones regulares completas indicamos de manera alternativa que busca expresiones de manera separada
- ^(): indicamos que salgan en las primeras lineas los patrones que indicamos

CUANTIFICADORES

siempre se pone despues de los caracteres
- ?: indicamos que el caracter que este anterior de el aparezca 0 o 1 vez despues del patron
- *: indicamos que un caracter puede aparecer 0 o mas veces despues del patron
- +: indicamos que un caracter puede aparecer 1 o mas veces despues del patron
- {}: especificamos que un caracter aparezca un numero determinado de veces
- {0,0}: especificamos que un caracter aparezca como minimo un numero determinado de veces y como maximo igual 
- {,0}: indicamos que puede aparecer minimo cualquier numero de veces pero como maximo lo que nosoytos le indiquemos

