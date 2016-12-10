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

