SHELL SCRIPT O BASH SCRIPT

#!/bin/bash= indica el programa con el que se va a ejecutar
#!/bins/sh= """"""""

mkdir shell_scripts.sh
emacs -nw nmap-parser.sh
echo > resultados_nmap.html

declare -r TITULO="resultados nmap"                                     # variable asignada a un valor
FECHA_ACTUAL="$(date)"                                                  # variable para mostrar la fecha actual
TIMESTAMP="Informe generado el $FECHA_ACTUAL por el usuario $USERNAME   # sabemos quien a generado el informe y en que   fecha se genero este informe

echo "<html>"                                                # saca los tags html
echo "    <head>"                                            # ponemos la cabezera
echo "        <title>resultados nmap</title>"                # le ponemos un titulo
echo "    </head>"                                           # cerramos la cabezera
echo "    <body>"                                            # le ponemos un body
echo "        <h1>resultados nmpa</h1>"                      # le ponemos un titulo que se vea en la propia pagina web
echo "        <p1>aqui van los resultados de nmap</p1>"      # le ponemos un texto
echo "    <body>"                                            # cerramos el body
echo "</html>"                                               # cerramos nuestro tag principal html

replace string """""" with """"""": para reemplazar o quitar los textos que queramos   

echo "<html>                                                
          <head>                                           
              <title>$TITULO</title>               
          </head>                                           
          <body>                                           
              <h1>$TITULO</h1>                       
              <p1>TIMESTAMP</p1>     
          <body>                                            
      </html>"                                              

COMANDOS

- emacs -nw nmap-parser.sh: este va a ser un programa 

VARIABLES

variable1="valor de prueba": para definir una variable
$variable1: para referenciarlo
var=$((4 * 5)): para asignarles un valor aritmetico
a=78
b="hola"
mv "$nombre_fichero" "${nombre_fichero}.mew": para cambiarle el nombre al fichero

CONSTANTES

es una variable que no se debe modificar su valor 

COMANDO 

- declare: el comando declare (typeset en ksh), es un comando incorporado en en el conjunto de herramientas de GNU Bash, técnicamente denominado built in. Al igual que en lenguajes como C, este builtin nos permite declarar variables definiendo su tipo de datos y haciendo de éste, un tipo inmutable.
- date: El comando date es un comando existente en sistemas Unix y tipo unix que muestra la hora y la fecha del sistema y el administrador también puede cambiarla.

HERE DOCUMENTS

 cat << EOF                      # nos saca el texto que escribamos por pantalla
 > esto es la primera linea
 > esto es la segunda linea
 > $USER
 > EOF

 emacs -ns script_ftp.sh

 #!/bin/bash

 ftp -n <<EOF                    # abre la conexion y se conecta a la maquina virtual tambien intenta autenticarse con el usuario

 open 0.0.0.0
 user santi

 EOF

 cat <<EOF
      
 <html>                                                
    <head>                                           
        <title>$TITULO</title>               
    </head>                                           
    <body>                                           
        <h1>$TITULO</h1>                       
        <p1>TIMESTAMP</p1>     
    <body>                                            
</html>

 EOF

FUNNCIONES

una funcion es una estructura que nos permite organizar el codigo de un programa en diferentes fragmentos que tienen una funcionalidad comun

- return: indica que se va a devolver la ejecucion al punto del programa que se invoco la funcion

declare -r TITULO="resultados nmap"                                     
FECHA_ACTUAL="$(date)"                                                  
TIMESTAMP="Informe generado el $FECHA_ACTUAL por el usuario $USERNAME  

# una funcion que nos saca por pantalla 1 mensaje, ejecuta el comando nmap sobre nuestra subred, saca los resultados al fichero salida_nmap.raw y luego nos saca una cadena de texto
nmap_exec () {                                                            
    echo " [INFO] ejecutando nmap, por favor espere unos segundos..."
    sudo nmap -sV 192.168.239.0/24 > salida_nmap.raw
    echo " [OK] fichero salida_nmap.raw generado correctamente"
}

generar_html () {
cat <<EOF  
<html>                                                
    <head>                                           
        <title>$TITULO</title>               
    </head>                                           
    <body>                                           
        <h1>$TITULO</h1>                       
        <p1>TIMESTAMP</p1>     
    <body>                                            
</html>  
EOF
}

# generamos el reporte raw con nmap
nmap_exec

# generamos el reporte con los resultados de nmap en HTML
echo "[INFO] generando reporte html..."
generar_html > resultados_nmap.html
echo "[OK] reporte resultados_nmap.html generado correctamente"

function mifuncion {
    echo "esta es mi funcion de pruebas"
    return
}

mifuncion2 () {
    echo "esta es mi funcion 2 de pruebas"
    return
}

mifuncion
mifuncion2

PARAMETROS Y ARGUMENTOS

los parametros son variables que se definen en el momento que estamos creando la funcion y que vamos apoder utilizar en el cuerpo de la funcion estas variables recibiran un valor cuando el usuario invoque la funcion y le proporciana esos valores, esos valores que se le proporcionan a la funcion suelen llamarse argumentos

los argumentos los da con con $1 $2

TITULO="resultados nmap"                                     
FECHA_ACTUAL="$(date)"                                                  
TIMESTAMP="Informe generado el $FECHA_ACTUAL por el usuario $USERNAME  

nmap_exec () {                                                            
    echo " [INFO] ejecutando nmap, por favor espere unos segundos..."
    sudo nmap -sV $1 > $2
    echo " [OK] fichero salida_nmap.raw generado correctamente"
}

generar_html () {
cat <<EOF  
<html>                                                
    <head>                                           
        <title>$TITULO</title>               
    </head>                                           
    <body>                                           
        <h1>$TITULO</h1>                       
        <p1>TIMESTAMP</p1>     
    <body>                                            
</html>  
EOF
}

nmap_exec () {                                                            
    echo " [INFO] ejecutando nmap, por favor espere unos segundos..."
    sudo nmap -sV $1 > $2
    echo " [OK] fichero salida_nmap.raw generado correctamente"
}

nmap_exec "192.168.239.0/24" "salida_nmap".raw

echo "[INFO] generando reporte html..."
generar_html > resultados_nmap.html
echo "[OK] reporte resultados_nmap.html generado correctamente"

VARIABLES LOCALES

variables que se definen dentro del cuerpo de una funcion en concreto

variable1="esta variable se encuentra fuera de la funcion"               # no se vera afectado el valor con la variable local pese a que tengan el mismo nombre

test_func () {
    local variable1="esta variable se encuentra dentro de la funcion"
    return
}

test_func

echo $variable1

CONTROL DE FLUJO

estructrua condicional if: nos permite controlar el flujo de ejecucion en base a una condicion que la shell evaluara como verdadera o falsa

{(emacs -nw if_test.sh})
#!/bin/bash

if true; then
    echo " qui va el codigo que se ejecuta cuando la expresion es true"
else 
    echo "aqui va el codigo que se ejecutara cuando la expresion es false"
fi

# para ejecutarlo
./if_test.

- test: El comando test permite efectuar una serie de pruebas sobre los archivos, las cadenas de caracteres, los valores aritméticos y el entorno de usuario. nos permite indicarle como argumento una expresion en la que podemos comparar diferentes tipos de datos y en funcion de esa comparacion nos va a devolver un 0(true) o 1(false)
 se puede referenciar tambien con [ expresion ]
 -le: significa si es menor o igual al valor dado despues

# para comparar cadenas de texto si es true 
 variable1="cadenatexto"

if [ $variable1 = "cadenatexto" ]; then
    echo " qui va el codigo que se ejecuta cuando la expresion es true"
else 
    echo "aqui va el codigo que se ejecutara cuando la expresion es false"
fi

# para comparar los numeros si es true 
 variable1=10

if [ $variable1 -le 10 ]; then
    echo " qui va el codigo que se ejecuta cuando la expresion es true"
else 
    echo "aqui va el codigo que se ejecutara cuando la expresion es false"
fi

if [ "cadena1" = "cadena" ]; then
    echo " qui va el codigo que se ejecuta cuando la expresion es true"
elif [ 5 -le 10 ]; then
    echo "esto seria la segunda condicion de la estructura"   
else 
    echo "aqui va el codigo que se ejecutara cuando la expresion es false"
fi

TITULO="resultados nmap"                                     
FECHA_ACTUAL="$(date)"                                                  
TIMESTAMP="Informe generado el $FECHA_ACTUAL por el usuario $USERNAME  

nmap_exec () {                                                            
    echo " [INFO] ejecutando nmap, por favor espere unos segundos..."
    sudo nmap -sV $1 > $2
    echo " [OK] fichero salida_nmap.raw generado correctamente"
}

generar_html () {
cat <<EOF  
<html>                                                
    <head>                                           
        <title>$TITULO</title>               
    </head>                                           
    <body>                                           
        <h1>$TITULO</h1>                       
        <p1>TIMESTAMP</p1>     
    <body>                                            
</html>  
EOF
}

nmap_exec () {                                                            
    echo " [INFO] ejecutando nmap, por favor espere unos segundos..."
    sudo nmap -sV $1 > $2
    echo " [OK] fichero salida_nmap.raw generado correctamente"
}

nmap_exec "192.168.239.0/24" "salida_nmap".raw

echo "[INFO] generando reporte html..."
generar_html > resultados_nmap.html
echo "[OK] reporte resultados_nmap.html generado correctamente"

# condicion quiero que se genere si el fichero no existe en mi directorio actual y ademas si existe tiene que tener una antoguedad menor a 30 mn si existe hace mas de 30 mn quiero que lo vuelva a generar


TITULO="resultados nmap"                                     
FECHA_ACTUAL="$(date)"                                                  
TIMESTAMP="Informe generado el $FECHA_ACTUAL por el usuario $USERNAME  

nmap_exec () {                                                            
    echo " [INFO] ejecutando nmap, por favor espere unos segundos..."
    sudo nmap -sV $1 > $2
    echo " [OK] fichero salida_nmap.raw generado correctamente"
}

generar_html () {
cat <<EOF  
<html>                                                
    <head>                                           
        <title>$TITULO</title>               
    </head>                                           
    <body>                                           
        <h1>$TITULO</h1>                       
        <p1>TIMESTAMP</p1>     
    <body>                                            
</html>  
EOF
}

nmap_exec () {                                                            
    echo " [INFO] ejecutando nmap, por favor espere unos segundos..."
    sudo nmap -sV $1 > $2
    echo " [OK] fichero salida_nmap.raw generado correctamente"
}

if [ $(find salida_nmap.raw -mmin 30) ]; then
    echo "[INFO] El fichero existe y tiene una antiguedad menor a 30 minutos" 
else
     nmap_exec "192.168.239.0/24" "salida_nmap".raw
fi     

echo "[INFO] generando reporte html..."
generar_html > resultados_nmap.html
echo "[OK] reporte resultados_nmap.html generado correctamente"

Expresiones utilizadas para evaluar condiciones con números:

                  Expresión                                    Verdadero si...

integer1 -eq integer2     →     integer1 es igual a integer2

integer1 -ne integer2     →     integer1 no es igual a integer2

integer1 -le integer2     →     integer1 es menor que o igual a integer2

integer1 -lt integer2     →     integer1 es menor que integer2

integer1 -ge integer2     →     integer1 es mayor que o igual a integer2

integer1 -gt integer2     →     integer1 es mayor que integer2



Expresiones utilizadas para evaluar condiciones con strings:

           Expresión                                    Verdadero si...

string                                →     string no es null.

-n string                         →     La longitud de string es mayor a cero

-z string                         →     La longitud del string es cero

string1 = string2       →     string1 y string2 son iguales

string1 == string2     →     string1 y string2 son iguales

string1 != string2     →     string1 y string2 no son iguales



Expresiones utilizadas para evaluar condiciones con ficheros:

                  Expresión                                    Verdadero si...

file1 -ef file2      →     file1 y file2 tienen el mismo número de inodo (mismo hard link)

file1 -nt file2      →     file1 is mas nuevo que file2

file1 -ot file2      →     file1 is mas antiguo que file2

-b file                        →     file existe y es un block-special (device) file

-c file                        →     file existe y es un character-special (device) file

-d file                        →    file existe y es un directorio

-e file                        →     file existe

-f file                        →     file existe y es un fichero regular

-k file                        →    file existe y tiene “sticky bit”

-L file                        →    file existe y es un enlace simbólico

-s file                        →    file existe y tiene longitud mayor a cero

-u file                        →     file existe y es setuid

-w file                        →    file existe y se puede escribir (por el usuario efectivo)

-x file                        →    file existe y es ejecutable (por el usuario efectivo)

CONDICIONES AVANZADAS

[[  ]]: unicamente funciona en versiones modernas de bash, el funcionamiento es el mismo de tes pero dentro de la expresion podemos utilizar expresiones regulares y wildcards
[[ "fichero1" =~ 1$ ]]: esta expresion regular consistiria en que todo aquel texto que termine en 1

variable="fichero.log"
[[ $variable == *.log ]]

variable="fichero.txt"
[[ $variable == *.txt ]]

if [[ $variable == *.log ]]; then echo "verdadero"; else echo "falso"; fi

(()): nos permite evaluar expresiones 
(()): utilizamos los mismos simbolos que en los corchetes
((5 < 8))

EXPRESIONES AND,OR Y NOT

-a= and
[ 4 -lt 10 -a "texto" = "texto" ]
&&: and pero se pone entre 4 corchetes
[[ 4 -lt 10 && "texto" = "texto" ]]
-lt= es igual a

-o= or decimos si una expresion es verdadera sin importar si la otra es falsa aparecera un true
[ 4 -lt 10 -o "texto" = "texto" ]
||: or pero se pone entr 4 corchetes
[ 4 -lt 10 || "texto" = "texto" ]

!= not negacion
[ ! 4 -lt 10 ]
!= not es igual para los 4 corchetes
[ ! 4 -lt 10 ]

COMANDO EXIT

exit tambien nos permite devolver un valor numerico al igual que return en ocasiones en lugar de poner return utilizan exit la diferencia es que con exit terminamos la ejecucion del progama y no ejecuta el resto de lineas

BUCLE FOR

los bucles nos permiten repetir la ejecucion de un fragmento de codigo concreto de nuestro programa 

# para crear un fichero
emacs -nw fortest.sh
#!/bin/bash

# crear un bucle que se repita 4 veces
for i in 1 2 3 4; do 
    echo "esta es la iteracion $i"
done

# crear un bucle que se repita 20 veces
for i in {1..20}; do 
    echo "esta es la iteracion $i"
done

# crear un bucle que se repita * pero con un caracter como valor
for i in {a..z}; do
    echo "esta es la iteracion $i"
done

# bucle sobre ficheros
for i in /var/log*.log; do
    echo "esta iteracion actuara sobre el fichero: $i"
done

# un bucle con shell expansions
for i in $(find /usr/bin -name '*zip'); do
    echo "esta iteracion actuara sobre el fichero: $i"
done    
# bucle en lenguaje de programacion c
i=0 le podemos asignar un valor numerico


for ((i=0; i<5; i=i+1)); do
    echo "esta es la iteracion: $i"
done

COMANDO

- split: nos permite dividir un fichero en diferentes secciones en base a un patron. El comando split sirve para dividir un archivo grande en varios archivos pequeños. Podemos realizar esa división por número de líneas, por tamaño u otras opciones.
split salida_nmap.raw
si escribimos una expresion regular tiene que ser entre estas barrras
csplit salida_nmap.rae '/^$/' {*}