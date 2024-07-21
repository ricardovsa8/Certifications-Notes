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

