13 Octubre 2025

Todos los clientes van a recibir el mismo mensaje.

<mark style="background: #FFB86CA6;">Eclusion mutua y variable compartida</mark>
Se usan mutex

# Linda: Modelo de espacio de tuplas
Su propósito es hacer trasparente la paralelización en la arquitectura MIMD con memoria compartida. 
Se parece al modelo <mark style="background: #ADCCFFA6;">productor-consumidor</mark>, en donde hay colaboradores.

## Operaciones 
1. **Meter**:Introduce una tupla al espacio.
2. **Tomar**:Sacar una tupla del espacio que coincida con la descripción $descripción.tomar("resultado",↑r)$
3. **Evaluar**:Proceso para evaluar la tupla y dejar el resultado.
4. **Leer**:Lee la tupla  sin reverla.

