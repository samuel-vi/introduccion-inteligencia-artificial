# Recursos complementarios

## 2.4 Búsqueda informada

Los siguientes recursos permiten ampliar el estudio de las estrategias de búsqueda que utilizan información heurística para orientar la exploración del espacio de estados.

---

## 1. Russell y Norvig

### Artificial Intelligence: A Modern Approach

Russell y Norvig presentan la búsqueda informada mediante funciones de evaluación que permiten determinar qué nodo parece más prometedor.

Los conceptos principales para este subtema son:

a) Función heurística \(h(n)\)

b) Greedy Best-First Search

c) Algoritmo A*

d) Función \(f(n)=g(n)+h(n)\)

e) Heurísticas admisibles

f) Heurísticas consistentes

g) Calidad de una heurística

**Referencia:**

Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.

---

## 2. Poole y Mackworth

### Artificial Intelligence: Foundations of Computational Agents

Este recurso aborda búsqueda heurística, búsqueda por menor costo y funciones que permiten orientar la exploración de espacios de estados.

[Consultar libro en línea](https://www.cs.ubc.ca/~poole/aibook/3e/html/ArtInt3e.html)

**Referencia:**

Poole, D. L., & Mackworth, A. K. (2023). *Artificial Intelligence: Foundations of Computational Agents* (3rd ed.). Cambridge University Press.

---

## 3. UC Berkeley CS188

### Search

El curso CS188 presenta problemas de búsqueda y permite estudiar la diferencia entre estrategias no informadas e informadas.

Es particularmente útil para comprender la relación entre:

```text
Costo recorrido
+
Heurística
+
Selección del siguiente nodo
```

[Consultar CS188](https://inst.eecs.berkeley.edu/~cs188/)

---

## 4. AIMA Python

El repositorio AIMA Python contiene implementaciones de los algoritmos asociados con *Artificial Intelligence: A Modern Approach*.

Puede utilizarse como referencia para analizar la estructura computacional de diferentes estrategias de búsqueda.

[Consultar AIMA Python](https://github.com/aimacode/aima-python)

---

## 5. Funciones fundamentales

### Heurística

\[
h(n)=\text{estimación del costo restante}
\]

### Greedy Best-First Search

\[
f(n)=h(n)
\]

Selecciona el nodo que aparentemente se encuentra más cerca del objetivo.

### A*

\[
f(n)=g(n)+h(n)
\]

donde:

\[
g(n)=\text{costo acumulado desde el estado inicial}
\]

y:

\[
h(n)=\text{estimación del costo restante}
\]

---

## 6. Heurística admisible

Una heurística es admisible cuando:

\[
h(n)\leq h^*(n)
\]

donde \(h^*(n)\) representa el costo real óptimo desde el estado \(n\) hasta el objetivo.

En términos simples:

> Una heurística admisible nunca sobreestima el costo mínimo real.

---

## 7. Heurística consistente

Una heurística consistente cumple:

\[
h(n)\leq c(n,a,n')+h(n')
\]

Esta propiedad mantiene coherencia entre estados consecutivos.

Como guía conceptual:

```text
Admisible
↓
No sobreestima

Consistente
↓
Respeta la relación de costo entre estados consecutivos
```

---

## 8. Preguntas para analizar una heurística

Al diseñar o evaluar una función heurística conviene responder:

a) ¿Qué información utiliza?

b) ¿Qué representa su valor?

c) ¿Puede sobreestimar el costo real?

d) ¿Qué tan cerca está de los costos reales?

e) ¿Es fácil de calcular?

f) ¿Reduce el número de estados explorados?

g) ¿Produce siempre los mismos resultados?

h) ¿Cómo afecta la calidad de la solución?

---

## 9. Greedy y A*

La diferencia fundamental puede resumirse mediante:

```text
GREEDY
   ↓
h(n)
   ↓
Considera principalmente
lo que parece faltar
```

```text
A*
   ↓
g(n) + h(n)
   ↓
Considera lo recorrido
y lo que estima que falta
```

| Característica | Greedy | A* |
|---|---|---|
| Utiliza heurística | Sí | Sí |
| Considera costo acumulado | No | Sí |
| Función | \(h(n)\) | \(g(n)+h(n)\) |
| Optimalidad | No garantizada | Bajo condiciones adecuadas |
| Riesgo principal | Decisiones voraces | Consumo de memoria |

---

## 10. Ejemplos de heurísticas

### Rutas

```text
Distancia en línea recta
hasta el destino
```

### 8-puzzle

```text
Número de piezas fuera de posición
```

o:

```text
Suma de distancias Manhattan
```

Estos ejemplos muestran que una heurística depende de las características del problema.

---

## Recurso visual

[Comparación entre Greedy y A*](../imagenes/greedy-vs-a-star.png)

---

## Notebook relacionado

[Implementación de Greedy y A* en Python](../notebooks/busqueda-informada.ipynb)

---

## Relación con los subtemas anteriores

```text
BFS / DFS / IDS
        ↓
Búsqueda no informada

Greedy / A*
        ↓
Búsqueda informada
        ↓
Utilización de heurísticas
```

La diferencia principal es que la búsqueda informada utiliza conocimiento adicional para orientar la exploración.

---

## Actividad relacionada

[Actividad: Comparación de búsqueda informada](../actividades/actividad-comparacion-busqueda-informada.md)

---

[← Volver al subtema 2.4](../)
