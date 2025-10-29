---
Date: 2025-10-29
tags:
  - "#TPC"
  - "#Capa_Internet"
---
---

28 de Octubre 2025

Las **MAC** viven entre la capa física y la de acceso a la red, y el **ARP** esta entre la capa de acceso a la red y la de internet 

Las aplicaciones solicitan servicios a la **Capa de Internet** o se la puede saltar para acceder a la capa de acceso a la red.

# Capa de Internet

Aquí esta el direccionamiento IP, realiza empaquetamiento.

**IP**:Identifica los nodos de la red y los identifica dentro de un grupo esto por el prefijo de red
Prefijo de red: Todos los dígitos son iguales por que son del mismo nodo.
Dirección de host: Él ultimo numero significa que nodo es.

Para mandar información manda un brodcast preguntando cual es su **MAC** esto por que en la trama tenemos el IP después el destinatario y al final quien lo manda.


# Capa de Acceso a  la red
Se utiliza de **ARP** de manera constante en donde guardamos el IP y MAC en una tabla  **tabla ARP** (Address Resolution Protocol).La tabla es dinámica.

Los nodos están conectados y se cierra el switch para que no haya colisiones por medio de  un enrutador.

>[!Note] Switch
>Este trabaja en la  capa dos y sabe cual a cual mandarlo por que tiene tablas de información.Si conmuta entre los host
	
Los conmutadores se pueden aumentar conectándolos en serie.

**Ether_type**:

- long: Cantidad de bytes en la carga útil 46 a 1500
- Protocolos: Números mayores a 8000 están estandarizados

Problemas en la tramas de Ethernet

- Representación de la información.(forma en la que se acomoda).


El preámbulo le dice que va a llegar información y el SDF es donde empieza (/ tiene en donde inicia).

###  RARP
Dada una **MAC** te dice que IP tiene.

MAC ->  IP ?

Este fue sustituido por <mark style="background: #FFB86CA6;">DHCP</mark>

La topología sigue siendo en estrella.

Reenvió: Es pasar las tramas de un Interfaz a otra.
Filtrado: Hacer que sea mas efectivo el mandado de  mensajes.


**Ventajas  del Ethernet**

- No existen colisiones
- Permiten operar a velocidades diferentes,  auto negociación.
- Algunos son administradores: Nos permiten hacer  grupos de interfaces los cuales estan encasulados.(Redes VLAN)
- No existen colisiones.
- 