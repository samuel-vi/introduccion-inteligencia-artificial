# Actividad de aprendizaje

## Comparación de estrategias de búsqueda no informada

## Propósito

Comparar experimentalmente **BFS, DFS e IDS** sobre un mismo espacio de estados, analizando el orden de exploración, el camino encontrado, el número de nodos visitados y la profundidad de la solución.

La actividad complementa el notebook del subtema y permite observar cómo distintas estrategias pueden producir comportamientos diferentes aun cuando resuelven el mismo problema.

---

## 1. Ejecuta el notebook

Utiliza el notebook:

[Implementación de BFS, DFS e IDS](../notebooks/busqueda-no-informada.ipynb)

Ejecuta todas las celdas y verifica que los tres algoritmos encuentren una solución.

---

## 2. Registra los resultados

Completa la siguiente tabla:

| Algoritmo | Orden de exploración | Camino encontrado | Nodos visitados | Profundidad |
|---|---|---|---:|---:|
| BFS | | | | |
| DFS | | | | |
| IDS | | | | |

---

## 3. Cambia el objetivo

Ejecuta nuevamente los algoritmos utilizando como objetivos:

a) D

b) E

c) F

d) G

Registra los resultados y responde:

a) ¿Qué algoritmo visita menos nodos en cada caso?

b) ¿Cuál encuentra primero una solución poco profunda?

c) ¿Cuál presenta mayor variación al cambiar el objetivo?

d) ¿Qué efecto tiene el orden de los sucesores en DFS?

---

## 4. Construye un nuevo espacio de estados

Modifica el grafo original y crea uno nuevo con al menos **10 estados**.

Define:

```text
Estado inicial =
Estado objetivo =
```

Incluye al menos:

a) Dos ramas diferentes

b) Una rama más profunda que las demás

c) Dos caminos posibles hacia el objetivo

d) Un estado que no conduzca a la solución

---

## 5. Ejecuta BFS, DFS e IDS

Aplica los tres algoritmos sobre tu nuevo espacio de estados.

Registra:

a) Orden de exploración

b) Camino encontrado

c) Número de nodos visitados

d) Profundidad de la solución

e) Algoritmo que encontró primero el objetivo

---

## 6. Comparación

Completa la siguiente matriz:

| Criterio | BFS | DFS | IDS |
|---|---|---|---|
| Explora por niveles | | | |
| Explora en profundidad | | | |
| Utiliza poca memoria | | | |
| Puede repetir nodos | | | |
| Encuentra soluciones poco profundas | | | |
| Puede verse afectado por el orden de sucesores | | | |

---

## 7. Análisis

Responde:

a) ¿Cuál algoritmo resultó más eficiente en tu problema?

b) ¿Cuál visitó más estados?

c) ¿Cuál utilizó el camino más corto en número de pasos?

d) ¿DFS encontró siempre la misma solución que BFS?

e) ¿IDS realizó trabajo repetido?

f) ¿Por qué puede ser útil IDS a pesar de repetir estados?

g) ¿Qué estrategia seleccionarías si la memoria fuera limitada?

h) ¿Qué estrategia seleccionarías si sospechas que la solución está cerca del estado inicial?

---

## 8. Modificación experimental

Realiza uno de los siguientes cambios:

a) Aumenta el factor de ramificación

b) Aumenta la profundidad del objetivo

c) Cambia el orden de los sucesores

d) Agrega estados que no conduzcan al objetivo

Ejecuta nuevamente los algoritmos y explica cómo cambia su comportamiento.

---

## Producto esperado

Entrega un documento o notebook que incluya:

a) Resultados del ejemplo original

b) Tabla comparativa

c) Nuevo espacio de estados

d) Resultados de BFS, DFS e IDS

e) Evidencia de la modificación experimental

f) Análisis de los resultados

g) Conclusión

---

## Criterios de evaluación

| Criterio | Valor |
|---|---:|
| Ejecución correcta de los algoritmos | 25% |
| Construcción del nuevo espacio de estados | 20% |
| Comparación experimental | 20% |
| Interpretación de resultados | 20% |
| Conclusión y claridad de la evidencia | 15% |

---

## Reflexión final

Responde en máximo **150 palabras**:

> **¿Por qué no es suficiente conocer que un algoritmo encuentra una solución y también es necesario analizar cuánto tiempo, memoria y exploración requiere para obtenerla?**

---

## Recursos de apoyo

[Consultar contenido del subtema 2.3](../)

[Consultar recursos complementarios](../recursos/)

[Consultar comparación visual de BFS, DFS e IDS](../imagenes/comparacion-bfs-dfs-ids.png)

[Consultar notebook](../notebooks/busqueda-no-informada.ipynb)

---

[← Volver al subtema 2.3](../)
