# Actividad 3.3 — Sistema experto simbólico con reglas de inferencia

## Propósito

Aplicar los conceptos de **base de hechos**, **base de reglas**, **encadenamiento hacia adelante**, **encadenamiento hacia atrás** y **traza de inferencia** mediante el diseño de un sistema experto simbólico sencillo para un dominio acotado.

## Instrucciones

Seleccione un problema sencillo en el que sea posible representar conocimiento mediante hechos y reglas.

Ejemplos de dominio:

a) Diagnóstico básico de fallas en un equipo

b) Sistema de riego

c) Control de acceso a una plataforma

d) Monitoreo básico mediante sensores

e) Otro dominio previamente justificado

## Requisitos mínimos

El sistema deberá incluir:

a) Al menos **5 hechos iniciales**

b) Al menos **5 reglas**

c) Al menos **2 reglas encadenadas**, es decir, que la conclusión de una regla pueda utilizarse como condición de otra

d) Al menos **una regla con variable**

e) Una ejecución mediante **forward chaining**

f) Una consulta mediante **backward chaining**

g) Una **traza de inferencia** para cada mecanismo

h) Una explicación breve de las conclusiones obtenidas

## Desarrollo

### 1. Definición del dominio

Explique en un párrafo:

a) Qué problema se desea resolver

b) Qué tipo de información utilizará el sistema

c) Qué tipo de conclusión espera obtener

### 2. Base de hechos

Liste los hechos iniciales.

Ejemplo:

```text
equipo_no_enciende
led_apagado
bateria_descargada
```

### 3. Base de reglas

Represente las reglas utilizando el formato:

```text
R1:
SI condición_1
Y condición_2
ENTONCES conclusión
```

### 4. Forward chaining

Ejecute el mecanismo de encadenamiento hacia adelante.

Documente:

a) Hechos iniciales

b) Regla aplicada en cada paso

c) Nuevo conocimiento obtenido

d) Estado final de la base de hechos

Puede presentar la traza en una tabla:

| Paso | Regla | Nuevo conocimiento |
|---|---|---|
| Inicial | — | ... |
| 1 | R1 | ... |
| 2 | R2 | ... |

### 5. Backward chaining

Seleccione una meta concreta.

Ejemplo:

```text
¿posible_falla_bateria?
```

Muestre:

a) Meta inicial

b) Regla utilizada para demostrarla

c) Subobjetivos generados

d) Hechos que permiten confirmar o rechazar cada subobjetivo

e) Resultado final

### 6. Variables y equiparación

Incluya al menos una regla general.

Ejemplo:

```text
SI Inscrito(X)
Y CuentaActiva(X)
ENTONCES PuedeAcceder(X)
```

Explique qué valor toma la variable durante la inferencia.

### 7. Comparación

Explique brevemente:

a) Qué diferencias observó entre forward chaining y backward chaining

b) Qué mecanismo considera más apropiado para el problema elegido y por qué

c) Qué información no pudo obtenerse con la base de conocimiento definida

### 8. Reflexión final

Responda:

> ¿Qué ventaja ofrece un sistema basado en reglas frente a una solución que únicamente almacena datos?

## Producto a entregar

Entregar un documento en **PDF o Markdown** de aproximadamente **3 a 5 páginas**, acompañado del código o notebook utilizado.

Debe incluir:

a) Descripción del problema

b) Base de hechos

c) Base de reglas

d) Traza de forward chaining

e) Traza de backward chaining

f) Regla con variable y ejemplo de equiparación

g) Comparación de ambos mecanismos

h) Reflexión final

## Criterios de evaluación

| Criterio | Porcentaje |
|---|---:|
| Definición del dominio y coherencia del problema | 10% |
| Base de hechos | 10% |
| Base de reglas | 20% |
| Forward chaining y traza | 20% |
| Backward chaining y traza | 20% |
| Variables y equiparación | 10% |
| Comparación y reflexión final | 10% |
| **Total** | **100%** |

## Relación con la Unidad 3

Esta actividad funciona como una primera versión del **sistema simbólico basado en reglas** de la Unidad 3. Más adelante podrá ampliarse incorporando razonamiento no monótono, incertidumbre u ontologías, según el desarrollo de los subtemas siguientes.
