
# Actividad integradora — Unidad 3

## Representación del conocimiento y razonamiento

### Propósito

Integrar los contenidos de la Unidad 3 mediante el diseño y documentación de un **sistema simbólico para un dominio acotado**, capaz de representar conocimiento, aplicar reglas de inferencia, considerar conocimiento incompleto o excepciones y organizar parte del dominio mediante una ontología o un grafo de conocimiento.

La actividad recupera los productos previstos para la unidad: **sistema simbólico documentado, ontología/grafo y reporte técnico**.

---

## Dominio de trabajo

Seleccione un dominio suficientemente acotado para poder representarlo y probarlo durante la actividad.

Puede trabajar, por ejemplo, con:

a) Diagnóstico básico de fallas en equipo de cómputo o eléctrico

b) Acceso de estudiantes a servicios académicos

c) Recomendación de acciones en un sistema de riego

d) Clasificación y consulta de recursos académicos

e) Otro dominio aprobado por el docente

El dominio debe permitir representar **hechos, reglas, relaciones, excepciones y consultas**.

---

## 1. Delimitación del problema

Describa brevemente:

a) Contexto del dominio

b) Problema que resolverá el sistema

c) Usuarios o actores involucrados

d) Alcance de la solución

e) Qué tipo de conclusiones deberá producir

---

## 2. Representación formal del conocimiento

Defina los elementos principales del dominio.

Incluya como mínimo:

a) 8 hechos o afirmaciones iniciales

b) 6 reglas

c) Al menos 3 relaciones entre entidades

d) Al menos una regla que utilice variables

e) Al menos una consulta que el sistema pueda responder

Ejemplo:

```text
equipo_no_enciende
led_apagado
bateria_descargada
```

```text
SI equipo_no_enciende
Y led_apagado
ENTONCES revisar_alimentacion
```

---

## 3. Sistema de inferencia

Implemente o represente un mecanismo de:

a) Encadenamiento hacia adelante

**o**

b) Encadenamiento hacia atrás

Deberá mostrar una **traza de inferencia** en la que se observe:

```text
Hechos iniciales
      ↓
Reglas activadas
      ↓
Conclusiones intermedias
      ↓
Conclusión final
```

Puede implementarlo con Python, pseudocódigo o una herramienta lógica apropiada, siempre que el mecanismo quede claramente explicado.

---

## 4. Conocimiento incompleto, regla por defecto o excepción

Incorpore al menos una situación en la que la conclusión inicial pueda depender de información incompleta o de una excepción.

Ejemplo:

```text
Conclusión inicial:
PuedeAcceder(Ana)

Nueva información:
CuentaBloqueada(Ana)

Conclusión revisada:
NoPuedeAcceder(Ana)
```

Explique:

a) Qué información se agregó

b) Qué conclusión cambió

c) Por qué debe revisarse

d) Si la situación se interpreta mejor mediante mundo abierto o mundo cerrado

---

## 5. Ontología o grafo de conocimiento

Construya una representación estructurada del dominio mediante una **ontología o un grafo pequeño de conocimiento**.

Debe incluir como mínimo:

a) 5 tipos de entidades o clases

b) 8 instancias

c) 5 tipos de relaciones

d) 15 triples o afirmaciones equivalentes

e) Una representación visual del grafo o la ontología

Ejemplo:

```text
Ana ── cursa ──► IntroduccionIA
IntroduccionIA ── formaParteDe ──► MSC
MSC ── perteneceA ──► TecNM
```

---

## 6. Consultas

Formule al menos **3 consultas** relevantes para el dominio.

Si utiliza RDF, realice las consultas mediante SPARQL.

Ejemplo:

```sparql
PREFIX ex: <http://ejemplo.org/>

SELECT ?estudiante
WHERE {
    ?estudiante ex:cursa ex:IntroduccionIA .
}
```

Para cada consulta indique:

a) Pregunta en lenguaje natural

b) Consulta formal

c) Resultado

d) Interpretación

---

## 7. Relación entre los cinco subtemas

Explique de manera sintética cómo su solución utiliza los contenidos de la unidad.

| Subtema | Evidencia dentro de la solución |
|---|---|
| 3.1 Lógica proposicional y lógica de primer orden | Hechos, predicados, reglas o expresiones |
| 3.2 Redes semánticas, marcos y ontologías | Estructura conceptual del dominio |
| 3.3 Sistemas de inferencia | Encadenamiento y traza |
| 3.4 Razonamiento no monótono e incierto | Excepción, conocimiento incompleto o conclusión revisable |
| 3.5 Web Semántica y grafos de conocimiento | RDF/grafo y consultas |

---

## 8. Reporte técnico

Entregue un reporte de aproximadamente **6 a 10 páginas**, sin contar anexos.

Debe contener:

a) Descripción del dominio y problema

b) Base de conocimiento

c) Reglas utilizadas

d) Estrategia de inferencia

e) Traza de una inferencia completa

f) Caso de excepción o conocimiento incompleto

g) Ontología o grafo de conocimiento

h) Consultas y resultados

i) Limitaciones de la solución

j) Conclusiones

k) Referencias utilizadas

El código o notebook deberá entregarse como archivo adicional o mediante el repositorio indicado por el docente.

---

## 9. Seminario y revisión entre pares

Cada estudiante presentará brevemente su solución.

Durante la revisión entre pares se valorará:

a) Coherencia del modelo de conocimiento

b) Claridad de las reglas

c) Validez de las inferencias

d) Consistencia entre ontología/grafo y sistema simbólico

e) Claridad de las consultas

f) Limitaciones identificadas

La retroalimentación recibida deberá utilizarse para realizar al menos una mejora documentada antes de la entrega final.

---

## Producto final

La entrega deberá contener:

```text
Sistema simbólico documentado
        +
Ontología o grafo de conocimiento
        +
Reporte técnico
        +
Código / notebook
        +
Evidencia de revisión entre pares
```

---

## Rúbrica de evaluación de la actividad

La siguiente rúbrica distribuye **100 puntos dentro de esta evidencia**. La ponderación global de la Unidad 3 dentro del curso se mantiene conforme a la instrumentación didáctica.

| Criterio | Porcentaje |
|---|---:|
| Delimitación del dominio y coherencia del problema | 10% |
| Base de conocimiento y representación formal | 15% |
| Reglas y mecanismo de inferencia | 20% |
| Traza de inferencia y explicación de resultados | 15% |
| Excepción, conocimiento incompleto o revisión de conclusión | 10% |
| Ontología o grafo de conocimiento | 15% |
| Consultas y resultados | 5% |
| Reporte técnico y claridad de la documentación | 5% |
| Seminario, revisión entre pares y mejora documentada | 5% |
| **Total** | **100%** |

---

## Criterios mínimos de aceptación

La actividad se considerará incompleta si falta alguno de los siguientes elementos:

a) Base de conocimiento

b) Reglas

c) Mecanismo o traza de inferencia

d) Ontología o grafo pequeño

e) Consultas

f) Reporte técnico

---

## Síntesis

La actividad integra la progresión de la Unidad 3:

```text
Representar
    ↓
Organizar
    ↓
Inferir
    ↓
Revisar
    ↓
Conectar y consultar conocimiento
```

> El objetivo no es construir un sistema de gran escala, sino demostrar que el estudiante comprende cómo se representa, organiza, razona y consulta conocimiento dentro de una solución simbólica coherente.
