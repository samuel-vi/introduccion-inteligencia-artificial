
# Recursos complementarios

## 2.5 Planificación automática

Los siguientes recursos permiten ampliar el estudio de la planificación clásica, la representación de acciones mediante precondiciones y efectos, y el modelo STRIPS.

---

## 1. Russell y Norvig

### Artificial Intelligence: A Modern Approach

Russell y Norvig presentan la planificación automática como un problema en el que un sistema debe encontrar una secuencia de acciones que transforme un estado inicial en uno que satisfaga un objetivo.

Los conceptos principales para este subtema son:

a) Estado inicial

b) Estado objetivo

c) Acciones

d) Precondiciones

e) Efectos

f) Plan

g) Planificación clásica

h) Representación mediante PDDL

**Referencia:**

Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson. Capítulo 11: Automated Planning.

---

## 2. STRIPS

### Stanford Research Institute Problem Solver

STRIPS constituye uno de los antecedentes fundamentales de la planificación automática.

Una acción puede representarse mediante:

```text
Acción
│
├── Precondiciones
├── Efectos positivos
└── Efectos negativos
```

En términos generales:

\[
a=
\langle
Precondiciones,
Efectos^+,
Efectos^-
\rangle
\]

Esta representación permite determinar:

a) Si una acción puede ejecutarse

b) Qué hechos pasan a ser verdaderos

c) Qué hechos dejan de ser verdaderos

d) Cómo cambia el estado del problema

**Referencia:**

Fikes, R. E., & Nilsson, N. J. (1971). STRIPS: A new approach to the application of theorem proving to problem solving. *Artificial Intelligence, 2*(3–4), 189–208.

---

## 3. Elementos de un problema de planificación

Un problema de planificación puede analizarse mediante:

| Elemento | Pregunta |
|---|---|
| **Estado inicial** | ¿Cómo comienza el problema? |
| **Objetivo** | ¿Qué condición debe alcanzarse? |
| **Acciones** | ¿Qué puede hacer el agente? |
| **Precondiciones** | ¿Qué debe cumplirse antes de actuar? |
| **Efectos positivos** | ¿Qué pasa a ser verdadero? |
| **Efectos negativos** | ¿Qué deja de ser verdadero? |
| **Plan** | ¿Qué secuencia de acciones alcanza el objetivo? |

---

## 4. Aplicabilidad de una acción

Una acción solamente puede ejecutarse cuando sus precondiciones se cumplen.

Ejemplo:

```text
Acción:
Recoger(Caja,A)

Precondiciones:
RobotEn(A)
CajaEn(A)
ManoLibre
```

Si:

```text
ManoLibre = falso
```

la acción no puede ejecutarse.

---

## 5. Actualización del estado

Después de ejecutar una acción:

```text
Estado nuevo
=
Estado actual
-
Efectos negativos
+
Efectos positivos
```

Por ejemplo:

```text
Estado inicial:

RobotEn(A)
CajaEn(A)
ManoLibre
```

Después de:

```text
Recoger(Caja,A)
```

se obtiene:

```text
RobotEn(A)
Sosteniendo(Caja)
```

---

## 6. Plan

Un plan es una secuencia ordenada de acciones:

\[
Plan=\langle a_1,a_2,\ldots,a_n\rangle
\]

que permite transformar:

```text
Estado inicial
      ↓
Estado objetivo
```

Ejemplo:

```text
Recoger(Caja,A)
        ↓
Mover(A,B)
        ↓
Depositar(Caja,B)
```

---

## 7. STRIPS y PDDL

STRIPS estableció varios de los principios fundamentales utilizados posteriormente en lenguajes de planificación.

Entre ellos se encuentra:

**PDDL — Planning Domain Definition Language**

PDDL permite separar:

```text
Dominio
↓
Tipos de acciones disponibles
```

de:

```text
Problema
↓
Estado inicial y objetivo específico
```

Para este curso utilizaremos principalmente la representación conceptual de STRIPS.

---

## 8. Preguntas para analizar un problema de planificación

Antes de construir un plan conviene responder:

a) ¿Cuál es el estado inicial?

b) ¿Cuál es el objetivo?

c) ¿Qué acciones existen?

d) ¿Qué precondiciones tiene cada acción?

e) ¿Qué efectos produce cada acción?

f) ¿Qué acciones pueden ejecutarse inicialmente?

g) ¿Qué acciones permiten acercarse al objetivo?

h) ¿Existe más de un plan posible?

i) ¿Todos los planes tienen la misma longitud o costo?

---

## 9. Planificación y búsqueda

La planificación puede verse también como un problema de búsqueda:

```text
Estado inicial
      ↓
Acciones aplicables
      ↓
Estados sucesores
      ↓
...
      ↓
Estado objetivo
```

La diferencia principal es que la representación de planificación describe explícitamente la estructura de las acciones mediante sus precondiciones y efectos.

---

## 10. Limitaciones de la planificación clásica

El modelo clásico supone condiciones simplificadas.

En problemas reales pueden aparecer:

```text
Incertidumbre
Percepción parcial
Acciones no deterministas
Tiempo
Recursos
Cambios en el entorno
```

Estas situaciones requieren modelos de planificación más avanzados.

---

## Recurso visual

[Planificación automática con STRIPS](../imagenes/planificacion-strips.png)

---

## Actividad relacionada

[Actividad: Planificación de acciones mediante STRIPS](../actividades/actividad-planificacion-strips.md)

---

## Referencias

Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.

Fikes, R. E., & Nilsson, N. J. (1971). STRIPS: A new approach to the application of theorem proving to problem solving. *Artificial Intelligence, 2*(3–4), 189–208.

---

[← Volver al subtema 2.5](../)
