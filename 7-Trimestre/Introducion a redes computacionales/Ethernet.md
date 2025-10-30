---
Date: 2035-10-21
tags:
  - Ethernet
---
21 Octubre 2025
    
Conceptos

- **Nodo**:Dispositivos conectados a la red.
- **Host**:Dispositivo capaz de generar o recibir datos.
- **Enlace**:Comunicación entre los nodos adyacentes.
- **Enlace Unico:** Unión entre dos de sus extremos.---


# Ethernet

Esto es en la capa física  y se utiliza Manchester 
- Para evitar colisiones se hace uso del protocolo de CSMA/CD (Carrier Sense).
- Proporciona un servicio sin conexión.
- El servicio es no fiable entonces no existe una retroalimentacion.
- La transmisión se realiza en banda base y generalmente se emplea codificación Manchester. 


>[!info]  Modulación
>Es desplazar una señal de su banda base hasta el ancho de banda.(Dezplazar)


## Capa de Acceso a la Red (TCP/IP)

Pasa los bits o tramas a la capa física es insuficiente, esto por que se generan errores, velocidad y sincronizar.

Se encarga de:
- Encapsulamiento
- Acceso a la red 
==Me faltaron cosas


**Entramado**:Crear una capa de unos y ceros (tramas), esto con el fin de encontrar el inicio yfin del bloque o trama.

*Por ejemplo*:

1. Conteo de bytes
2. Bits bandera:
3. Violaciones de la codificamos:Detectar cuando inicia y termina la trama


Si dos nodos o mas nodos transmiten al mismo tiempo **colisionan**

Los protocolos se pueden clasificar en:

- Particionamiento del canal:TDN Y FDM
- Acceso aleatorio: ALOHA,CSMA
- Toma de turnos:Paso de testigos (token)

TDM9->TDMA
FDM->FDMAA

Warcarp:El espacio que queda en medio de la señal es decir los pedazos muertos


espectro cuadrado de la señal 

>[!info] Informacion
>Mientras mas grande el ancho de banda mayor sera su velocidad.


### ALOHA (puro)

Algoritmos de contienda
Lo de el numero aleatorio antes de poder volver a retransmitir los datos.
Cada vez que existe una colisión se manda una paquete de información.

Estación Central:Si uno nodo manda los datos y llega le informa a los demás datos que si llego

### ALOHA (RANURADO)


El tiempo de segmenta en donde cada inicio de las ranuras es cuando se transmite la información y al final nos dice que es lo que sucedió.

Solo se mandan los datos al inicio de la ranura.

Pero si dos nodos mandan al inicio de la ranura ahora se tienen que esperar n ranuras  aleatorias para que avance.

## Variantes de las CSMA

- **CSMA O CSMA 1-Persistente**: No están ranurados, siempre escuchan el canal y una vez libre transmite.
- **CSMA no Persistente**: Si el canal esta ocupado, espera un tiempo aleatorio para después volver a escuchar el canal.Si el canal esta libre transmite.
- **CSMA p-Persistente**:Si el canal esta libre se transmite con probabilidad de p.


>[!bug] Investigar para examern
>CSMA/CD (avisa de la colision) y CSMA/CA (evita la colisión)
>Como saber si un protocolo es bueno o malo
>Se realiza un analisis y se obtienen algunas metricas como throuhput o caudal


**Control de errores**

- Errores dentro de la tramas 
- Tramas en orden inapropiado
- Desaparición de tramas


**Codigos detectores**

- Paridad:par o impar
- Suma de comprobacion
- CRC (Comprobacion de redundantes ciclica, cyclic redundancy check)


