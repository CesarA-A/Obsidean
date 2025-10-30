---
Date: 2025-10-30
tags:
  - "#Capa_Internet"
  - "#IP"
---
---

En las capas de acceso a la red y la física usan software y hardware.

## **Funciones básicas:**
- Transmisor de datos.
- Enrutamiento de los datos al destino correcto.

## **Protocolos**

- Protocolo de Internet (IP -> Protocolo de Internet)
- Protocolo de resolución de dirección (ARP):Estado de la red
- Protocolo de Mensajes de Control de in Internet (ICMP)


**Direcciones IP vs v4**

Se compone de 4 octetos cada uno de 8 bits.

Una parte  se le llama prefijo,esta asociada a la red local.
La parte restante son el host.
Todos los host de una red tiene el mismo prefijo.
La longitud del prefijo, indica la mascara que extraerá la dirección de red.

A nivel capa 3: Su prefijo es diferente  , pero se pueden comunicar por que estan en la misma subred.

A nivel capa 2:Codos los nodos se pueden comunicar por que están conectados por un 
conmutador por lo que dependen de estar en una VLAN.

Con el  prefijo se puede usar para mandar los paquetes (usan los prefijos)

 Las direcciones IP de agrupan por:
 
Clase A, B,C, la A es la mas grande
Las IP se escriben en IP.

La primera IP con ceros no se puede usar, aquí también se puede usar el broadcast entonces le restamos uno a las posibles combinaciones.
2^16 -1-1= 65534 posibles combinaciones

La de broadcast es la 108.130.1.1
Cada segmento debe tener una puerta  de enlace.



[[Ethernet]]


