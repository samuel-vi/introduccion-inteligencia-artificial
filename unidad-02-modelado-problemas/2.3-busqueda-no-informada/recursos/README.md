# Recursos complementarios

## 2.3 Búsqueda no informada

Los siguientes recursos permiten ampliar el estudio de las estrategias de búsqueda que exploran un espacio de estados sin utilizar información heurística.

---

## 1. Russell y Norvig

### Artificial Intelligence: A Modern Approach

Russell y Norvig presentan la búsqueda no informada como el conjunto de estrategias que utilizan únicamente la información contenida en la definición del problema.

Entre las estrategias principales se encuentran:

a) Breadth-First Search (BFS)

b) Depth-First Search (DFS)

c) Depth-Limited Search

d) Iterative Deepening Search (IDS)

El análisis de estas estrategias considera:

```text
Completitud
Optimalidad
Tiempo
Espacio
```

**Referencia:**

Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.

---

## 2. Poole y Mackworth

### Artificial Intelligence: Foundations of Computational Agents

Este recurso permite estudiar búsqueda sobre grafos y espacios de estados, incluyendo diferentes formas de administrar la frontera de búsqueda.

[Consultar libro en línea](https://www.cs.ubc.ca/~poole/aibook/3e/html/ArtInt3e.html)

**Referencia:**

Poole, D. L., & Mackworth, A. K. (2023). *Artificial Intelligence: Foundations of Computational Agents* (3rd ed.). Cambridge University Press.

---

## 3. UC Berkeley CS188

### Search

El curso CS188 contiene materiales y ejercicios relacionados con búsqueda, estructuras de frontera y exploración de espacios de estados.

Resulta útil para observar la aplicación de los algoritmos en problemas como:

```text
Navegación
Laberintos
Rutas
Agentes
```

[Consultar CS188](https://inst.eecs.berkeley.edu/~cs188/)

---

## 4. AIMA Python

El repositorio AIMA Python contiene implementaciones asociadas al libro de Russell y Norvig.

Puede utilizarse como recurso de consulta para comparar diferentes estrategias de búsqueda.

[Consultar AIMA Python](https://github.com/aimacode/aima-python)

---

## 5. Estructuras de datos utilizadas

### BFS

Utiliza normalmente una:

```text
Cola FIFO
```

```text
Primero en entrar
        ↓
Primero en salir
```

### DFS

Utiliza normalmente una:

```text
Pila LIFO
```

```text
Último en entrar
        ↓
Primero en salir
```

### IDS

Ejecuta repetidamente:

```text
DFS limitada
```

con límites crecientes.

---

## 6. Criterios para comparar algoritmos

Al analizar una estrategia de búsqueda conviene responder:

a) ¿Es completa?

b) ¿Es óptima?

c) ¿Cuántos estados explora?

d) ¿Cuánta memoria utiliza?

e) ¿Qué estructura de datos requiere?

f) ¿Puede quedar atrapada en ciclos?

g) ¿Qué ocurre cuando aumenta la profundidad?

h) ¿Qué ocurre cuando aumenta el factor de ramificación?

---

## 7. Notación utilizada

```text
b = Factor de ramificación

d = Profundidad de la solución más cercana

m = Profundidad máxima del espacio

l = Límite de profundidad
```

Estas variables permiten analizar el crecimiento del costo computacional de los algoritmos.

---

## 8. Comparación conceptual

| Característica | BFS | DFS | IDS |
|---|---|---|---|
| Exploración | Por niveles | En profundidad | Profundidades crecientes |
| Estructura | Cola | Pila | DFS limitada |
| Memoria | Alta | Baja | Baja |
| Óptima con costos unitarios | Sí | No | Sí |
| Riesgo principal | Consumo de memoria | Ciclos o gran profundidad | Repetición de estados |

---

## Recurso visual

[Comparación de BFS, DFS e IDS](../imagenes/comparacion-bfs-dfs-ids.png)

---

## Notebook relacionado

[Implementación de BFS, DFS e IDS en Python](../notebooks/busqueda-no-informada.ipynb)

---

## Relación con el siguiente subtema

La búsqueda no informada no sabe qué estados parecen más prometedores.

En el siguiente subtema se incorporará información adicional mediante una:

```text
Función heurística
```

Esto conduce al estudio de:

**2.4 Búsqueda informada**

donde se analizarán:

```text
Greedy Best-First Search
A*
Heurísticas admisibles
```

---

## Actividad relacionada

[Actividad: Comparación de estrategias de búsqueda](../actividades/actividad-comparacion-busquedas.md)

---

[← Volver al subtema 2.3](../)
