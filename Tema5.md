# Ejercicios tema 5
## Ejercicio 1

Instalar los paquetes necesarios para usar KVM. Se pueden seguir estas instrucciones. Ya lo hicimos en el primer tema, pero volver a comprobar si nuestro sistema está preparado para ejecutarlo o hay que conformarse con la paravirtualización.

![](https://raw.github.com/elmendacorp/IVTAREAS/master/img/kvmfunciona.png)

## Ejercicio 2
Crear varias máquinas virtuales con algún sistema operativo libre, Linux o BSD. Si se quieren distribuciones que ocupen poco espacio con el objetivo principalmente de hacer pruebas se puede usar CoreOS (que sirve como soporte para Docker) GALPon Minino, hecha en Galicia para el mundo, Damn Small Linux, SliTaz (que cabe en 35 megas) y ttylinux (basado en línea de órdenes solo).

![](https://raw.github.com/elmendacorp/IVTAREAS/master/img/qemufunciona.png)

Instalo COREOS siguiendo el manual para qemu, pero a la hora de entrar con ssh, tras generar el fichero de acceso y cargarlo el sistema no me deja loguearme.

Hacer un ejercicio equivalente usando otro hipervisor como Xen, VirtualBox o Parallels.
## Ejercicio 3
Crear un benchmark de velocidad de entrada salida y comprobar la diferencia entre usar paravirtualización y arrancar la máquina virtual simplemente con

`qemu-system-x86_64 -hda /media/Backup/Isos/discovirtual.img`

## Ejercicio 4
Crear una máquina virtual Linux con 512 megas de RAM y entorno gráfico LXDE a la que se pueda acceder mediante VNC y ssh.

##Ejercicio 5
