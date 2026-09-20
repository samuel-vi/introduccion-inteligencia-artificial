# Actividad 3.4 — Análisis de conocimiento revisable

## Propósito

Analizar cómo cambia una conclusión cuando aparece nueva información, identificando **reglas por defecto**, **excepciones**, **conocimiento incompleto** y diferencias entre **mundo abierto** y **mundo cerrado**.

## Instrucciones

Seleccione uno de los siguientes dominios:

a) Acceso de estudiantes a una plataforma

b) Sistema de riego

c) Diagnóstico básico de un equipo

d) Otro dominio sencillo previamente justificado

## Desarrollo

### 1. Situación inicial

Describa brevemente el problema e identifique los hechos disponibles.

Ejemplo:

```text
Inscrito(Ana)
CuentaActiva(Ana)
```

### 2. Regla general

Formule una regla que permita obtener una conclusión inicial.

Ejemplo:

```text
SI Inscrito(X)
Y CuentaActiva(X)
ENTONCES PuedeAcceder(X)
```

### 3. Conclusión inicial

Indique la conclusión obtenida con la información disponible.

```text
PuedeAcceder(Ana)
```

### 4. Nueva información

Agregue un nuevo hecho que funcione como excepción o modifique el contexto.

Ejemplo:

```text
CuentaBloqueada(Ana)
```

### 5. Revisión de la conclusión

Explique si la conclusión inicial:

a) Se mantiene

b) Se modifica

c) Se retracta

Justifique la decisión.

### 6. Comparación monotónica y no monotónica

Analice el mismo caso bajo ambos enfoques.

| Aspecto | Monotónico | No monotónico |
|---|---|---|
| Conclusión inicial |  |  |
| Nueva información |  |  |
| ¿La conclusión cambia? |  |  |
| Justificación |  |  |

### 7. Conocimiento incompleto

Introduzca al menos un hecho cuyo valor sea desconocido.

Ejemplo:

```text
CuentaActiva(Carlos) = desconocido
```

Explique por qué **desconocido** no debe confundirse automáticamente con **falso**.

### 8. Mundo abierto y mundo cerrado

Utilice una consulta que no pueda responderse directamente con la información disponible.

Ejemplo:

```text
¿Inscrito(Carlos)?
```

Explique el resultado bajo:

a) Supuesto de mundo abierto

b) Supuesto de mundo cerrado

### 9. Regla por defecto y excepción

Formule:

a) Una regla por defecto

b) Una excepción

Ejemplo:

```text
Regla por defecto:
Normalmente, si SueloSeco → ActivarRiego

Excepción:
LluviaInminente → NoActivarRiego
```

### 10. Reflexión final

Responda:

a) ¿Qué diferencia encontró entre una conclusión definitiva y una provisional?

b) ¿Qué información provocó la revisión de la conclusión?

c) ¿Por qué es importante distinguir entre falso y desconocido?

d) ¿Qué limitación tendría este enfoque para representar grados de confianza o probabilidad?

## Producto a entregar

Entregar un documento en **PDF o Markdown** de aproximadamente **3 a 5 páginas**.

Debe incluir:

a) Descripción del dominio

b) Hechos iniciales

c) Regla general

d) Conclusión inicial

e) Nueva información

f) Conclusión revisada

g) Comparación monotónica vs. no monotónica

h) Ejemplo de conocimiento desconocido

i) Comparación mundo abierto vs. mundo cerrado

j) Reflexión final

Puede apoyarse en el notebook del subtema para mostrar el comportamiento de las reglas.

## Criterios de evaluación

| Criterio | Porcentaje |
|---|---:|
| Definición del dominio y hechos iniciales | 10% |
| Regla general y conclusión inicial | 15% |
| Excepción y revisión de la conclusión | 20% |
| Comparación monotónica vs. no monotónica | 20% |
| Conocimiento incompleto | 10% |
| Mundo abierto vs. mundo cerrado | 15% |
| Reflexión final | 10% |
| **Total** | **100%** |

## Relación con la Unidad 3

La actividad amplía el sistema simbólico desarrollado en 3.3 al incorporar conocimiento revisable, excepciones y ausencia de información. Estos conceptos preparan el estudio de **ontologías en la Web Semántica y grafos de conocimiento** del subtema 3.5.
