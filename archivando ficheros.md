COMANDOS 

- tar: El comando TAR es usado para empaquetar un archivo o directorio.15
- tar -cf ficheros.tar ./fichero*: archiva todos los ficheros que uno le indique en uno solo
- tar -xvf ficheo.tar: para desarchivar los ficheros que estaban en uno solo
- tar -czf ficheros.tar.gz ./fichero*: para comprimirlos en un solo fichero con gzip
- tar -cjf ficheros.tar.bz2 ./fichero*: para comprimirlos con bzip2
- zip: En linux existe tambien el comando zip para comprimir y empaquetar y el unzip para sacar los archivos, el alumno puede referirse a 'man zip', aqui veremos un ejemplo con los comandos anteriores por ser lo típico en entronos Unix.
  {(zip fichero1.zip fichero1.txt)} {(zip syslog.zip syslog2)}
- zip -r testdir2.zop testdir2: de comprimir y archivar un directorio
- unzip: para descomprimir
  