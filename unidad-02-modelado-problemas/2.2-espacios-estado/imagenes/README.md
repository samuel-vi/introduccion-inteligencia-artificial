
# Recursos complementarios

## 2.2 Espacios de estado y operadores

Los siguientes recursos permiten ampliar los conceptos relacionados con la representación formal de problemas mediante estados, acciones, transiciones, objetivos y costos.

---

## 1. Russell y Norvig

### Artificial Intelligence: A Modern Approach

El capítulo dedicado a resolución de problemas mediante búsqueda presenta los elementos fundamentales para representar un problema:

a) Estado inicial

b) Acciones

c) Modelo de transición

d) Estado objetivo

e) Costos

A partir de estos componentes se construye el **espacio de estados** sobre el cual posteriormente operan los algoritmos de búsqueda.

**Referencia:**

Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.

---

## 2. Poole y Mackworth

### Artificial Intelligence: Foundations of Computational Agents

Este recurso aborda la representación de problemas mediante grafos y espacios de búsqueda, así como la relación entre estados, acciones y caminos.

[Consultar libro en línea](https://www.cs.ubc.ca/~poole/aibook/3e/html/ArtInt3e.html)

**Referencia:**

Poole, D. L., & Mackworth, A. K. (2023). *Artificial Intelligence: Foundations of Computational Agents* (3rd ed.). Cambridge University Press.

---

## 3. UC Berkeley CS188

### Introduction to Artificial Intelligence

El curso CS188 de la Universidad de California, Berkeley, contiene materiales relacionados con búsqueda, grafos, espacios de estados y agentes de resolución de problemas.

Resulta especialmente útil para observar cómo una representación formal puede implementarse posteriormente mediante algoritmos de búsqueda.

[Consultar CS188](https://inst.eecs.berkeley.edu/~cs188/)

---

## 4. AIMA Python

El repositorio **AIMA Python** contiene implementaciones de numerosos algoritmos presentados en *Artificial Intelligence: A Modern Approach*.

En los siguientes subtemas será útil para estudiar y comparar estrategias de búsqueda.

[Consultar AIMA Python](https://github.com/aimacode/aima-python)

---

## 5. Elementos que deben identificarse

Al analizar un problema de búsqueda conviene responder:

a) ¿Cuál es el estado inicial?

b) ¿Cómo se representa un estado?

c) ¿Qué acciones pueden ejecutarse?

d) ¿Qué estado produce cada acción?

e) ¿Cuál es la condición objetivo?

f) ¿Existen costos asociados a las acciones?

g) ¿Qué estados pueden alcanzarse?

h) ¿Qué secuencia de acciones constituye una solución?

---

## 6. Espacio de estados y árbol de búsqueda

Es importante distinguir:

```text
Espacio de estados
        ↓
Representación del problema

Árbol de búsqueda
        ↓
Exploración realizada por un algoritmo
```

El **espacio de estados** no depende de BFS, DFS, A* u otro algoritmo.

La estrategia de búsqueda determina cómo se explora dicho espacio.

---

## Recurso visual

[Espacio de estados y operadores](../imagenes/espacio-estados.png)

---

## Relación con el siguiente subtema

Una vez representado el problema mediante estados y operadores, la siguiente pregunta es:

> ¿En qué orden deben explorarse los estados?

Esta pregunta conduce al estudio de:

**2.3 Búsqueda no informada**

donde se analizarán principalmente:

```text
BFS
DFS
Búsqueda en profundidad iterativa
```

---

## Actividad relacionada

[Actividad: Representación de un problema mediante espacios de estado](../actividades/actividad-representacion-problema.md)

---

[← Volver al subtema 2.2](../)
