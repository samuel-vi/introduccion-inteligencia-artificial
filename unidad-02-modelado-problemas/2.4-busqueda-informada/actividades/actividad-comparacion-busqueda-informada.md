
# Actividad de aprendizaje

## Comparación de estrategias de búsqueda informada

## Propósito

Comparar experimentalmente **Greedy Best-First Search** y **A\***, analizando el efecto de la función heurística sobre el orden de exploración, el costo de la solución y el número de nodos expandidos.

---

## 1. Ejecuta el notebook

Utiliza:

[Implementación de Greedy y A* en Python](../notebooks/busqueda-informada.ipynb)

Ejecuta todas las celdas y verifica los resultados del problema:

```text
Arad → Bucharest
```

---

## 2. Registra los resultados

Completa:

| Algoritmo | Función | Ruta encontrada | Costo total | Nodos expandidos |
|---|---|---|---:|---:|
| Greedy | \(h(n)\) | | | |
| A* | \(g(n)+h(n)\) | | | |

---

## 3. Analiza la diferencia

Responde:

a) ¿Por qué Greedy selecciona Fagaras antes que Rimnicu Vilcea?

b) ¿Por qué A* puede seleccionar un nodo con mayor \(h(n)\)?

c) ¿Qué función desempeña \(g(n)\) en A*?

d) ¿Cuál algoritmo encontró la ruta de menor costo?

e) ¿Cuál parece tomar decisiones más voraces?

---

## 4. Experimento con \(h(n)=0\)

Modifica la heurística para que:

\[
h(n)=0
\]

para todos los estados.

Ejecuta nuevamente A* y registra:

| Aspecto | A* original | A* con \(h(n)=0\) |
|---|---:|---:|
| Costo de la solución | | |
| Nodos expandidos | | |
| Ruta encontrada | | |

Explica qué cambió y por qué.

---

## 5. Heurística no admisible

Modifica uno o más valores de la heurística para que sobreestimen el costo real.

Ejemplo:

```text
h(Pitesti) = 500
```

Ejecuta nuevamente A*.

Analiza:

a) Ruta encontrada

b) Costo total

c) Orden de expansión

d) Diferencia respecto a la heurística original

e) Consecuencias de utilizar una heurística que sobreestima

---

## 6. Diseña una nueva heurística

Propón una nueva función heurística para un problema diferente.

Puede ser:

a) Laberinto

b) Robot móvil

c) 8-puzzle

d) Navegación entre edificios

e) Distribución de objetos

Describe:

```text
Problema =
Estado inicial =
Estado objetivo =
Heurística propuesta =
```

Explica:

a) Qué representa \(h(n)\)

b) Cómo se calcula

c) Por qué podría orientar la búsqueda

d) Si consideras que es admisible

---

## 7. Comparación conceptual

Completa:

| Característica | Greedy | A* |
|---|---|---|
| Utiliza \(h(n)\) | | |
| Utiliza \(g(n)\) | | |
| Considera costo acumulado | | |
| Puede ser óptimo | | |
| Depende de la calidad de la heurística | | |
| Puede consumir mucha memoria | | |

---

## 8. Análisis crítico

Responde:

a) ¿Una heurística admisible necesariamente es una buena heurística?

b) ¿Qué ocurre si la heurística es demasiado poco informativa?

c) ¿Por qué una heurística más precisa puede reducir la exploración?

d) ¿Cuál es el costo de utilizar una heurística compleja de calcular?

e) ¿En qué situación seleccionarías Greedy en lugar de A*?

f) ¿En qué situación seleccionarías A*?

---

## Producto esperado

Entrega un documento o notebook que incluya:

a) Resultados de Greedy y A*

b) Tabla comparativa

c) Experimento con \(h(n)=0\)

d) Experimento con heurística no admisible

e) Nueva heurística propuesta

f) Análisis de resultados

g) Conclusión

---

## Criterios de evaluación

| Criterio | Valor |
|---|---:|
| Ejecución correcta de Greedy y A* | 25% |
| Comparación experimental | 20% |
| Análisis de la heurística | 20% |
| Diseño de nueva heurística | 20% |
| Interpretación y conclusión | 15% |

---

## Reflexión final

Responde en máximo **150 palabras**:

> **¿Por qué una buena heurística puede hacer que un algoritmo explore menos estados sin modificar el problema que está resolviendo?**

---

## Recursos de apoyo

[Consultar contenido del subtema 2.4](../)

[Consultar recursos complementarios](../recursos/)

[Consultar comparación visual entre Greedy y A*](../imagenes/greedy-vs-a-star.png)

[Consultar notebook](../notebooks/busqueda-informada.ipynb)

---

[← Volver al subtema 2.4](../)
