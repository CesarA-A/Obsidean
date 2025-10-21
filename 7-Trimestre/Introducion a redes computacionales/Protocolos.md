 15 Octubre 2025

**Funciones de los protocolos**

- Encapsulamiento: Agrega información de control.
- Segmentación y ensamblado:
	- Segmentación: Dividir un mensaje en partes.
	- Ensamblado: Volver a unir cada una parte del mensaje.
- Control de conexión: Solamente se necesita si en orientado.
- Entrega en orden.
- Control de flujo.
- Multiplexación: Es una técnica para que las señales pasen una por una a la capa física.
- Servicios de conexión.
- Tamaño de mensaje.
- Tiempo de espera

>[!NOTE] Nota
>Cada capa tiene sus propias funciones de protocolos.

# Capo de enlace de Datos (red) para el Modelo OSI

Transforma el medio de transmisión  en una linea de comunicación libre de errores. Proporciona un servido de transferencia de datos seguros a treves del medio físico.

1. Se encarga de **sincronización** de paquetes denominados tramas (frames).
2. **Maneja los errores**
3. **Control de flujos**:Controla la velocidad con la que la fuente envía los datos.
4. Se agregan bit de inicio y fin.

## Mecanismo de Paridad

Nos permite detectar los errores esto por medio de la cantidad de unos **1** que cuenta nuestro mensaje. Existen varios tipo los cuales son:

- Par: Busca los unos **1**  y tiene que ser par si no lo es se agrega  un 1 lo cual hace que sea impar que cuando lo reciba el receptor sabrá  que es un error.
- Impar: Busca los unos **1**  y tiene que ser impar si no lo es se agrega  un 1 lo cual hace que sea impar que cuando lo reciba el receptor sabrá  que es un error.


## Aloja 

Para evitar que los paquetes colisionen, en este existe  un **estación central**.

Se le asigna un tiempo de espera aleatorio y el que sea mayor es el primero en mandar la señal