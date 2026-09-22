# Unidad 3. Representación del conocimiento y razonamiento

## Objetivo de la unidad

**Estudiar formas estructuradas de representar conocimiento.**

## Datos de la unidad

| Elemento | Valor |
|---|---|
| Horas de trabajo | 6 horas |
| Distribución | 3 horas teóricas + 3 horas prácticas |
| Ponderación | 12% |
| Producto global | Sistema simbólico documentado, ontología/grafo y reporte técnico |
| Estrategias previstas | Diseño de base de conocimiento, trazas de inferencia, sistema experto, ontología o grafo pequeño, seminario y revisión entre pares |

---

## Descripción general

En esta unidad se estudian los fundamentos de la **representación del conocimiento en Inteligencia Artificial**, desde lenguajes lógicos y estructuras semánticas hasta mecanismos de inferencia, razonamiento revisable, ontologías y grafos de conocimiento.

La unidad busca que el estudiante comprenda cómo un sistema inteligente puede:

a) Representar hechos, objetos, propiedades y relaciones

b) Organizar conocimiento de manera estructurada

c) Utilizar reglas para obtener nuevas conclusiones

d) Trabajar con conocimiento incompleto, revisable o incierto

e) Utilizar ontologías y grafos de conocimiento en contextos como la Web Semántica

---

## Ruta de aprendizaje

La progresión conceptual de la unidad es:

```text
3.1 Lógica proposicional y lógica de primer orden
        ↓
3.2 Redes semánticas, marcos y ontologías
        ↓
3.3 Sistemas de inferencia
        ↓
3.4 Razonamiento no monótono e incierto
        ↓
3.5 Web Semántica y grafos de conocimiento
```

La unidad avanza desde:

> **¿Cómo representamos conocimiento?**

hasta:

> **¿Cómo puede un sistema organizarlo, inferir nuevas conclusiones, revisar lo que sabe y consultar conocimiento conectado?**

---

## Estado de avance

| Subtema | Estado |
|---|---|
| 3.1 Lógica proposicional y lógica de primer orden | ✅ Disponible |
| 3.2 Redes semánticas, marcos y ontologías (OWL) | ✅ Disponible |
| 3.3 Sistemas de inferencia: hacia adelante y hacia atrás | ✅ Disponible |
| 3.4 Razonamiento no monótono e incierto | ✅ Disponible |
| 3.5 Ontologías en la Web Semántica y grafos de conocimiento | ✅ Disponible |

---

## 3.1 Lógica proposicional y lógica de primer orden

**Estado:** ✅ Disponible

En este subtema se estudia cómo la lógica puede utilizarse como **lenguaje formal para representar conocimiento** y como fundamento del razonamiento simbólico.

El estudiante trabajará con:

a) Bases de conocimiento

b) Hechos y reglas

c) Lógica proposicional

d) Sintaxis y semántica

e) Consecuencia lógica e inferencia

f) Lógica de primer orden

g) Objetos, predicados y relaciones

h) Variables y cuantificadores

i) Representación de conocimiento general

### Recursos disponibles

- [Contenido académico](./3.1-logica-proposicional-y-logica-de-primer-orden/README.md)
- [Recursos complementarios](./3.1-logica-proposicional-y-logica-de-primer-orden/recursos/README.md)
- [Notebook: Base de conocimiento e inferencia simple](./3.1-logica-proposicional-y-logica-de-primer-orden/notebooks/3.1-base-conocimiento-logica.ipynb)
- [Actividad de aprendizaje](./3.1-logica-proposicional-y-logica-de-primer-orden/actividades/README.md)
- [Imágenes e infografías](./3.1-logica-proposicional-y-logica-de-primer-orden/imagenes/)

### Secuencia sugerida

**Video → Apunte → Infografía → Recursos → Notebook → Actividad → Autoevaluación**

La autoevaluación correspondiente al subtema 3.1 se realiza en Moodle.

---

## 3.2 Redes semánticas, marcos y ontologías (OWL)

**Estado:** ✅ Disponible

En este subtema se estudian formas estructuradas de representar conocimiento, avanzando desde relaciones gráficas entre conceptos hasta la construcción de ontologías formales y computables.

El estudiante trabajará con:

a) Redes semánticas: nodos, arcos, conceptos, instancias y relaciones

b) Relaciones estructurales como `subclase-de`, `instancia-de` y `parte-de`

c) Jerarquías y herencia de propiedades

d) Marcos clase y marcos instancia

e) Ranuras, valores y facetas

f) Ontologías: clases, individuos, propiedades, relaciones y axiomas

g) OWL 2 como lenguaje para representar ontologías computables

h) Conocimiento explícito e implícito mediante razonamiento básico

### Recursos disponibles

- [Contenido académico](./3.2-redes-semanticas-marcos-ontologias/README.md)
- [Recursos complementarios](./3.2-redes-semanticas-marcos-ontologias/recursos/README.md)
- [Práctica con Protégé y OWL 2](./3.2-redes-semanticas-marcos-ontologias/practica/README.md)
- [Actividad de aprendizaje](./3.2-redes-semanticas-marcos-ontologias/actividades/README.md)
- [Imágenes e infografías](./3.2-redes-semanticas-marcos-ontologias/imagenes/)

### Secuencia sugerida

**Video → Apunte → Infografía → Recursos → Práctica con Protégé → Actividad → Autoevaluación**

La autoevaluación correspondiente al subtema 3.2 se realiza en Moodle.

---

## 3.3 Sistemas de inferencia: hacia adelante y hacia atrás

**Estado:** ✅ Disponible

En este subtema se estudia cómo un sistema de Inteligencia Artificial utiliza una **base de hechos** y una **base de reglas** para obtener nuevas conclusiones mediante mecanismos de inferencia.

El estudiante trabajará con:

a) Componentes de un sistema de inferencia

b) Base de hechos, base de reglas y memoria de trabajo

c) Reglas de producción

d) Encadenamiento hacia adelante (*forward chaining*)

e) Encadenamiento hacia atrás (*backward chaining*)

f) Trazas de inferencia

g) Variables, equiparación y unificación básica

h) Comparación entre razonamiento dirigido por datos y dirigido por metas

i) Ejemplo integrado de sistema experto simbólico

j) Implementación didáctica en Python

k) Limitaciones de la inferencia determinista

### Recursos disponibles

- [Contenido académico](./3.3-sistemas-de-inferencia/README.md)
- [Recursos complementarios](./3.3-sistemas-de-inferencia/recursos/README.md)
- [Notebook: Forward y backward chaining](./3.3-sistemas-de-inferencia/notebooks/3.3-sistemas-de-inferencia.ipynb)
- [Actividad de aprendizaje](./3.3-sistemas-de-inferencia/actividades/README.md)
- [Imágenes e infografías](./3.3-sistemas-de-inferencia/imagenes/)

### Secuencia sugerida

**Video → Apunte → Infografía → Recursos → Notebook → Actividad → Autoevaluación**

La autoevaluación correspondiente al subtema 3.3 se realiza en Moodle.

---

## 3.4 Razonamiento no monótono e incierto

**Estado:** ✅ Disponible

En este subtema se estudia cómo un sistema de Inteligencia Artificial puede razonar cuando la información disponible es incompleta, contiene excepciones o puede cambiar.

El estudiante trabajará con:

a) Razonamiento monotónico y no monotónico

b) Conocimiento incompleto

c) Reglas por defecto

d) Excepciones

e) Revisión y retractación de conclusiones

f) Negación como falla

g) Mundo abierto y mundo cerrado

h) Introducción conceptual a la incertidumbre

i) Ejemplos integrados de conocimiento revisable

j) Comparación práctica mediante un notebook en Python

### Recursos disponibles

- [Contenido académico](./3.4-razonamiento-no-monotono-e-incierto/README.md)
- [Recursos complementarios](./3.4-razonamiento-no-monotono-e-incierto/recursos/README.md)
- [Notebook comparativo](./3.4-razonamiento-no-monotono-e-incierto/notebooks/3.4-razonamiento-monotono-no-monotono.ipynb)
- [Actividad de aprendizaje](./3.4-razonamiento-no-monotono-e-incierto/actividades/README.md)
- [Imágenes e infografías](./3.4-razonamiento-no-monotono-e-incierto/imagenes/)

### Secuencia sugerida

**Video → Apunte → Infografías → Recursos → Notebook → Actividad → Autoevaluación**

La autoevaluación correspondiente al subtema 3.4 se realiza en Moodle.

---

## 3.5 Ontologías en la Web Semántica y grafos de conocimiento

**Estado:** ✅ Disponible

En este subtema se estudia cómo las ontologías se utilizan en la **Web Semántica** y en los **grafos de conocimiento** para representar, vincular y consultar información estructurada.

El estudiante trabajará con:

a) Web Semántica

b) IRI e identificación de recursos

c) RDF y triples

d) RDF/Turtle

e) RDFS

f) OWL

g) SPARQL

h) Linked Data

i) Grafos de conocimiento

j) Diferencia entre ontología y grafo de conocimiento

k) Mundo abierto e inferencia en grafos semánticos

l) Construcción práctica de un minigrafo con RDFLib

### Recursos disponibles

- [Contenido académico](./3.5-ontologias-web-semantica-grafos-conocimiento/README.md)
- [Recursos complementarios](./3.5-ontologias-web-semantica-grafos-conocimiento/recursos/README.md)
- [Notebook RDFLib + SPARQL](./3.5-ontologias-web-semantica-grafos-conocimiento/notebooks/3.5-rdflib-sparql.ipynb)
- [Actividad de aprendizaje](./3.5-ontologias-web-semantica-grafos-conocimiento/actividades/README.md)
- [Imágenes e infografías](./3.5-ontologias-web-semantica-grafos-conocimiento/imagenes/)

### Secuencia sugerida

**Video → Apunte → Infografías → Recursos → Notebook → Actividad → Autoevaluación**

La autoevaluación correspondiente al subtema 3.5 se realiza en Moodle.

---

# Integración conceptual de la Unidad 3

Los cinco subtemas forman una secuencia continua.

En **3.1**, el conocimiento se representa mediante:

**Hechos + reglas + expresiones lógicas**

En **3.2**, ese conocimiento se organiza mediante:

**Conceptos + relaciones + propiedades + jerarquías + ontologías**

En **3.3**, el sistema utiliza ese conocimiento para razonar mediante:

**Hechos + reglas + motor de inferencia + trazas**

En **3.4**, se analiza qué ocurre cuando el conocimiento es:

**Incompleto + revisable + sujeto a excepciones**

En **3.5**, el conocimiento se transforma en información:

**Identificable + enlazada + estructurada + consultable**

La progresión completa puede resumirse como:

```text
Situación del mundo real
        ↓
Representación lógica
        ↓
Base de conocimiento
        ↓
Representación estructurada
        ↓
Redes semánticas / marcos / ontologías
        ↓
Motor de inferencia
        ↓
Forward chaining / backward chaining
        ↓
Conclusiones
        ↓
Nueva información / excepciones
        ↓
Revisión de conclusiones
        ↓
RDF / RDFS / OWL
        ↓
Grafo de conocimiento
        ↓
SPARQL
        ↓
Consulta e inferencia
```

---

## Forma sugerida de trabajo

Para cada subtema se recomienda seguir una secuencia común:

```text
Video introductorio
        ↓
Contenido académico
        ↓
Recurso visual
        ↓
Recursos complementarios
        ↓
Práctica o notebook
        ↓
Actividad aplicada
        ↓
Autoevaluación
```

Cuando el contenido requiere una herramienta especializada, como en 3.2, la práctica se realiza con **Protégé**. Cuando el objetivo se beneficia de programación, como en 3.1, 3.3, 3.4 y 3.5, se utiliza un notebook didáctico.

---

## Productos de la unidad

A lo largo de la unidad se integran progresivamente los siguientes productos:

a) Bases de conocimiento

b) Representaciones lógicas

c) Representaciones mediante redes semánticas y marcos

d) Ontologías

e) Trazas de inferencia

f) Sistema simbólico

g) Representación de conocimiento revisable

h) Grafo de conocimiento

i) Consultas SPARQL

j) Reporte técnico

---

## Actividad integradora de la unidad

**Estado:** ✅ Disponible

La actividad integradora articula los cinco subtemas mediante el desarrollo de una solución simbólica para un dominio acotado.

El estudiante deberá integrar:

a) Representación formal del dominio

b) Base de conocimiento con hechos y reglas

c) Inferencia hacia adelante o hacia atrás

d) Trazas de inferencia

e) Al menos una situación con excepción o conocimiento incompleto

f) Una ontología o grafo pequeño

g) Consultas sobre el conocimiento representado

h) Reporte técnico

i) Presentación breve y revisión entre pares

- [Consultar actividad integradora de la Unidad 3](./actividad-integradora/README.md)

---

## Evidencias de aprendizaje

Las evidencias previstas para la unidad incluyen:

a) Representaciones formales de conocimiento

b) Actividades de modelado lógico

c) Notebooks de experimentación

d) Modelos mediante redes semánticas y marcos

e) Ontología desarrollada en Protégé

f) Trazas de inferencia

g) Sistema simbólico documentado

h) Análisis de conocimiento revisable

i) Grafo de conocimiento pequeño

j) Consultas SPARQL

k) Reporte técnico

---

## Evaluación

De acuerdo con la instrumentación didáctica, la unidad contempla productos y actividades relacionados con:

a) Diseño de bases de conocimiento

b) Trazas de inferencia

c) Sistema experto

d) Ontología o grafo pequeño

e) Seminario

f) Revisión entre pares

El producto global de la unidad se orienta a un **sistema simbólico documentado, una ontología o grafo de conocimiento y un reporte técnico**.

---

## Navegación

- [← Volver al repositorio principal](../README.md)
- [Ir al subtema 3.1 →](./3.1-logica-proposicional-y-logica-de-primer-orden/README.md)
- [Ir al subtema 3.2 →](./3.2-redes-semanticas-marcos-ontologias/README.md)
- [Ir al subtema 3.3 →](./3.3-sistemas-de-inferencia/README.md)
- [Ir al subtema 3.4 →](./3.4-razonamiento-no-monotono-e-incierto/README.md)
- [Ir al subtema 3.5 →](./3.5-ontologias-web-semantica-grafos-conocimiento/README.md)
- [Ir a la actividad integradora →](./actividad-integradora/README.md)
