# gantt-ej-4

| Descripción                                         | Tarea | Precedente(s) | Tiempo (semanas) |
|-----------------------------------------------------|-------|---------------|-------------------|
| Entrevistar ejecutivos                              | A     | Ninguna       | 6                 |
| Entrevistar personal en abastecimiento de pedido    | B     | Ninguna       | 3                 |
| Diseñar prototipo de entrada                        | C     | B             | 2                 |
| Diseñar prototipo de salida                         | D     | A, C          | 3                 |
| Escribir casos de uso                               | E     | A, C          | 4                 |
| Registrar las reacciones del personal a los prototipos | F   | D             | 2                 |
| Desarrollar el sistema                              | G     | E, F          | 5                 |
| Escribir manual de capacitación                     | H     | B, G          | 3                 |
| Capacitar al personal en abastecimiento de pedidos   | I   | H             | 2                 |


la Ruta Crítica

La ruta crítica es la secuencia de tareas que determinan el tiempo total del proyecto. Para identificarla, calculamos el camino con la duración más prolongada desde el inicio hasta el final.

Posibles Caminos y Duración
1. **A → D → F → G → H → I**: 6 + 3 + 2 + 5 + 3 + 2 = 21 semanas
2. **A → E → G → H → I**: 6 + 4 + 5 + 3 + 2 = 20 semanas
3. **B → C → D → F → G → H → I**: 3 + 2 + 3 + 2 + 5 + 3 + 2 = 20 semanas

La ruta crítica es la primera secuencia: **A → D → F → G → H → I**, que toma **21 semanas**. Cualquier retraso en estas tareas retrasará el proyecto completo.

Reducción en “Escribir Casos de Uso”

Reducir el tiempo en la tarea "Escribir casos de uso (E)" no sería útil para reducir la duración total del proyecto, ya que esta tarea no se encuentra en la ruta crítica. Reducciones en tareas fuera de la ruta crítica no afectan el tiempo total de finalización.



```mermaid
flowchart TD
    %% Tareas y dependencias
    A[Entrevistar ejecutivos] --> D[Diseñar prototipo de salida]
    A --> E[Escribir casos de uso]
    B[Entrevistar en abastecimiento] --> C[Diseñar prototipo de entrada]
    C --> D
    C --> E
    D --> F[Registrar reacciones]
    E --> G[Desarrollar el sistema]
    F --> G
    B --> H[Escribir manual de capacitación]
    G --> H
    H --> I[Capacitar personal]



