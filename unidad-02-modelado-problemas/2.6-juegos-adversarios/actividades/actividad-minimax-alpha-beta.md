
# Actividad de aprendizaje

## Comparación de minimax y poda alpha-beta

## Propósito

Aplicar los algoritmos **minimax** y **poda alpha-beta** sobre un mismo árbol de juego para comparar la decisión obtenida, el número de nodos evaluados y el efecto del orden de exploración.

---

## 1. Ejecuta el notebook

Utiliza:

[Implementación de minimax y poda alpha-beta](../notebooks/minimax-alpha-beta.ipynb)

Ejecuta todas las celdas y verifica el ejemplo:

```text
                 MAX
              /       \
             A         B
             ↓         ↓
            MIN       MIN
           /   \     /   \
          4     7   2     9
```

---

## 2. Calcula minimax manualmente

Completa:

```text
MIN(A) =

MIN(B) =

MAX(____, ____) =
```

Indica:

```text
Mejor acción para MAX =
Valor minimax =
```

Explica por qué MAX debe considerar la mejor respuesta posible de MIN.

---

## 3. Identifica la poda alpha-beta

Utilizando el mismo árbol, determina:

```text
Después de evaluar A:

α =
```

Después de evaluar el primer hijo de B:

```text
β =
```

Comprueba si:

\[
\beta \leq \alpha
\]

Responde:

a) ¿Qué nodo puede podarse?

b) ¿Por qué su valor ya no puede cambiar la decisión de MAX?

c) ¿La poda modifica el valor minimax?

---

## 4. Comparación experimental

Completa la siguiente tabla con los resultados del notebook:

| Algoritmo | Valor final | Mejor acción | Nodos evaluados | Podas |
|---|---:|---|---:|---:|
| Minimax | | | | |
| Alpha-beta | | | | |

Analiza:

a) ¿Ambos algoritmos obtienen la misma decisión?

b) ¿Cuál evalúa menos nodos?

c) ¿Qué ventaja práctica representa la poda?

---

## 5. Cambia los valores terminales

Modifica el árbol.

Por ejemplo:

```text
A = [3, 8]
B = [5, 6]
```

Ejecuta nuevamente ambos algoritmos.

Registra:

| Aspecto | Minimax | Alpha-beta |
|---|---|---|
| Valor final | | |
| Mejor acción | | |
| Nodos evaluados | | |
| Podas | | |

Explica qué cambió respecto al ejemplo original.

---

## 6. Modifica el orden de exploración

Compara:

```text
A → B
```

con:

```text
B → A
```

Registra:

| Orden | Valor final | Nodos evaluados | Podas |
|---|---:|---:|---:|
| A → B | | | |
| B → A | | | |

Responde:

a) ¿La decisión final cambia?

b) ¿El número de nodos evaluados cambia?

c) ¿Por qué el orden de exploración es importante para alpha-beta?

---

## 7. Construye un nuevo árbol

Diseña un árbol de juego con:

a) Al menos tres niveles de decisión

b) Estados MAX y MIN alternados

c) Al menos ocho valores terminales

d) Dos o más decisiones posibles desde la raíz

Representa el árbol mediante un diagrama.

---

## 8. Aplica minimax

Sobre el árbol construido:

a) Calcula los valores desde las hojas hacia la raíz

b) Identifica qué nodos corresponden a MAX

c) Identifica qué nodos corresponden a MIN

d) Determina el valor minimax

e) Identifica la mejor acción para MAX

---

## 9. Aplica alpha-beta

Utiliza el mismo árbol y:

a) Registra los valores de \(\alpha\)

b) Registra los valores de \(\beta\)

c) Identifica las ramas que pueden podarse

d) Cuenta los nodos evaluados

e) Compara el resultado con minimax

---

## 10. Análisis

Responde:

a) ¿Por qué minimax supone que MIN también juega de forma óptima?

b) ¿Qué diferencia existe entre buscar un camino y buscar una estrategia?

c) ¿Qué representa la función de utilidad?

d) ¿Por qué alpha-beta obtiene la misma decisión que minimax?

e) ¿Qué ocurre si las mejores jugadas se exploran primero?

f) ¿Qué limitación aparece cuando el árbol de juego es muy profundo?

g) ¿Por qué en juegos complejos se utilizan funciones de evaluación?

---

## Producto esperado

Entrega un documento o notebook que incluya:

a) Resolución manual del ejemplo original

b) Comparación minimax vs. alpha-beta

c) Modificación de valores terminales

d) Experimento con el orden de exploración

e) Nuevo árbol de juego

f) Aplicación de minimax

g) Aplicación de alpha-beta

h) Evidencia de las podas

i) Análisis de resultados

j) Conclusión

---

## Criterios de evaluación

| Criterio | Valor |
|---|---:|
| Aplicación correcta de minimax | 25% |
| Aplicación correcta de alpha-beta | 25% |
| Construcción del árbol de juego | 15% |
| Comparación experimental | 20% |
| Análisis y conclusión | 15% |

---

## Reflexión final

Responde en máximo **150 palabras**:

> **¿Por qué una técnica que elimina ramas del árbol puede encontrar exactamente la misma decisión que un algoritmo que explora todos los estados?**

---

## Recursos de apoyo

[Consultar contenido del subtema 2.6](../)

[Consultar recursos complementarios](../recursos/)

[Consultar minimax y poda alpha-beta](../imagenes/minimax-alpha-beta.png)

[Consultar notebook](../notebooks/minimax-alpha-beta.ipynb)

---

[← Volver al subtema 2.6](../)
