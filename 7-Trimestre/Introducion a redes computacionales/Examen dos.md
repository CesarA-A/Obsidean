---
Date: 2025-11-12
tags:
---
---

# Capas del modelo TCP/IP

Aplicación.
Transporte.
Internet
Acceso a la Red
Fisica


## Capa Física

Transmisión de bits a través de un medio de transporte. Algunos de sus aspectos son:

- Señales analógicas/digitales
- Medios de transmisión guiados y No guiados.
- Modulaciones.

>[!Note] Conceptos
>Nodos: Cualquier dispositivo conectado a una red.
>Hosts: Son los dispositivos capases de recibir información o mandar datos.
>Enlace: Canal de comunicación entre dos o mas nodos.
>Enlace Simple: Union de dos nodos.

# Ethernet #Ethernet 

- Para evitar colisiones en un medio compartido se usa el protocolo **CDMA/CD**(es protocolo solo es para ethernet)
- Al momento de enviar los paquetes se necesita establecer un acuerdo previo.
- No hay retroalimentación entre las interfaces (el servicio no es fiable).
- La transmisión se hace en banda base y se suele usar la **codificación Manchester**.

### Tipos  de codificación
La codificacion es convertir una Señal digital entra señal digital

Digital -> Digital

- NRZ-L
- NRZ-I
- Bipolar-AMI
- Manchester
- Manchester Diferencial

---

## Capa de Acceso a la red

Se encarga de efectuar el <mark style="background: #BBFABBA6;">enlace fisico con los nodos de la red</mark>.(Mueve los paquetes que en esta capa se le llaman datagramas)

Lo que se desea es que se mejore el envió de datos esto por un medio de comunicación o enlace de comunicación.

A esta capa también se le conoce como **Protocolo de Control de Enlace de Datos** la  cual se encarga de:

- **Encapsulamiento (entramado):** Se trata en diseñar las tramas para al receptor le sea mas sencillo encontrar el inicio y final del bloque o trama.
		Ejemplos:
		1. Conteo de byes
		2. Bits bandera
		3. Violasiones de codificación.
 
- **Acceso al enlace**: 
	- Tipos
		1. **Punto a punto**:Un único enlace simple.
		2. **Difusión**:Varios nodos comparten el mismo enlace.


Cuando dos o mas nodos mandar información se dice que colisionan.

Protocolos de acceso múltiple se pueden clasificar en:
1. Particionamiento del canal: TDA y FDM
2. Acceso aleatorio: ALOHA y CSMA
3. Toma de turnos: Paso de testigos.


### ALOHA (puro)

Si hay datos por enviar estos se mandan y si existe una colisión la estación será informada y volverá a transmitir.

### ALOHA Ranurado
Solo de manda la información en el ranurado.

### CSMA (Carrier Múltiple Access)

La idea es que antes de mandar información primero escuchemos el canal.

**CSMA o CSMA 1-Persistente:** Siempre escucha el canal y nada mas manda información cuando esta libre.

**CSMA No Persistente:** Si el canal esta ocupado esperamos un tiempo aleatorio para volver a escuchar el canal, para que si esta libre transmitir los datos.

**CSMA p-Persistente:** Si el canal esta libre entonces  existe la **probabilidad p** la cual le indica si transmite o espera para volver a mandar la información.

**CSMA/CD** ->Esta es para rebles cableadas (Ethernet)
Su objetivo es detectar colisiones cuando dos dispositivos mandan información.

Funcionamiento:
1. El dispositivo escucha el cana.
2. Si esta libre transmite.
3. Si existe una colisión la detecta y detiene la trasmisión.
4. Espera un tiempo aleatorio y vuelve a intentarlo.

Ventajas: Es eficiente en medio fisicos.
Desventajas: No funciona en redes inalambricas.

**CSDA/CA** ->  Para redes inalambricas
Carrier Sense Multiple Access

Evita las colisiones antes de trasmitir.
Funcionamiento:
1. El dispositivo escucha el canal.
2. Si esta libre espera un tiempo aleatorio antes de transmitir.
3. Puede enviar una señal de **reserva** (RTS-CTS) para evitar que otros transmitan al mismo tiempo.

Desventaja: Introduce mayor latencia.

