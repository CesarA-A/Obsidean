
9 Octubre 2025

Ejemplo: Modelo de tres capas

<mark style="background: #FF5582A6;">Dificultades para resolver:
</mark>
a) "Entrada" o servicios para las diversas aplicaciones.
b)Que los datos lleguen a su destino y en orden.
c)Una interfaz que se encarga de "colocar" los datos en el medio de comunicación.

## Capas


- **Aplicación**:Tendrá la lógica para soportar varias aplicaciones de usuarios.
- **Transporte**:Los datos de la capa de aplicación se empaquetan (*fragmentan*) y se asegura que llegue en orden  y seguros.
- **Acceso a la red**:Que la información llegue a su destino por lo que es necesario las direcciones.


Multiplexar :Para atender diversas aplicaciones, para canalizar los datos para el mismo camino.

**Tipo de servicios**:Forma en la que se va a hacer la conexión, pueden ser de dos tipo:

- Orientado a conexión(Ambos lados deben estar atentos)
	- Secuencial
	- Flujo

- No orientado a conexión
	- Con información
	- Sin información

## Protocolo y servicios
[[Protocolos]]
- Los servicios son las primitivas u operaciones.
- Solo así arriba (una capa arriba)
- Protocolos son las reglas de comunicación entre capas.