# Ejercicios tema 6

## Ejercicio 1
Instalar chef en la máquina virtual que vayamos a usar
```
sudo apt-get install ruby1.9.1 ruby1.9.1-dev rubygems
sudo gem install ohai chef
```
## Ejercicio 2
Crear una receta para instalar nginx, tu editor favorito y algún directorio y fichero que uses de forma habitual.
```
package 'nginx'
package 'nano'
directory '$home/carpeta'
file "$home/carpeta/archivo" do
	owner "fran"
	group "fran"
	mode 00544
	action :create
	content "Direcctorio creado desde chef"
end
```

## Ejercicio 3
Escribir en YAML la siguiente estructura de datos en JSON.
```
tres:
    - 4
    - 5
    - "Seis"
    -
      siete: 8
      nueve:
        - "Object"
  uno: "dos"
```

## Ejercicio 6
Instalar una máquina virtual Debian usando Vagrant y conectar con ella.
Instalamos un box de debian:
`vagrant box add Debian https://dl.dropboxusercontent.com/s/xymcvez85i29lym/vagrant-debian-wheezy64.box`

```
vagrant up
vagrant ssh
```
Eso inicia y nos da acceso a la maquina que hemos instalado con vagrant.

## Ejercicio 7

Crear un script para provisionar `nginx` o cualquier otro servidor web que pueda ser útil para alguna otra práctica.

```
hosts: localhost
  sudo: yes
  tasks:
    - name: Update mc
      apt: pkg=nginx state=present
```
## Ejercicio 8
Configurar tu máquina virtual usando vagrant con el provisionador ansible.

```
  hosts: localhost
  sudo: yes
  tasks:
     name: Install nginx
     apt: pkg=nginx state=present
     name: Start nginx
     command: sudo service nginx start
```
