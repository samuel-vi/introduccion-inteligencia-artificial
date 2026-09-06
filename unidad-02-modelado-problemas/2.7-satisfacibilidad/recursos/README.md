
# Recursos complementarios

## 2.7 Satisfacibilidad — SAT

Los siguientes recursos permiten ampliar el estudio de la satisfacibilidad booleana, las fórmulas en CNF, el algoritmo DPLL y su relación con problemas de planificación.

---

## 1. Russell y Norvig

### Artificial Intelligence: A Modern Approach

Russell y Norvig presentan SAT como un problema fundamental de lógica proposicional y muestran cómo puede utilizarse para resolver problemas de razonamiento y planificación.

Los conceptos principales para este subtema son:

a) Variables proposicionales

b) Literales

c) Cláusulas

d) Forma normal conjuntiva (CNF)

e) Satisfacibilidad

f) DPLL

g) Propagación unitaria

h) Literales puros

i) SATPLAN

**Referencia:**

Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson. Capítulo 7: *Logical Agents*.

---

## 2. Forma normal conjuntiva — CNF

Una fórmula en CNF tiene la forma:

\[
C_1 \land C_2 \land \cdots \land C_n
\]

donde cada \(C_i\) representa una cláusula.

Ejemplo:

\[
(A \lor B)
\land
(\neg A \lor C)
\land
(\neg B \lor C)
\]

Para que la fórmula sea satisfacible:

```text
Todas las cláusulas
        ↓
Deben ser verdaderas
```

---

## 3. SAT y UNSAT

### SAT

Existe al menos una asignación que satisface todas las cláusulas.

Ejemplo:

\[
(A \lor B)\land(\neg A \lor C)
\]

puede ser satisfacible.

### UNSAT

No existe ninguna asignación que satisfaga la fórmula.

Ejemplo:

\[
A\land\neg A
\]

es imposible de satisfacer.

---

## 4. DPLL

DPLL es uno de los algoritmos clásicos para resolver problemas SAT.

Su funcionamiento conceptual incluye:

```text
Fórmula CNF
     ↓
Propagación unitaria
     ↓
Literales puros
     ↓
Asignar una variable
     ↓
Simplificar
     ↓
Retroceder si es necesario
```

El proceso continúa hasta obtener:

```text
SAT
```

o:

```text
UNSAT
```

---

## 5. Propagación unitaria

Una cláusula unitaria contiene un solo literal pendiente.

Ejemplo:

\[
\neg C
\]

obliga a:

\[
C=F
\]

Esta asignación puede simplificar otras cláusulas y generar nuevas cláusulas unitarias.

---

## 6. Literal puro

Un literal es puro cuando aparece únicamente con una polaridad dentro de la fórmula.

Por ejemplo, si:

```text
A
```

aparece en varias cláusulas pero:

```text
¬A
```

no aparece en ninguna, entonces \(A\) puede asignarse como verdadero sin hacer falsa una cláusula por esa variable.

---

## 7. SAT como problema de restricciones

SAT puede interpretarse como:

```text
Variables booleanas
        +
Restricciones lógicas
        ↓
Buscar una asignación válida
```

Ejemplo:

```text
A = Seleccionar recurso A
B = Seleccionar recurso B
```

Restricción:

\[
A\lor B
\]

significa:

> Debe seleccionarse al menos uno.

Mientras que:

\[
\neg A\lor\neg B
\]

significa:

> No pueden seleccionarse ambos simultáneamente.

---

## 8. SAT y planificación

Un problema de planificación puede codificarse mediante proposiciones que representen:

```text
Estado inicial
Acciones
Transiciones
Objetivo
```

La estructura general es:

```text
Problema de planificación
        ↓
Codificación proposicional
        ↓
CNF
        ↓
SAT Solver
        ↓
Modelo
        ↓
Plan
```

Russell y Norvig denominan **SATPLAN** a este procedimiento.

---

## 9. Importancia de la codificación

La calidad de la solución depende de representar correctamente todas las restricciones.

Una codificación incompleta puede permitir modelos lógicamente válidos pero incompatibles con el problema real.

Por ello deben representarse correctamente:

a) Estados posibles

b) Precondiciones

c) Transiciones

d) Acciones permitidas

e) Exclusión de acciones incompatibles

f) Objetivo

---

## 10. Preguntas para analizar un problema SAT

Antes de resolverlo conviene identificar:

a) ¿Cuáles son las variables booleanas?

b) ¿Qué representa cada variable?

c) ¿Cuáles son las restricciones?

d) ¿Cómo se expresan mediante cláusulas?

e) ¿La fórmula está en CNF?

f) ¿Existen cláusulas unitarias?

g) ¿Existen literales puros?

h) ¿Qué asignaciones pueden descartarse?

i) ¿Existe al menos un modelo satisfactorio?

---

## 11. Relación con la Unidad 3

En este subtema utilizamos únicamente la lógica proposicional necesaria para comprender SAT.

En la siguiente unidad se estudiarán con mayor profundidad:

```text
Lógica proposicional
Lógica de primer orden
Inferencia
Representación del conocimiento
```

---

## Recurso visual

[SAT, CNF y DPLL](../imagenes/sat-cnf-dpll.png)

---

## Actividad relacionada

[Actividad: Resolución de problemas de satisfacibilidad](../actividades/actividad-sat.md)

---

## Referencias

Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.

Davis, M., Logemann, G., & Loveland, D. (1962). A machine program for theorem-proving. *Communications of the ACM, 5*(7), 394–397.

---

[← Volver al subtema 2.7](../)
