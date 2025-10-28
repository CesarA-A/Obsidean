
## Sistema  Distribuido

Es un sistema en donde el software y hardware se comunicar por medio de mensajes.

**Concurrencia**:Es donde múltiples tarea están sucediendo a la vez.
**Paralelismo**:Cuando dos tarea se ejecutan simultaneas.

### Elementos de una aplicación Distribuida

***Indispensables***

- **Designación**:Mecanismos para referenciar a los recursos  esto con el fin de poder acceder a ellos.
- **Localización**:Esquema que nos permite saber donde esta cada componente.
- **Comunicación y sincronización**:Medio para mandar información y ocurrencia de datos.
---

- Tolerancia a fallas.
- Escalabilidad
- Transparencia
- Balanceo de cargas




# Linda: Espacio de tuplas

Es un modelo que se enfoca en la coordinacion entre procesos recurrentes o distribuidos.

El **espacio de tuplas** es como tener una bolsa que contiene tuplas, en donde cada procesos hace operaciones con ellas.

>[!NOTE] Operaciones
>OUT: Sacar tuplas
>IN: Meter tuplas
>RD: Buscar tuplas

**Caracterización y problemática**

- Permite compartir.
- Apertura: Un sistema es abierto cuando puede ser extendido sin afectar o duplicar servicios.
- Seguridad
- Escalabilidad
- Tolerancia a fallas
- Transparencia: Para que los usuarios sientan que se comparta como una aplicación tradicional.
	Niveles de Transparencia (ISO RM ODP)
	1. Acceso
	2. Localización: No se deben indicar donde están los objetos.
	3. Concurrencia: No se deben percibir los procesos recurrentes.
	4. Replicas: Aumentar disponibilidad y eficiencia sin informar al usuario.
	5. Fallas: Permitir que se termine las tareas a pesar de las fallas/
	6. Migración.
	7. Rendimiento.
	8. Escalamiento.

- Balance de cargas: Es la estrategia para distribuir tareas de una manera equitativa para evitar sobrecargas.

---
# Middleware

Es una capa de software que esta entre el sistema operativo y la aplicación. Su tarea es transparentar la distribución de la plataforma. Así los programadores nos enfocamos en la aplicación.

**Que ofrece**

- Comunicación y sincronización
- Designación
- Localización

## Tipos de servicios

**Servicios funcionales**:Para los que el sistema fue construido (independientes)
1. Comunicación
2. Sincronización
3. Designación
4. Localización

**Servicios NO funcionales**:Son los relacionados con la calidad del sistema.
1. Tolerancia a fallas.
2. Balance de cargas




 