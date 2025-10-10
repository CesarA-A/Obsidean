2 Octubre 2025

El **modelo de dominio** es todo lo que implica, donde debemos identificar y describir:
- Base de datos.
- Reglas y restricciones.

**Requerimientos**
Son las cosas que el software debe de hacer.
1. Requerimientos funcionales: Lo que queremos que se haga.
2. Requerimientos **No** funcionales: Son las restricciones del sistema. Es decir un requerimiento funcional pude tener requerimientos **No** funcionales.


# Características de un software a gran escala

1. Definición de roles y responsabilidades.
2. Mantenimiento.
3. Métricas(Principios de medición).
4. Gestión de calidad y pruebas.
5. Gestión de configuración.
6. Modulación.
7. Patrones arquitectónicos.
8. Requerimientos no funcionales.
9. Especificaciones detallada de los requerimientos funcionales.

# Metodologías / Modelos de desarrollo 

## Modelo en cascada.

Se sigue me manera secuencial en el cual sus partes son:
1. Análisis de requerimientos.
2. Diseño.
3. Codificación.
4. Pruebas.
5. Mantenimiento.

>[!NOTE] Artefactos
>Lo que recibimos como salida en cada una de las etapas de los modelos (productos).

Este modelo cuenta con <mark style="background: #FF5582A6;">limitaciones</mark>:

1. Falta de flexibilidad.
2. Dependencia de requisitos bien definidos.
3. Retroalimentación tardía.
4. Alto costo de corrección.
5. Tiempo prolongado antes de entregar resultados.
6. Riego de acumulación de errores.
7. Incompatibilidad con proyectos complejos o dinámicos.
8. Subestimación del mantenimiento.

Para solucionar estas limitaciones se crearon variantes basadas en el modelo en cascada.

### Cascada en fases solapadas.

Una de las limitaciones del método tradicional del modelo cascada es que no se puede avanzar hasta terminar por completo la etapa anterior.

Pero en esta versión permite que dos o mas etapas se lleven a cabo en paralelo.

<mark style="background: #FF5582A6;">Limitaciones</mark>:

- Complejidad en la gestión: Se necesita una planificación mas cuidadosa para manejar el solapamiento de las actividades.
- Riesgo de errores en requisitos: Empezar una etapa sin haber terminado la anterior puede generar malentendidos si los requisitos cambian o no están claros.
- Dependencias entre actividades.

### Cascada en subproyectos

Las tareas de el proyecto se dividen en subproyectos (no necesariamente toda la fase), en cada subproyecto hacemos el modelo en cascada tradicional.

<mark style="background: #FF5582A6;">Limitaciones:</mark>

Pueden existir independencias no previstas entre los proyectos.

# Metodologías Agiles 

Son enfoques de gestión de proyectos que se centran en la **flexibilidad**, la **colaboración constante** y la **entrega rápida de valor**.

Ejemplos

- Scrum
- Kanban
- Proceso Unificado Ágil

Para abordar las limitaciones del modelo en cascada, se han desarrollado enfoques iterativos como el [[Proceso unificado]], que permite una mayor flexibilidad en la gestión de requerimientos y validación continua.