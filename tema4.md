## Ejercicio 1
Tengo instalado un sistema de dos particiones primarias y una lógica, orientada al almacenamiento de datos, las particiones primarias a un sistema operativo.
Los sistemas de la escuela se basan en discos en red, de los que supongo serán discos virtuales.
Entre las paginas que ofrecen servicio de almacenamiento he optado por mega y drive, ambos permiten la sincronizacion de directorio.
Mega: 
500GB 12TB transferencia 99,99 euros anuales
2TB 48TB transferencia 199,99 euros anuales
4TB 96TB transferencia 299,99 euros anuales
Drive:
100GB 4,99 dolares mes
200GB 9,99 dolares mes
400GB 19,99 dolares mes
1TB 49,99 dolares mes
2TB 99,99 dolares mes
4TB 199,99 dolares mes
8TB 399,99 dolares mes
16TB 799,99 dolares mes

##Ejercicio 3
Crear imágenes con estos formatos (y otros que se encuentren tales como VMDK) y manipularlas a base de montarlas o con cualquier otra utilidad que se encuentre

`dd of=fichero-suelto.img bs=1k seek=5242879 count=0`

`sudo mkdir /mnt/mountpoint`

`mount -o loop,offset=32256 /camino/a/fichero-suelto.img /mnt/mountpoint`

##Ejercicio 4
Crear uno o varios sistema de ficheros en bucle usando un formato que no sea habitual (xfs o btrfs) y comparar las prestaciones de entrada/salida entre sí y entre ellos y el sistema de ficheros en el que se encuentra, para comprobar el overhead que se añade mediante este sistema

`sudo losetup -v -f fichero-suelto.img`

![](https://raw.github.com/elmendacorp/IVTAREAS/master/img/montajeunidad.png)
![](https://raw.github.com/elmendacorp/IVTAREAS/master/img/prueba1.png)

## Ejercicio 5
Instalar ceph en tu sistema operativo.

`sudo apt-get install ceph-mds`

`sudo mkdir -p /srv/ceph/{osd,mon,mds}`

Configuramos el fichero cambiando el nombre de la maquina local y si queremos el del puerto.

`sudo mkdir /srv/ceph/osd/osd.0`

`sudo /sbin/mkcephfs -a -c /etc/ceph/ceph.conf`

`sudo /etc/init.d/ceph -a start`
##Ejercicio 6
Crear un dispositivo ceph usando BTRFS o XFS
![](https://raw.github.com/elmendacorp/IVTAREAS/master/img/cephinstalado.png)

## Ejercicio 7
Almacenar objetos y ver la forma de almacenar directorios completos usando ceph y rados.

## Ejercicio 8
Tras crear la cuenta de Azure, instalar las herramientas de línea de órdenes (Command line interface, cli) del mismo y configurarlas con la cuenta Azure correspondiente
Se hace todo desde windows con un ejecutable de siguiente, siguiente.
COn esto añadimos la cuenta

`azure account download`
## Ejercicio 9


