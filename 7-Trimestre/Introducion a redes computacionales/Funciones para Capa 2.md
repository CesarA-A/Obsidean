---
Date: 2024-10-07
tags:
  - "#funciones_capa2"
---
---
# Funciones para la comunicación 

##  Sockets
Se utiliza para poder comunicarnos bidirecionalmente entre dos procesos, esto puedo ser en la misma maquina o a través de la red.

***Funciones***


- Para la creacion de un socket listo para operar en enlace (Ethernet )

```c
//Parametros de la funcion socket
socket(domiain,type,protocolo)
```

```c

#include <sys/socket.h> // socket(), recvfrom(), sendto()
#include <arpa/inet.h> // htons(), ntohs()
#include <netinet/if_ether.h> // struct ether_header, ETH_P_ALL

int s = socket(AF_PACKET,SOCK_RAW,htons(ETH_P_ALL));

if(s == -1)
{
	perror("Erorr al crear el socket");
}
```

**Parámetros**

- AF_PACKET : Le indica al socket que va a trabajar con tramas Ethernet.
- SOCK_RAW : Para que nosotros armemos la trama 
- htons(ETH_P_ALL): Es el protocolo para detectar todas las tramas ethernet.Tambien se le puede pasar como parámetro ETH_TYPE aquí nadamas EtherType.

##  Ioctl

Es una interfaz genérica que le pide/pone información de red al kernel.

Sirve para comunicarse con los controladores de dispositivos para hacer operaciones de bajo nivel que no tienen una llamada del sistema estandar.

```c
#include <net/if.h> // struct ifreq (para nombres de interfaz)
#include <sys/ioctl.h> // ioctl() para obtener información de interfaz

struct ifreq ifr;

memeset(&ifr,0,sizeof(ifr));
strncpy(ifr.ifr_name,nombre_interfaz,IFNAMSIZ-1);
ioctl(socket,SIOCGIFINDEX,&ifr); //Para obtener el indice de la interfaz y se guarda eb ifr.ifr_ifindex

ioctl(socket,SIOCGIFHWADDR,&ifr);//ahora ifr.ifr_hwaddr) tiene la MAC 
```

**Parámetros y funciones**

- memeset(puntero,valor,tamaño_en_bytes) :Se utiliza para llenar un bloque de memoria con un valor en especifico, para el **puntero** este puede ser por malloc o un puntero directo,valor es con lo que queremos llenar ese bloque de memoria, tamaño en bytes para esto se usa sizeof().
- strncpy(destino,origen): Para copiar la string origen en el destino esta en la libreria **destino**.
- ioctl(socket,cmd,struct ifreq *ifr*); El comando es lo que hace la operaciones alguno de estos comandos son **SIOCGIFNDEX** este rellena ifr->ifr_ifrindex con el indice de la interfaz.El otro es **SIOCGIFHWADDR** este rellena ifr->ifr_hwaddr con la MAC

>[!NOTE] Interfaz
>Dentro de ifr.ifr_name debemos tener el nombre de la interfaz antes de llamar.

## Bind

Solo sirve para AF_PACKET, por que esta función asocia un socket a una interfaz/dirección local. 
Se utliza para asignar una direccionde protocolo local (IP, numero de puerto, etc), pero solo si el socket no tiene nombre.

```C

struct socket_ll sa={0};
sa.sll_family = AF_PACKET;
sa.sll_protocol = htons(ETH_P_ALL);
sa.sll_ifindex = ifindez;

bind(socktf,(struct sockaddr *)&sa,sizeof(sa));
```

>[!bug]
>Si no se hace bind recvfrom puede recivir tramas de todas las interfaces.

## Sendto

Envía bytes al destino indicado por addr. En la capa 2 add es strcut sockadd_all y el buf debe contener la trama Ethernet completa(14 bytes de cabezera + payload).

```c
sendto(socktd, bufferm sizeof(struct ether_header) + payload_len,(struct sockaddr *)&socket_address, sizeof(socket_address))
```
**Parámetros y funciones**

- sendto(fd, buf, len, flags, (struct sockaddr*)&addr, addrlen): **fd** es el socket a través del cual se enviaran los datos, **buf** es un puntero al buffer el cual contiene los datos (mensaje) que se va a transmitir, **len** tamaño del mensaje (buffer), flags  es la forma en la que se controla la transmisor (MSG_00B para datos fuera de banda) .Normalmente se pone en 0,**addr** un puntero a la estructura que contiene la dirección destino,**addlen** es el tamaño en bytes de la estructura ala que apunta dest_addr.


## Recvfrom

Nos sirve para recibir las tramas completas con la cabecera de Ethernet puesta al inicio del buffer.

```c
int n = recvfrom(sockfd , buffer , BUF_SIZ, NULL, NULL)

if(n){
	struct ether_header *et = (struct ether_header *)buffer;
}
```

**Parámetros**

- recvfrom(fd, buf, len, flags, src_addr, addrlen): **fd** es un socket , **buffer** es un puntero en donde se guardaran los datos, **BUF_SIZ** es el tamaño máximo del buffer, **flags** generalmente se pone en 0 por que es el comportamiento de la recepción, **src_addr**  se utiliza para guardar la dirección del remitente,**addrlen** tamaño del buffer.

##  Htons/ ntohs

1. Htons: Se utiliza para convertir un valor entero corto sin signo del orden de bytes del host al orden de bytes  de la red.

```c
eh -> ether_type = htons(MI_ETHER_TYPE)
if(nhtons(eh -> ether type) == MI_ETHER_TYPE){

}
```

## Memcpy/memeset
Para copiar o llenar bloques de memoria (se usan comúnmente para MAC, payload, etc).

```c
//MAC destino broadcast
memset(eh -> ether_dhost,off,6)

//Copiar MAC origen
memcpt(eh -> ether_shost,ifr.ifr_hwaddr.sa_data,6)

//Copiar payload despues de la cabecera
memcpy(buffer+sizeof(struct ether_header),payload,payload_len)
```

## Close
Cierra el socket

```c
close(socket)
```

# Estructuras importantes

## Struct ifreq

Se suele usar junto con la llamada al sistema ioctl() para inspeccionar o controlar las interfaces de red del sistema.Como para obtener direcciones IP, MAC, las banderas de la interfaz entre mas cosas.
[[Funciones para Capa 2#Ioctl]] 

Esta estructura tiene los siguientes campos y se encuentra en esta libreria#include <net/if.h>:

1. `ifr_name`: Un nombre de interfaz (ej. "eth0", "lo", "wlan0"). Es una cadena de caracteres.La llenamos usando <mark style="background: #FFB8EBA6;">ioctl()</mark>
2. `ifr_ifru`: Una unión que contiene diferentes tipos de datos, dependiendo de la operación `ioctl()` que se realice.
3. `ifr_addr`: Se usa para direcciones (como la IP).
4. `ifr_hwaddr`: Para direcciones de hardware (como la MAC tras SIOCGIFWADDR).
5. `ifr_flags`: Para banderas de la interfaz (como `IFF_UP`, `IFF_RUNNING`).

## Struct sockaddr_ll

Para direcciones a nivel de enlace en sendto/bind

**Campos importantes**
- `sll_family` = `AF_PACKET`
- `sll_protocol` = `htons(ETH_P_...)`
- `sll_ifindex` = índice de interfaz
- `sll_halen` = longitud de la dirección física (6)
- `sll_addr[8]` = MAC destino (primeros 6 bytes)

## Struct ether_header

Se utiliza para representar el encabezado de tramas en ethernet.Esta 
definida en `<netinet/if_ether.h>` o `<net/ethernet.h>`

 **Campos típicos:**
- `ether_dhost[6]` (destino)
- `ether_shost[6]` (origen)
-  `ether_type` (uint16_t)
**Nota:** tamaño = 14 bytes en total.