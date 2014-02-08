[TOC]

## Ejercicio 1:

Procedemos a instalar lxc.
`sudo apt-get install lxc`

![foto](https://github.com/elmendacorp/IVTAREAS/raw/master/img/lxc.png)

## Ejercicio 2
Comprobar qué interfaces puente se han creado y explicarlos.
![foto](https://github.com/elmendacorp/IVTAREAS/raw/master/img/lxc.png)

## Ejercicio 3

Crear y ejecutar un contenedor basado en Debian.
![foto](https://github.com/elmendacorp/IVTAREAS/raw/master/img/maquinalxc.png)

## Ejercicio 4
Instalar lxc-webpanel y usarlo para arrancar, parar y visualizar las máquinas virtuales que se tengan instaladas.
![foto](https://github.com/elmendacorp/IVTAREAS/raw/master/img/lxcweb.png)

## Ejercicio 6
Instalar juju.
`sudo apt-get install juju juju-core juju-local`

Usándolo, instalar MySQL en un táper.
```
juju switch local
sudo juju bootstrap
juju deploy mysql
juju expose mysql

```
## Ejercicio 7
Destruir toda la configuración creada anteriormente
`sudo juju destoy-enviroment`
Volver a crear la máquina anterior y añadirle mediawiki y una relación entre ellos.
```
sudo juju bootstrap
juju deploy --to 1 mysql
juju deploy --to 1 mediawiki
juju explose mysql
juju expose mediawiki
```
Crear un script en shell para reproducir la configuración usada en las máquinas que hagan falta.

## Ejercicio 8
Instalar libvirt
`sudo apt-get install libvirt-bin`

## Ejercicio 10
Instalar docker.

```
sudo apt-get update
sudo apt-get install linux-image-extra-`uname -r`
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 36A1D7869245C8950F966E92D8576A8BA88D21E9
sudo sh -c "echo deb http://get.docker.io/ubuntu docker main\
> /etc/apt/sources.list.d/docker.list"
sudo apt-get update
sudo apt-get install lxc-docker
```
## Ejercicio 11
Instalar a partir de docker una imagen alternativa de Ubuntu y alguna adicional, por ejemplo de CentOS.
`sudo docker pull centos`