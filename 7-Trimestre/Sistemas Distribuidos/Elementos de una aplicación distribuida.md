8 de Octubre 2025

<mark style="background: #ADCCFFA6;">Localización</mark>    <mark style="background: #ADCCFFA6;">Designación</mark>   <mark style="background: #ADCCFFA6;">Comunicación</mark> 

<mark style="background: #FF5582A6;">Tolerancia a fallas</mark> <mark style="background: #FF5582A6;">Escalabilidad</mark> <mark style="background: #FF5582A6;">Transparencia Balance de carga </mark>

Las de color <mark style="background: #ADCCFFA6;">azul</mark> son las cosas que una aplicación  distribuido debe tener, las rojas cosas que son indispensables para tener una aplicación distribuida .

## Como mínimo debe tener 

**Designación**:Ponerle un nombre a los recursos involucrados para poder utilizarlos.(Nombrar a lo que van a tener acceso a los usuarios)

**Localización**:Esquema para saber la ubicación de los recursos para poder utilizarlos.

**Comunicación y distribución**

***Ejemplos***

- El sistema de **DNS** (Domain Name System) y las  **URL** (Uniform Resource Localicaion): Acceder a las computadores alrededor del mundo.



**DNS**
www.google.com -> IP:XXX.XX.XX.X

<mark style="background: #BBFABBA6;">URL->IP</mark>

**URL**

/home/alumnos/tarea.txt -> IP:XXX.XXX.XX.X

<mark style="background: #BBFABBA6;">Ruta-> IP</mark>

#  Como funciona el NFS

Pasos para montar un directorio en un servidor NFS

- Instalar el cliente NFS en ubuntu : sudo apt-get intall nfs-common portmap
- Crear un directorio en su maquina: mkdir /home/[usuario]/cloud
- Montar el directorio remoto en el directorio local.
- sudo mount -t nfs IP:home/antonio/distribuidos ~/cloud

