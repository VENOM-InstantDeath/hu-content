# Bash De 0 a 1000 #3 - OpenSUSE
<b>By: Darth Venom - 11/03/2022</b>
<br>
<br>
En OpenSUSE y los sistemas derivados, el gestor de paquetes es zypper. Zypper es un programa de gestión de paquetes que utiliza la librería libzypp. Este gestor administra paquetes con el formato RPM, al igual que RHEL (Red Hat Enterprise Linux), Fedora y CentOS.
<br>
<center><b><u>Sintaxis</u></b></center>
<br>
zypper [operación] [opciones] [paquete]
<br>
Zypper admite el uso de versiones abreviadas de cada una de las operaciones disponibles del gestor, al final de cada sección se indicará cuál es la versión abreviada de cada operación.
<br>
<center><b><u>Instalar paquetes</u></b></center>
<br>
Para esto se utiliza la operación *install* seguido del nombre del paquete, esto se hace de la siguiente forma:
<br>
<i>zypper <b>install</b> [paquete]</i>
<br>
*[package]* debe ser reemplazado por el nombre del paquete que se desea instalar. Para las instalaciones se requiere que el usuario tenga permisos elevados, por ende, tendrá que preceder zypper con el comando sudo pasando zypper como argumento de sudo. Lo anterior debe ser así:
<br>
*sudo zypper install [paquete]*
<br>
<center>Para instalar paquetes localmente sólo debes poner la ruta del paquete.</center>
<br>
**Ejemplo:** *sudo zypper install [/ruta/hacia/paquete.rpm]*
<br>
Del mismo modo se puede hacer uso del gestor dpkg para la instalación de paquetes locales, para esto se usa:
<br>
*sudo rpm -i [/ruta/hacia/paquete.rpm]*
<br>
La versión abreviada de la operación *'install'* es *'in'*.
<br>
<center><b><u>Actualizar datos sobre los paquetes</u></b></center>
<br>
En OpenSUSE por defecto cada vez que se ejecuta zypper para operaciones de instalación, el gestor actualiza automáticamente la base de datos de los paquetes, aún así como este comportamiento puede ser desactivado para cada repositorio zypper admite la operación refresh para actualizar la base de datos.
<br>
<i>sudo zypper <b>refresh</b></i>
<br>
La versión abreviada de la operación *'refresh'* es *'ref'*.
<br>
<center><b><u>Actualizar paquetes</u></b></center>
<br>
Regularmente se deben actualizar los paquetes, esto es necesario para tener todos los programas en sus versiones más recientes, los últimos parches de seguridad y la última versión del kernel. Esto no sólo es para tener las mejores versiones de los programas, sino para tener un sistema más seguro.
<br>
La operación que se usa para actualizar los paquetes es la siguiente:
<br>
<i>sudo zypper <b>update</b></i>
<br>
A parte de esta operación existe la operación *dist-upgrade* que se utiliza para otro tipo de actualización, se usa para actualizar "en vivo" la distribución a la última versión, es decir, sin necesidad de instalar un disco o una USB. Entre las ventajas de esta operación se encuentra que mientras se realiza la actualización se puede seguir usando el sistema, y únicamente se requerirá un reinicio para cargar el nuevo software. Por otro lado, entre las desventajas si por alguna razón este proceso se interrumpe, ya sea por un corte de luz, falta de batería o pérdida de conexión, podría quedarse con un sistema roto.
<br>
La versión abreviada de la operación *'update'* es *'up'*.
<br>
<center><b><u>Remover paquetes</u></b></center>
<br>
Para remover paquetes existe la operación remove:
<br>
<i>sudo zypper <b>remove</b> [paquete]</i>
<br>
Si se desea simplemente remover un paquete, se usa la operación remove. Si se busca eliminar un paquete y sus dependencias, se usa la opción *--clean-deps* de la operación *remove*. Esta opción sólo eliminará los programas o librerías que sólo sean dependencia del programa que se busca eliminar, sino se mantendrán.
<br>
<i>sudo zypper remove <b>--clean-deps</b> [paquete]</i>
<br>
La versión abreviada de la operación *'remove'* es *'rm'*.
<br>
<center><b><u>Listar paquetes</u></b></center>
<br>
Para listar paquetes se usa la misma operación que para buscarlos, *search*. Si se desean listar todos los paquetes disponibles, se usa:
<br>
<i>zypper <b>search</b></i>
<br>
Si lo que se busca es listar sólo los instalados, se pasa la opción *-i*
<br>
<i>zypper search <b>-i</b></i>
<br>
La versión abreviada de la operación *'search'* es *'se'*.
<br>
<center><b><u>Buscar paquetes</u></b></center>
<br>
Si se quiere buscar un paquete entre la lista de los paquetes disponibles se usa la operación search
<br>
<i>zypper <b>search</b> [paquete]</i>
<br>
La versión abreviada de la operación *'search'* es *'se'*.
<br>
<center><b><u>Información sobre un paquete</u></b></center>
<br>
Para obtener una descripción sobre un paquete se usa *info*.
<br>
<i>zypper <b>info</b> [paquete]</i>
<br>
La versión abreviada de la operación *'info'* es *'if'*.
<br>
<hr>
El blog ha llegado a su fin. Si tienes dudas puedes contactarme en Discord, soy Kiss_Linux#7802.
