# SJA-UTA — APE 3

Proyecto de Estructura de Datos de Ingeniería de Software de la Universidad Técnica de Ambato.

El Sistema Jerárquico Académico UTA utiliza dos estructuras:

- Un árbol general para representar la organización académica: universidad, facultades, carreras, niveles y paralelos.
- Un árbol binario de búsqueda por cada paralelo para gestionar estudiantes ordenados por matrícula.

## Organización del repositorio

| Carpeta                    | Contenido                                                                                                                                                         |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Grupo1](Grupo1/README.md) | Fase 1: caso práctico, modelos, enumerados, diagramas, datos de prueba y código base.                                                                             |
| [Grupo2](Grupo2/README.md) | Fase 2: inserción, búsqueda, recorridos recursivos, trazas y consultas del árbol general. Incluye modificación y eliminación del ABB como adelantos de la Fase 3. |
| [Grupo3](Grupo3/README.md) | Fase 3: transformación a binario, eliminación segura, casos límite, estadísticas del ABB y clínica de errores.                                                    |

## Fase 1 — Modelado y estructura base

El Grupo 1 define el caso SJA-UTA, las clases, las relaciones, las reglas jerárquicas y los datos de prueba.

La organización utiliza un árbol general porque una unidad puede tener varios hijos. Cada paralelo contiene su propio ABB de estudiantes.

- [Documentación del Grupo 1](Grupo1/README.md)

## Fase 2 — Implementación recursiva

El Grupo 2 continúa sobre la estructura base e incorpora:

- Agregar y buscar unidades académicas.
- Mostrar la jerarquía con sangría.
- Consultar grado y nivel.
- Contar hojas.
- Insertar estudiantes sin matrículas repetidas.
- Buscar estudiantes por matrícula.
- Obtener preorden, inorden y posorden.
- Mostrar trazas de las llamadas recursivas.
- Modificar y eliminar estudiantes como adelantos de la Fase 3.

La altura del árbol general sigue pendiente en la copia revisada. Su resultado esperado con los datos iniciales es de cuatro aristas.

### Documentación (Fase 2)

- [README del Grupo 2](Grupo2/README.md)
- [Casos de prueba](Grupo2/docs/casos_prueba.md)
- [Decisiones de implementación](Grupo2/docs/decisiones.md)
- [Diagramas de flujo](Grupo2/docs/diagramas-flujo/README.md)
- [Diagramas de secuencia](Grupo2/docs/diagramas-secuencia/README.md)
- [Trazas de recorridos](Grupo2/docs/trazas_recorridos.md)
- [Trazas de inserción y eliminación](Grupo2/docs/trazas_insercion_eliminacion.md)

### Facilitación de la clase (Fase 2)

La Fase 2 utiliza cuatro estaciones: inserción, preorden, inorden y posorden, y caza del error recursivo.

- [Organización de las estaciones](Grupo2/facilitacion/estaciones/README.md)
- [Lista de cotejo](Grupo2/facilitacion/lista-cotejo-fase2.md)
- [Enlaces y recursos](Grupo2/facilitacion/enlaces.md)

## 🚀 Fase 3 — Transformación, Eliminación y Casos Límite (Grupo 3)

Esta fase integra operaciones avanzadas sobre las estructuras base, garantizando que los métodos no arrojen excepciones y funcionen de manera independiente. Todo nuestro desarrollo e integración se encuentra aislado en el directorio `Grupo3` para evitar conflictos con las fases anteriores.

- **Estadísticas (ABB):** Cálculo de altura, cantidad de nodos, valores mínimos/máximos y promedios generales.
- **Eliminación Segura:** Borrado de nodos en el árbol general (validando que no existan subunidades) y en el ABB (manejando casos de hoja, un hijo y reemplazo por sucesor inorden).
- **Transformación a Binario:** Conversión del Árbol General a Árbol Binario aplicando la regla algorítmica: *"Primer hijo → izquierdo, siguientes hermanos → derecho"*.

### Estructura de Trabajo (Fase 3)

- [`/src`](Grupo3/src): Núcleo del código fuente actualizado (`ArbolOrganizacional`, `ArbolEstudiantes` y `Main` adaptado a la Fase 3).
- [`/docs`](Grupo3/docs): Trazas de escritorio sobre la transformación y documentación de casos límite del sistema.
- [`/facilitacion`](Grupo3/facilitacion): Material interactivo para la clase, incluyendo la Clínica de Errores, la Lista de Cotejo y accesos a Padlet/Quizizz.

## Ejecución

Consultar las instrucciones del README de cada grupo en su respectiva carpeta.

Los proyectos se compilan por separado porque contienen clases con los mismos nombres y paquetes. **No compilar juntos los archivos Java de Grupo1, Grupo2 y Grupo3.**

La guía solicita JDK 21. El código también se ha comprobado con Java 17.

## Trabajo colaborativo

Cada integrante trabaja en su rama y abre un pull request hacia `main`. 
- **Fase 3:** Justin lidera la integración y evaluación de los aportes del Grupo 3.
Después de integrar, se comprueban los resultados y se actualiza la documentación.