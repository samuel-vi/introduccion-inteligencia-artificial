
# Actividad de aprendizaje

## Resolución de problemas de satisfacibilidad — SAT

## Propósito

Representar y analizar un problema sencillo mediante variables booleanas, cláusulas y fórmulas en forma normal conjuntiva (CNF), determinando si existe una asignación que satisfaga simultáneamente todas las restricciones.

---

## 1. Analiza una fórmula SAT

Considere:

\[
(A \lor B)
\land
(\neg A \lor C)
\land
(\neg B \lor C)
\]

Identifica:

a) Las variables proposicionales

b) Los literales positivos

c) Los literales negativos

d) Las cláusulas

e) El número total de cláusulas

---

## 2. Evalúa una asignación

Utiliza:

```text
A = Verdadero
B = Falso
C = Verdadero
```

Evalúa cada cláusula:

| Cláusula | Resultado |
|---|---|
| \(A \lor B\) | |
| \(\neg A \lor C\) | |
| \(\neg B \lor C\) | |

Después determina:

```text
Resultado de la fórmula =
```

Indica si es:

```text
SAT
```

o:

```text
UNSAT
```

---

## 3. Encuentra otras soluciones

Busca al menos **dos asignaciones adicionales** de:

```text
A
B
C
```

que satisfagan la fórmula.

Completa:

| A | B | C | ¿Satisface la fórmula? |
|---|---|---|---|
| | | | |
| | | | |

---

## 4. Analiza una fórmula no satisfacible

Considere:

\[
A \land \neg A
\]

Responde:

a) ¿Qué valor debería tener \(A\) para satisfacer el primer literal?

b) ¿Qué valor debería tener \(A\) para satisfacer el segundo?

c) ¿Por qué ambas condiciones no pueden cumplirse simultáneamente?

d) ¿La fórmula es SAT o UNSAT?

---

## 5. Representa un problema mediante SAT

Considere el siguiente problema:

> Se deben seleccionar recursos A y B. Debe seleccionarse al menos uno, pero no pueden seleccionarse ambos simultáneamente.

Define:

```text
A = Seleccionar recurso A
B = Seleccionar recurso B
```

Representa:

### Restricción 1

Debe seleccionarse al menos uno.

\[
____________________
\]

### Restricción 2

No pueden seleccionarse ambos.

\[
____________________
\]

Combina ambas restricciones mediante:

\[
____________________
\]

---

## 6. Tabla de verdad

Construye la tabla:

| A | B | \(A \lor B\) | \(\neg A \lor \neg B\) | Fórmula completa |
|---|---|---|---|---|
| F | F | | | |
| F | V | | | |
| V | F | | | |
| V | V | | | |

Identifica:

a) Qué asignaciones satisfacen la fórmula

b) Cuántas soluciones existen

c) Qué representa cada solución en el problema original

---

## 7. Construye tu propio problema SAT

Diseña un problema sencillo que contenga:

a) Al menos tres variables booleanas

b) Al menos tres restricciones

c) Una fórmula en CNF

Puedes utilizar situaciones como:

```text
Asignación de recursos
Selección de componentes
Configuración de sistemas
Asignación de horarios
Activación de servicios
```

Describe primero qué representa cada variable.

Ejemplo:

```text
A =
B =
C =
```

Después expresa las restricciones mediante cláusulas.

---

## 8. Determina satisfacibilidad

Para tu problema:

a) Propón una asignación

b) Evalúa cada cláusula

c) Determina si la fórmula es SAT

d) Si no lo es, intenta otra asignación

e) Identifica al menos una solución satisfactoria, si existe

---

## 9. Identifica cláusulas unitarias

Considere:

\[
(A \lor B)
\land
(\neg B)
\land
(B \lor C)
\]

Responde:

a) ¿Cuál es la cláusula unitaria?

b) ¿Qué valor obliga a asignar?

c) ¿Cómo afecta esa asignación a las otras cláusulas?

d) ¿Qué variable puede determinarse después?

---

## 10. Idea general de DPLL

Utilizando el problema anterior, describe el proceso mediante:

```text
Fórmula CNF
     ↓
Identificar cláusula unitaria
     ↓
Asignar valor
     ↓
Simplificar
     ↓
Seleccionar otra variable
     ↓
Continuar o retroceder
     ↓
SAT / UNSAT
```

No es necesario implementar completamente DPLL.

---

## 11. SAT y planificación

Explica brevemente cómo los siguientes elementos de un problema de planificación podrían representarse mediante variables proposicionales:

a) Estado inicial

b) Acciones

c) Precondiciones

d) Transiciones

e) Objetivo

Después explica con tus palabras la idea:

```text
Planificación
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

Russell y Norvig denominan **SATPLAN** a este enfoque.

---

## 12. Análisis

Responde:

a) ¿Qué significa que una fórmula sea satisfacible?

b) ¿Cuál es la diferencia entre SAT y UNSAT?

c) ¿Por qué todas las cláusulas de una fórmula CNF deben cumplirse simultáneamente?

d) ¿Qué ventaja tiene representar restricciones mediante variables booleanas?

e) ¿Por qué una codificación incorrecta puede producir una solución lógica que no sea válida en el problema real?

f) ¿Cómo se relaciona SAT con la planificación automática estudiada anteriormente?

---

## Producto esperado

Entrega un documento que incluya:

a) Análisis de la fórmula inicial

b) Evaluación de asignaciones

c) Ejemplo UNSAT

d) Problema de selección de recursos

e) Tabla de verdad

f) Problema SAT diseñado por el estudiante

g) Fórmula CNF

h) Solución satisfactoria

i) Análisis conceptual de DPLL

j) Relación entre SAT y planificación

k) Conclusión

---

## Criterios de evaluación

| Criterio | Valor |
|---|---:|
| Identificación correcta de variables, literales y cláusulas | 20% |
| Evaluación de fórmulas SAT/UNSAT | 20% |
| Formulación del problema propio | 25% |
| Representación correcta en CNF | 20% |
| Análisis y conclusión | 15% |

---

## Reflexión final

Responde en máximo **150 palabras**:

> **¿Por qué resolver un problema SAT depende tanto de la correcta formulación de las restricciones como del algoritmo utilizado para encontrar una asignación?**

---

## Referencias

Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.

Davis, M., Logemann, G., & Loveland, D. (1962). A machine program for theorem-proving. *Communications of the ACM, 5*(7), 394–397.

---

## Recursos de apoyo

[Consultar contenido del subtema 2.7](../)

[Consultar recursos complementarios](../recursos/)

[Consultar SAT, CNF y DPLL](../imagenes/sat-cnf-dpll.png)

---

[← Volver al subtema 2.7](../)
