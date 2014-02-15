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
