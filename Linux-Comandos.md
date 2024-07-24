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
