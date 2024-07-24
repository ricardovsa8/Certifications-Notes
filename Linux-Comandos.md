===========================================
Comandos Linux
===========================================
Prompt= sysadmin@localhost:~$

Sysadmin = nombre del usuario registrado

localhost = nombre del sistema

~ = direcctorio actual

-----
Shell = es el intérprete que traduce los comandos introducidos por un usuario en acciones a realizar por el sistema operativo.

-----
Formato de un comando

comando [opciones] [argumentos]

-----
Listar archivos y direcctorios

$ ls

------
Listar archivos con detalles

$ ls -l

------
Listar archivos mostrando el tamaño de los archivos

$ ls -l -h   
$ ls -lh

------
Ver fecha

$ date

------
Ver historial de consultas

$ history

------
Muestra los ultimos 5 comando de la lista del historial

$ history 5

------
Ejecuta el ultimo comando otra vez

!!

------
Ejecuta el quinto comando desde la parte inferior de la lista de historial

!-5

------
Ejecuta el comando ls más reciente

!ls

------
Declarar variable y mostrar

$ VARIABLE=499999
$ echo #VARIABLE

-----
Crear una variable local

$ variable1='Something'

-----
Buscar una variable de entorno

$ env | grep variable1 

-----
Exportar una varible local a una variable de entorno

$ export variable1

-----
Crear una variable de entorno

$ export variable2='Else'

-----
Eliminar una variable exportada

$ unset variable2

-----
Buscar la ubicación de un comando en la variable PATH

$ which date

----
Determinar información acerca de un comando

sysadmin@localhost:~$ type which                                       
which is hashed (/usr/bin/which)

-----
mostrará todos los archivos que contienen al menos un número:

$ echo /etc/*[0-9]*

-----
mostrará todos los archivos que comiencen con cualquier letra entre e incluyendo a y d

$ echo /etc/[a-d]*

-----
imprimirá cualquier archivo que comienza con el carácter g o u y contiene cero o más caracteres adicionales

$ echo /etc/[gu]*   

-----
mostrará cualquier archivo que no comienza con D o P

$echo [!DP]*

-----
Traer la fecha de hoy

$ echo Today is `date`

-----
imprimir los meses de enero, febrero y marzo de 2015,

$ cal 1 2015; cal 2 2015; cal 3 2015

-----
Obtener información del sistema actual

$ uname

-----
mostrará el nombre del host del nodo de la red

$ uname --nodename

-----
Mostrar ubicación actual

$ pwd

-----
mostrarán todos los archivos en el directorio actual que comienzan con la letra D y la letra P

$ echo P*
$ echo D*

-----
mostrará todos los archivos en tu directorio actual que terminan en la letra s

$ echo *s

-----
UNIX es un sistema operativo desde el cual se construyo la base de Linux.

Las PAGINAS MAN, son documentos de ayuda

-----
Mostrar la pagina Man del comando cal

$ man cal

-----	
Comandos que existen

- Comando de usuario
- Comando del sistema
- Comando de administración

-----
Ver las paginas en la se encuentra un comando (Opción 1)

$ man -f passwd

-----
Ver las paginas en la se encuentra un comando (Opción 2)

$ whatis passwd

-----
Buscar paginas man por una palabra clave (Opción 1)

$ man -k passwd

-----
Buscar paginas man por una palabra clave (Opción 2)

$ apropos passwd

-----
Obtener información de un comando

$ info ls

-----
Otras forma de ayuda

$ ls --help

-----
Ver la ubicación de un comando

$ whereis ls

-----
Encontrar cualquier archivo o directorio

$ locate gshadow

-----
Actualizar manualmente la base de datos locate

$ updatedb

------
Contar los numero de archivos

$ locate -c passwd

-----
Limitar la salida

$ locate -b "\passwd"

-----
Para ver el sistema de archivos raiz

$ ls /

------
Rutas

usr
Share
gnome, doc, sounds

-----
Ver direcctorio actual

$ pwd

-----
Una ruta de acceso relativa proporciona direcciones usando tu ubicación actual como un punto de referencia. 
Recuerda que esto es diferente de las rutas absolutas, que siempre requieren que utilices el directorio raíz como punto de referencia.

------
Lista de archivos

$ ls

-----
Mostrar lista de archivos, incluyendo archivos ocultos

$ ls -a

-----
Detalles de un archivo

$ ls -l

-----
Tipo de archivo
Permisos
Conteo de enlaces fisicos
Usuario propietario
Grupo propietario
Tamaño de archivo
Hora de modificacion
Nombre de archivo o directorio

-----
Saber el tamaño de archivo en megabytes o gigabytes

$ ls -lh /usr/bin/omshell

-----
Saber el direcctorio actual

$ ls -d
$ ls -ld

-----
Listar de manera recursiva

$ ls -R /etc/ppp

-----
Ordenar archivos por tamaño

$ ls -S /etc/ssh

-----
Ordenar archivos por momento que se modificaron

$ ls -t

------
Orbtener información detalla de la hora

$ ls -t --full-time /etc/ssh

-----
Ordenar de manera menor a mayor

$ ls -lrS /etc/ssh

------
Ordenar de manera mayor a menos

$ ls -lrt /etc/ssh

-----
Copiar archivos

$ cp fuente destino

-----
Mover archivos

$ mv fuente destino

------
-i	Movimiento interactivo: pregunta si un archivo debe sobrescribirse.
-n	No sobrescribir el contenido de los archivos de destino
-v	Verbose: muestra el movimiento resultante

-----
Crear un archivo vacion

$ touch ejemplo

-----
Elminar un archivo

$ rm ejemplo

-----
Para eliminar varios archivos es recomendable usar -i

$ rm -i *.txt

-----
Elminar un directorio

$ rm -r ejemplo

-----
Elminar u directorio vacio

$ rmdir ejemplo

------
Crear un directorio

$ mkdir ejemplo

-----
gzip y gunzip. Éstos son el bzip2 y bunzip2. Las utilidades del bzip utilizan un algoritmo de compresión diferente 
(llamado bloque de clasificación de Burrows-Wheeler frente a la codificación Lempel-Ziv que utiliza gzip) 
que puede comprimir los archivos más pequeños que un gzip a costa de más tiempo de CPU

-----
comando tar para crear un archivo empaquetado del directorio /etc/udev. Guardar la copia de seguridad en el directorio ~/mybackups

cd
mkdir mybackups
tar –cvf mybackups/udev.tar /etc/udev
ls mybackups

La opción -c le indica al comando tar que cree un archivo tar. La opción -v significa "verbose", que le indica al comando tar para muestre lo que está haciendo. La opción -f se utiliza para especificar el nombre del archivo tar.

-----
Muestra el contenido del archivo tar (t = lista el contenido, v = verbose, f =nombre del archivo):

tar –tvf mybackups/udev.tar

-----
Para crear un archivo tar comprimido, utiliza la opción -z

tar –zcvf mybackups/udev.tar.gz /etc/udev
ls –lh mybackups

Observa la diferencia de tamaño; la primera copia de seguridad (10 Kbytes) es mayor que la segunda copia de seguridad (1.2 Kbytes).

La opción -z hace uso de la utilidad gzip para realizar la compresión.

-----
Extraer el contenido de un archivo. Los datos se restauran en el directorio actual por defecto:

tar –xvf udev.tar.gz

-----
Para añadir un archivo a un archivo empaquetado existente, utiliza la opción -r con el comando tar. Ejecuta los siguientes comandos para realizar esta acción y comprobar la existencia del archivo nuevo en el archivo empaquetado tar:

tar -rvf udev.tar /etc/hosts
tar –tvf udev.tar

-----
gzip y gunzip para comprimir y descomprimir un archivo

gzip words

-----
descomprimir el archivo words.gz

gunzip words.gz

-----
Populares

bzip2/bunzip2
.bz2
-----
Comprime el directorio /etc/udev y su contenido con el comando de compresión zip

zip -r udev.zip /etc/udev
ls -l udev.zip

-----
Para ver el contenido de un archivo zip, utiliza la opción -l con el comando unzip

unzip -l udev.zip

-----
Para extraer el archivo zip, utiliza el comando unzip sin ninguna opción

unzip udev.zip

-----
El carácter barra vertical puede utilizarse para enviar la salida de un comando a otro.

-----
Mostrar las 10 primeras lineas

$ head /etc/sysctl.conf

-----
Mostrar las 10 ultimas lineas

$ tail /etc/sysctl.conf

-----
Ver algunos archivos del directorio

$ ls /etc | head

-----
Comando para enumeras datos obtenidos

$ ls -l /etc/ppp | nl

----
Mostrar los ultimos 5 lineas de salida

$ ls -l /etc/ppp | n1 |  tail -5

--ado ---
STDIN es la información normalmente introducida por el usuario mediante el teclado.

-----
STDOUT es la información que muestra cuando se ejecuta un comando.

-----
STDERR son mensajes de error que muestra en pantalla cuando se ejecuta un comando.

-----
Redirigir un STDOUT a un archivo txt

$ echo "line 1" > ejemplo.txt

-----
Para agregrar otro resultado al archivo tct

$ echo "nota 2" >> ejemplo.txt

------
Ver el archivo txt

$ cat archivo.txt

------
Guardar en un archivo resultado STDOUT y STDERR

$ ls /fake /etc/ppp > example.txt 2> error.txt

-----
La sintaxis del comando find es:

find [directorio de inicio] [opción de búsqueda] [criterio de búsqueda] [opción de resultado]

-----
Buscar y dirigir los resultados a un archivos txt

$ find /etc -name hosts 2> errors.txt 

-----
Donde se envia los archivos innecesarios

$ find /etc -name hosts 2> /dev/null

-----
Buscar archivos por tamaño

$ find /etc -size 10c -ls 2>/dev/null 

------
Buscar archivos que sea mayor a 100 megabytes

$ find /usr -size +100M -ls 2> /dev/null

-----
Buscar archivos que sea menor a 100 megabytes

$ find /usr -size -100M -ls 2> /dev/null

-----
Muestra todos los archivos en la estructura de directorio /etc con el tamaño de 10 bytes y que son archivos simples:

$ find /etc -size 10c -type f -ls 2>/dev/null

------
muestra la línea #22 hasta el final de la salida del comando nl

$ nl /etc/passwd | tail -n +22

------
Ordenar datos de un archivo

$ sort mypasswd

------
Ver estadisticar de un archivo

$ wc /etc/passwd /etc/passwd-

-l para mostrar sólo el número de líneas
-w para mostrar sólo el número de palabras
-c para mostrar sólo el número de bytes.
------
Utilizar el Comando cut para Filtrar el Contenido del Archivo

$ cut -d: -f1,5-7 mypasswd

-----
tilizar el comando grep para filtrar las líneas del archivo /etc/passwd para las líneas que contengan los caracteres bash

grep --color bash /etc/passwd 

-----
más bien cuántas líneas coinciden con el patrón

$ grep -c bash /etc/passwd 

-----
Opción -n del comando grep muestra los números de la línea originales

$ grep -n bash /etc/passwd

-----
Todas las líneas que no contengan nologin en el archivo /etc/passwd

grep -v nologin /etc/passwd

-----
Lista de los archivos en el directorio /etc que contengan linux

grep -l linux /etc/*

-----
Listado de las líneas de los archivos en el directorio /etc que contengan cualquier tipo de letra (mayúscula o minúscula) del patrón de caracteres linux

grep -i linux /etc/*

-----
Listado de las líneas de los archivos en el directorio /etc que contengan el patrón de la palabra linux

grep -w linux /etc/*

-----
Buscar tres letras en archivo txt

$ gred --color 'a..' ejemplo.txt

-----
Para el inicio

$ grep --color "^a" example.txt

------
Para el final

$ grep "c$" example.txt  

------
Buscar un caracter especial (colocar antes el \)

$ grep --color "cd\*" example.txt

-----
Editores

nano - es un editor para pequeños archivos
vi , vim - un editor muy potente

-----
Ejemplo de la condicion if

if somecommand; then
  # do this if somecommand has an exit code of 0
fi

-----
Comando test como alternativa de if

test –f /dev/ttyS0	0 si el archivo existe
test ! –f /dev/ttyS0	0 si el archivo no existe
test –d /tmp	0 si el directorio existe
test –x `which ls`	sustituir la ubicación de ls y luego (probar) test, si el usuario puede ejecutar
test 1 –eq 1	0 si tiene éxito la comparación numérica
test ! 1 –eq 1	NO – 0 si la comparación falla
test 1 –ne 1	Más fácil, ejecutar test (probar) si hay desigualdad numérica
test “a” = “a”	0 si tiene éxito la comparación de cadenas
test “a” != “a”	0 si las cadenas son diferentes
test 1 –eq 1 –o 2 –eq 2	-o es OR: cualquiera de las opciones pueden ser igual
test 1 –eq 1 –a 2 –eq 2 es AND: ambas comparaciones deben ser iguales


-----
La instrucción if tiene una forma final que te permite hacer varias comparaciones al mismo tiempo usando elif (abreviatura de elseif).

#!/bin/bash

if [ "$1" = "hello" ]; then
  echo "hello yourself"
elif [ "$1" = "goodbye" ]; then
  echo "nice to have met you"
  echo "I hope to see you again"
else
  echo "I didn't understand that"
fi

------
el loop for y el loop while

#!/bin/bash

SERVERS="servera serverb serverc"
for S in $SERVERS; do
  echo "Doing something to $S"
done

---

#!/bin/bash

i=0
while [ $i -lt 10 ]; do
  echo $i
  i=$(( $i + 1))
done
echo "Done counting"

-----
Para ver a que familia pertenece tu CPU (Opcion 1)

$ arch

-----
Para ver a que familia pertenece tu CPU (Opcion 2)

$ lscpu

-----
Para ver a que familia pertenece tu CPU (Opcion 3) más detallada

$ car /proc/cpuinfo

-----
Mostar informacipión de SMBIOS

$ dmidecode

-----
Ver la cantidad de RAM fisica y RAM virtual

$ free -m

-----
Ver todos los dispositivos conectados por un bus PCI

$ lspci

-----
Ver dispositivos de Bus Serie Universal USB

$ lsusb

-----
Ver dispositios conectados

$ lshal

-----
Ver los modulos cargados actualmente

$ lsmod

-----
Ver los discos

$ fdisk -l

-----
