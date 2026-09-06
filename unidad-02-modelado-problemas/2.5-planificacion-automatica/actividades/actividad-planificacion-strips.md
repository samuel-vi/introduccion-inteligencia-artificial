
# Actividad de aprendizaje

## Planificación de acciones mediante STRIPS

## Propósito

Representar un problema sencillo de planificación mediante **estado inicial, objetivo, acciones, precondiciones y efectos**, y construir una secuencia válida de acciones que permita alcanzar el objetivo.

---

## 1. Selección del problema

Selecciona uno de los siguientes escenarios:

a) Robot que transporta una caja entre dos ubicaciones

b) Robot móvil que debe desplazarse entre varias habitaciones

c) Brazo robótico que organiza objetos

d) Sistema que prepara una secuencia de tareas

e) Agente que debe trasladar recursos entre ubicaciones

También puedes proponer un problema equivalente.

---

## 2. Estado inicial

Describe los hechos que son verdaderos al comenzar el problema.

Ejemplo:

```text
RobotEn(A)
CajaEn(A)
ManoLibre
Conectado(A,B)
```

Identifica al menos **cuatro hechos iniciales**.

---

## 3. Estado objetivo

Define claramente la condición que debe alcanzarse.

Ejemplo:

```text
CajaEn(B)
```

El objetivo puede contener uno o varios hechos.

---

## 4. Definición de acciones

Define al menos **tres acciones**.

Para cada acción especifica:

```text
Acción:

Precondiciones:

Efectos positivos:

Efectos negativos:
```

Ejemplo:

```text
Acción:
Recoger(Caja,A)

Precondiciones:
RobotEn(A)
CajaEn(A)
ManoLibre

Efectos positivos:
Sosteniendo(Caja)

Efectos negativos:
CajaEn(A)
ManoLibre
```

---

## 5. Aplicabilidad de las acciones

Para cada acción responde:

a) ¿Puede ejecutarse en el estado inicial?

b) ¿Qué precondiciones deben cumplirse?

c) ¿Qué ocurriría si una precondición fuera falsa?

d) ¿Qué cambia después de ejecutar la acción?

---

## 6. Construcción del plan

Construye una secuencia de acciones que permita alcanzar el objetivo.

Representa el plan mediante:

```text
Acción 1
   ↓
Acción 2
   ↓
Acción 3
   ↓
...
   ↓
Objetivo
```

También puedes expresarlo como:

\[
Plan=\langle a_1,a_2,\ldots,a_n\rangle
\]

---

## 7. Evolución del estado

Describe cómo cambia el estado después de cada acción.

Utiliza una tabla como:

| Paso | Acción | Hechos verdaderos después de la acción |
|---|---|---|
| 0 | Estado inicial | |
| 1 | | |
| 2 | | |
| 3 | | |

Verifica que:

a) Cada acción cumpla sus precondiciones

b) Los efectos positivos se agreguen

c) Los efectos negativos se eliminen

d) El estado final satisfaga el objetivo

---

## 8. Plan alternativo

Determina si existe una secuencia diferente de acciones que también alcance el objetivo.

Si existe:

a) Escribe el segundo plan

b) Compara el número de acciones

c) Identifica cuál considerarías mejor

Si no existe, explica por qué.

---

## 9. Error en el plan

Modifica intencionalmente el orden de dos acciones.

Analiza:

a) ¿Qué precondición deja de cumplirse?

b) ¿En qué paso falla el plan?

c) ¿Por qué el orden de las acciones es importante?

---

## 10. Representación compacta

Selecciona una acción y represéntala mediante:

\[
a=
\langle
Precondiciones,
Efectos^+,
Efectos^-
\rangle
\]

Ejemplo:

```text
Mover(A,B)

Precondiciones:
{RobotEn(A), Conectado(A,B)}

Efectos positivos:
{RobotEn(B)}

Efectos negativos:
{RobotEn(A)}
```

---

## 11. Análisis

Responde:

a) ¿Qué diferencia existe entre una acción y un plan?

b) ¿Por qué las precondiciones son necesarias?

c) ¿Qué función cumplen los efectos negativos?

d) ¿Puede existir más de un plan válido para el mismo problema?

e) ¿Cómo se relaciona este problema con los espacios de estados?

f) ¿Qué limitaciones tendría esta representación en un entorno con incertidumbre?

---

## Producto esperado

Entrega un documento que incluya:

a) Descripción del problema

b) Estado inicial

c) Estado objetivo

d) Definición de las acciones

e) Precondiciones y efectos

f) Plan propuesto

g) Evolución del estado

h) Plan alternativo, si existe

i) Análisis de un plan incorrecto

j) Conclusión

---

## Criterios de evaluación

| Criterio | Valor |
|---|---:|
| Definición del estado inicial y objetivo | 20% |
| Representación correcta de acciones | 25% |
| Precondiciones y efectos | 20% |
| Construcción del plan | 20% |
| Análisis y justificación | 15% |

---

## Reflexión final

Responde en máximo **150 palabras**:

> **¿Por qué un planificador necesita conocer no solo qué acciones existen, sino también bajo qué condiciones pueden ejecutarse y qué efectos producen?**

---

## Recursos de apoyo

[Consultar contenido del subtema 2.5](../)

[Consultar recursos complementarios](../recursos/)

[Consultar planificación automática con STRIPS](../imagenes/planificacion-strips.png)

---

[← Volver al subtema 2.5](../)
