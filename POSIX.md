POSIX

El estándar POSIX incluye un número de clases que proporcionan rangos útiles de caracteres que podemos utilizar al construir una expresión regular.

A continuación se describen estas clases:

[:alnum:] → Los caracteres alfanuméricos. En ASCII, equivalen a: [A-Za-z0-9]

[:word:] → Lo mismo que [:alnum:], añadiendo el carácter de subrayado (_)

[:alpha:] → Los caracteres alfabéticos. En ASCII, equivalen a: [A-Za-z]

[:blank:] → Incluye los caracteres de espacio y tabulación

[:cntrl:] →  Los códigos de control ASCII. Incluye los caracteres ASCII 0 a 31 y 127

[:digit:] → Los números del 0 al 9

[:graph:] → Los caracteres visibles. En ASCII, incluye los caracteres 33 a 126

[:lower:] → Las letras minúsculas

[:punct:] → Los caracteres de puntuación. En ASCII, es equivalente a: [-!"#$%&'()*+,./:;<=>?@[\\\]_`{|}~]

[:print:] → Los caracteres imprimibles. Todos los caracteres de [:graph:] más el carácter de espacio

[:space:] → Incluye el espacio, el tabulador, el retorno de carro, la nueva línea, el tabulador vertical y el avance de forma. En ASCII, equivale a: [ \t\r\n\v\f]

[:upper:] → Las letras mayúsculas

[:xdigit:] → Caracteres utilizados para expresar números hexadecimales. En ASCII, equivale a: [0-9A-Fa-f]

