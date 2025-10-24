---
Date: 2025-10-23
tags:
  - Examen1_Redes
---
---

# Introducción a las redes

Fuente -> Transmisor -> Medio de transmisión -> Receptor -> Destino

**Fuente**:Es donde se reciben los datos o el que pose los datos.
**Transmisor**:Se encarga de convertir los datos en señales para poder mandar la información.
**Medio de transmisión**:Forma en la que se mandaran las señales.
**Receptor**:Encargado de convertir las señales para que llegue a su destino.
**Destino**:Lugar en donde se desea que llegue las señales ya decodificadas pero también puede mandarlas.

## Señales

-  Digital: Toma valores finitos en un conjunto [a,b]
- Analógico : Toma valores infinitos en un conjunto (-inf,inf)

###  Parámetros de las señales

**Amplitud**: Intensidad de una señal.
**Frecuencia**:Cantidad de veces que se repite en un segundo (Hz)
**Fase**:Posición de la señal respecto al tiempo.
**Ancho de banda**: Es el radio de frecuencia en donde se tiene mayor energía (información)

### Factores que afectan a las señales

**Atenuación**: Perdida de energía y si sucede el receptor puede no detectar los datos enviados.
**Distorsión (Desplazamiento)**:Cambios en la forma de la señal.

## Modos de transmisión

1. **Simplex**:Solamente va a una dirección.
2. **Half-Duplex**: Va a hacia ambas direcciones pero solamente una a la vez.
3. **Full-Duplex**:Comunicación simultanea en ambas direcciones.

## Transmisión

Analógica -> Analógica :Modulación
Digital -> Analógica: Modulación

Digital->Digital : Codificación

### Elementos o inconvenientes

- **Interfaces:** Puntos de conexión entre las capas. Como accede una capa a los servicios de la capa inferior.
- **Representación**:Forma en la que se codificara la información.
- **Sincronización**:Que el receptor y emisor estén alineados en tiempo.
- **Detección y corrección de errores**
-  **Presentación/Formato de mensaje**:Como se estructura la información.
- **Seguridad**
- **Direccionamiento**
- **Control de flujo**:Para evitar cuellos de botella, que el emisor sature al receptor.
- **Cambios en la estructura o topología de la red**
- **Sintaxis**
- **Semántica, formato de los datos**
- **Temporización**
	- **Sincronización de la velocidad**:Que ambos reciban/transmitan a ritmos compatibles.
	- **Secuenciación**:Que los datos lleguen en orden.
- **Control de errores**
- **Control de flujo**
- **Multiplexacion**


**<mark style="background: #FF5582A6;">Red</mark>**:Es el conjunto de dispositivos digitales autónomos conectados para poder compartir información y recursos.

**Capas pares**:Capas del mismo nivel en dos dispositivos que están intercambiando información.
**Protocolos**:Reglas que se tiene entre las capas pares.

<mark style="background: #FF5582A6;">Arquitectura de la red</mark>:Diseño que organiza la comunicación entre dispositivos, organiza la comunicación entre capas independientes 

## Tipos de servicios

- Orientado a Conexión
	- Secuencia
	- Flujo
- No orientado a Conexión
	- Con Confirmación
	- Sin Confirmación



***Capa***: Es un modulo el cual realiza una tarea.

# Modelos de referencia

## Modelo OSI

Principios

1. Cada capa debe tener una tarea especifica.
2. Las capas deben definir sus protocolos estandarizados.
3. Sin tanto flujo de datos.
4. Numero optimo de capas.

## Capas

1. Aplicación
2. Presentación
3. Sesión
4. Transporte
5. Red
6. Enlace de datos
7. Física

### Capa de Aplicación
Acceso a los usuarios.

Para que las aplicaciones puedan transmitir información hacia un punto determinado. Aquí se encuentran los protocolos particulares de las aplicaciones que son empleadas por los usuarios.

### Capa de Presentación
Es la de mantener las sintaxis y la semántica de los datos transmitidos, sus tareas son:

-  Cifrado de los datos.
- Comprensión de los datos.
- Formateo de los datos

  
### Capa de Sesión
En esta capa se establece el control de dialogo y sincronización pero a nivel de aplicación.

Funciones principales:

1. Control de dialogo :Define el turno de la transmisión.
2. Administración de turnos.
3. Recuperación.

### Capa de Transporte

Ofrece servicios confiables sobre una red poco confiables , ofrece servicios a las aplicaciones, es necesario una multiplexación de los flujos de datos.

Además de eso la capa de transporte y la de enlace de datos comparten algunas funciones.
1. Control de errores.
2. Secuenciación.
3. Control de flujo.

### Capa de Red
Es la encargada de evitar la congestión.

Servicios:

1. Orientado a conexión en donde se predomina la calidad de servicio.CIrcuito VIrtual (CV)

Función :Enrutar los paquetes desde el origen hasta un destino.

Elementos:
- Algoritmos para escoger rutas.
- Estructuras para guardar datos de las rutas.
- Algoritmo para buscar en estas rutas.

**Enrutador**:Su función es dirigir el trafico de datos, se conforma de dos funciones las cuales son el reenvió, enrutamiento(escoger la mejor ruta para que los paquetes de datos viajen)

Algoritmos de enrutamiento :Decide cual será la linea de salida que seguirá un paquete.

### Capa de Enlace de datos

Garantiza la transferencia de tramas sin errores dentro de una conexión física.

**Tramas**:Flujos de bits en bloques o paquetes.

Contiene una subcapa la cual se llama <mark style="background: #FFB86CA6;">Control de Acceso al Medio</mark> la cual se encarga de controlar el acceso al canal compartido.

>[!bug] 
>Esta capa no se define como tal unos protocolos

### Capa Física

Manda los datos de un punto a otro y para esto los medios de trasmisión se clasifican en:

- Medios Guiados: Par trenzado, cable coaxial, fibra óptica.
- Medio NO guiados: Intervienen las comunicaciones inalámbricas. Ejemplos: Espectro Electromagnético, ondas de rabio, microondas.

bits ->Señales eléctricas.

## Resumen de las capas

**Capa Física**:Transforma los bits en señales eléctricas para mandarlas por un medio de transmisión.

**Capa de Enlace de datos**:Agrupa los bits en tramas para detectar errores, corregirlos ademas de eso controla el acceso al medio.
	x
**Capa de Red**:Decide que ruta van a tomas los datos.

**Capa de Transporte**:Se  asegura que los datos lleguen completos y en orden.

**Capa de Sesión**:Se encarga de establecer, mantener y cerrar la comunicación entre aplicaciones.

**Capa de Presentación**:Traduce ,cifra o comprime los datos para que tengan sentido para la aplicación.

**Capa de Aplicación**:Es la interfaz con la interactúa el usuario.

<mark style="background: #BBFABBA6;">NEUMOTECNIA</mark>

Feliz El Raton Travieso Se Pasea Alegramente
