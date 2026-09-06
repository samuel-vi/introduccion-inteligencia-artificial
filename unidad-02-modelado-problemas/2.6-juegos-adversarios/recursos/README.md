# Recursos complementarios

## 2.6 Juegos y adversarios

Los siguientes recursos permiten ampliar el estudio de la búsqueda adversarial, el algoritmo minimax y la poda alpha-beta.

---

## 1. Russell y Norvig

### Artificial Intelligence: A Modern Approach

Russell y Norvig presentan la búsqueda adversarial como un problema en el que la decisión de un agente depende también de las decisiones de un oponente racional.

Los conceptos principales para este subtema son:

a) Estados MAX y MIN

b) Árbol de juego

c) Utilidad

d) Minimax

e) Poda alpha-beta

f) Función de evaluación

g) Profundidad limitada

**Referencia:**

Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson. Capítulo 6: *Adversarial Search and Games*.

---

## 2. Minimax

El principio general de minimax es:

```text
MAX
↓
Elige la acción que maximiza el resultado

MIN
↓
Elige la respuesta que minimiza la utilidad de MAX
```

Formalmente:

\[
MINIMAX(s)=
\begin{cases}
UTILITY(s) & \text{si }s\text{ es terminal}\\
\max MINIMAX(Result(s,a)) & \text{si juega MAX}\\
\min MINIMAX(Result(s,a)) & \text{si juega MIN}
\end{cases}
\]

Este procedimiento permite tomar decisiones óptimas bajo el supuesto de que ambos jugadores actúan racionalmente.

---

## 3. Función de utilidad

Los estados terminales reciben un valor numérico que representa el resultado del juego.

Ejemplo:

```text
Victoria = +1
Empate   =  0
Derrota  = -1
```

o bien:

```text
Victoria = +10
Empate   =   0
Derrota  = -10
```

Lo importante es que:

a) Valores altos favorecen a MAX

b) Valores bajos favorecen a MIN

---

## 4. Poda alpha-beta

La poda alpha-beta evita explorar ramas del árbol que ya no pueden cambiar la decisión final.

Mantiene dos límites:

\[
\alpha
\]

Mejor valor que MAX puede garantizar.

\[
\beta
\]

Mejor valor que MIN puede garantizar.

Cuando:

\[
\alpha \geq \beta
\]

puede detenerse la exploración de la rama actual.

---

## 5. Diferencia entre minimax y alpha-beta

| Característica | Minimax | Alpha-beta |
|---|---|---|
| Considera MAX y MIN | Sí | Sí |
| Produce la decisión minimax | Sí | Sí |
| Explora ramas innecesarias | Puede hacerlo | Las poda cuando es posible |
| Eficiencia | Menor | Mayor |
| Influencia del orden de exploración | Menor | Mayor |

La idea clave es:

> Alpha-beta no cambia la decisión, solo reduce el número de nodos que deben evaluarse.

---

## 6. Árbol de juego

Un árbol de juego representa:

```text
Nodo     = Estado del juego
Arista   = Acción posible
Hoja     = Estado terminal
Valor    = Utilidad
```

Ejemplo:

```text
                 MAX
              /       \
             A         B
             ↓         ↓
            MIN       MIN
           /   \     /   \
          4     7   2     9
```

En este caso:

```text
MIN(A) = 4
MIN(B) = 2
MAX(4,2) = 4
```

---

## 7. Búsqueda con profundidad limitada

En juegos grandes no suele ser posible explorar todo el árbol.

Una solución práctica es:

```text
Limitar profundidad
        ↓
Evaluar estados no terminales
        ↓
Usar función de evaluación
```

La función de evaluación aproxima la utilidad de una posición intermedia.

---

## 8. Preguntas para analizar un juego adversarial

Antes de aplicar minimax conviene responder:

a) ¿Quién es MAX?

b) ¿Quién es MIN?

c) ¿Cuál es el estado inicial?

d) ¿Qué acciones puede realizar cada jugador?

e) ¿Qué estados son terminales?

f) ¿Cómo se calcula la utilidad?

g) ¿Qué profundidad es razonable explorar?

h) ¿Qué ramas podrían podarse?

---

## 9. Fuentes adicionales

### Knuth y Moore

Este trabajo clásico analiza formalmente la poda alpha-beta y su comportamiento computacional.

**Referencia:**

Knuth, D. E., & Moore, R. W. (1975). An analysis of alpha-beta pruning. *Artificial Intelligence, 6*(4), 293–326.

---

## 10. Relación con subtemas anteriores

```text
BFS / DFS / IDS
        ↓
Exploración sin oponente

Greedy / A*
        ↓
Exploración con heurística

Minimax / Alpha-beta
        ↓
Exploración con oponente
```

La diferencia esencial es que ahora el resultado depende de las decisiones de otro agente.

---

## Recurso visual

[Minimax y poda alpha-beta](../imagenes/minimax-alpha-beta.png)

---

## Notebook relacionado

[Implementación de minimax y poda alpha-beta en Python](../notebooks/minimax-alpha-beta.ipynb)

---

## Actividad relacionada

[Actividad: Comparación de minimax y poda alpha-beta](../actividades/actividad-minimax-alpha-beta.md)

---

[← Volver al subtema 2.6](../)
