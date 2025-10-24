# CRC (Capa de acceso a la red)

Tenemos un mensaje  M de m bits, con r bits de redundancia.
La trama es la suma del mensaje (M) y la redundancia (r)

Trama es el mensaje, redundancia y encabezados


Hacemos la división del Mensaje y el residuo pero este no lo conocemos por que sustituimos r con puros ceros para después

$P / T(M+R)$


P es la  trama y para eso necesitamos hacer p = r +1 usando modulo dos de tal forma que T/P no tenga resido

1011 Divide a 110101 **000** estos últimos son la redundancia sacada de p = r + 1 despejamos r y nos queda que es 4 y como faltan 3 dígitos los ponemos como 0

y el residuo de la división es el residuo por lo que es T= 110101(M)**111**(R)

>[!bug] Mayor Errores
>En Wifi si existen mas errores que los que tenemos en etherneth

El mecanismo de flujo tiene la función de no sobrecargar al receptor con los datos , cada **receptor** 

**Control de Flujo**
***Parada y Espera***

-  Parada  y Espera (Stop-Wait) simple
-  Parada  y Espera (Stop-Wait) en canales ruidosos
-  Parada  y Espera (Stop-Wait) con retroalimentación (ARQ, Automatic Repeat-Request)

***Ventana de Paquetes***


Este protocolo suele tener un buen rendimiento cuando son pocos paquetes y de gran tamaño.

Para controlar los nodos existe un notificador **único** y con lo que los identificamos se le conoce como LAN, dirección física o MAC (Es la dirección de cada nodo en una red local).

# MAC

Son un grupo de 6 bytes, los cuales  identifican de manera única el dispositivo conectado a la red local.

XX:XX:XX:XX:XX:XX:XX:XX

Capa de acceso a la red y la física están traslapadas.

3 primeros bytes son los bits de la empresa

**Tipos de comunicación:**

El primero es la de entrada y el segundo datos son las salidas
- Unicast (Uno a uno).
- Multicast (Uno, alguno):Solo a que se le quiere mandar el paquete lo utiliza los demás lo tiran.
- Broadcast (Uno a todos): Si se le pone FF..F todos los nodos van a tomas los paquetes. Por lo que puras F son de este tipo de comunicacion.

>[!NOte]
> Las Unicast y multicast son las mas utilizadas ethernet, para poder comunicarnos entre nodos necesitamos saber el direccion MAC. 
> La IP es en la capa de red

En el encabezado tiene que la dirección MAC del destinatario y el que lo manda

>[!note] 
>Las direcciones MAC pueden cambiar por lo que es necesario es que se pregunte constantemente su direccion.

***Funcionamiento del ARP (Addres Resolution Protocol)***

Se conoce la IP y a quien le corresponda le manda su MAC

##  TRAMA Ethernet 



