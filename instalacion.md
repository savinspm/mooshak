### Instalación

La instalación se va a realizar sobre un equipo Ubuntu 14.04.03 LTS. La guía original para este capítulo se puede encontrar en: [http://blankrk.blogspot.com.es/2014/05/mooshak-installation-on-linux-1204-and.html](http://blankrk.blogspot.com.es/2014/05/mooshak-installation-on-linux-1204-and.html)

Bien, comencemos!!

Suponiendo que se empieza con una instalación limpia, el primer paso es actualizar los respositorios y paquetes del equipo. Para ello usamos los siguientes comandos. Puede que en el proceso de actualización nos aparezca si deseamos modificar el grub: dejamos la opción por defecto.

![](/images/actualizacion.png)

`sudo apt-get update`

`sudo apt-get upgrade`

El siguiente paso consiste en instalar el compilar de c y el programa make

`sudo apt-get install tcl xsltproc lpr rsync gcc libxml2-utils`

`sudo apt-get install apache2`

`sudo apt-get install apache2-suexec`

En caso de que no se encuentre el paquete apache2-suexec, se puede instalar el apache2-suexec-custom.

Una vez se ha instalado Apache, es necesario habilitar dos mods:

`sudo a2enmod userdir`

`sudo a2enmod suexec`

Después habilitamos el userdir y el usexec modulos de Apache.

`cd /etc/apache2/mods-enabled`

`sudo ln -s ../mods-available/userdir.conf`

`sudo ln -s ../mods-available/userdir.load`

`sudo ln -s ../mods-available/suexec.load`

Es posible que haya salido el siguiente mensaje:

ln: failed to create symbolic link ‘./suexec.load’: File exists

