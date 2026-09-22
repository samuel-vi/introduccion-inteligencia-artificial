# Actividad 3.5 — Construcción de un minigrafo de conocimiento

## Propósito

Construir un pequeño grafo de conocimiento de un dominio delimitado, representando entidades, relaciones y hechos mediante RDF, y realizar consultas básicas con SPARQL.

## Instrucciones

Seleccione un dominio sencillo. Puede utilizar alguno de los siguientes:

a) Sistema académico de posgrado

b) Biblioteca

c) Proyectos de investigación

d) Sistema de cursos

e) Otro dominio previamente justificado

## Desarrollo

### 1. Definir el dominio

Describa brevemente el dominio seleccionado y su propósito.

### 2. Identificar tipos de entidades

Defina al menos **5 tipos de entidades**.

Ejemplo:

```text
Estudiante
Profesor
Asignatura
Programa
Institucion
```

### 3. Definir relaciones

Establezca al menos **5 tipos de relaciones**.

Ejemplo:

```text
cursa
imparte
perteneceA
formaParteDe
participaEn
```

### 4. Crear instancias

Incluya al menos **8 instancias** concretas.

Ejemplo:

```text
Ana
Luis
Profesor1
IntroduccionIA
BasesDatos
MSC
TecNM
ProyectoIA
```

### 5. Construir triples RDF

Genere al menos **15 triples RDF**.

Ejemplo:

```text
(Ana, cursa, IntroduccionIA)

(Profesor1, imparte, IntroduccionIA)

(IntroduccionIA, formaParteDe, MSC)

(MSC, perteneceA, TecNM)
```

### 6. Representar el grafo

Incluya una representación gráfica o esquemática del grafo.

Ejemplo:

```text
Ana ── cursa ──► IntroduccionIA
                     │
                formaParteDe
                     ↓
                    MSC
                     │
                perteneceA
                     ↓
                   TecNM
```

### 7. Representar el conocimiento en RDF/Turtle o RDFLib

Puede utilizar:

a) RDF/Turtle

b) RDFLib en Python

c) El notebook del subtema 3.5 como base

Ejemplo Turtle:

```turtle
@prefix ex: <http://ejemplo.org/> .

ex:Ana
    a ex:Estudiante ;
    ex:cursa ex:IntroduccionIA .
```

### 8. Formular consultas SPARQL

Realice al menos **3 consultas SPARQL**.

Las consultas deben responder preguntas distintas.

Ejemplos:

```text
¿Qué estudiantes cursan IntroduccionIA?

¿Qué profesor imparte una asignatura determinada?

¿A qué institución pertenece el programa de una asignatura?
```

### 9. Distinguir ontología y grafo de conocimiento

Explique claramente:

a) Qué elementos de su propuesta corresponden a la ontología

b) Qué elementos corresponden al grafo de conocimiento

### 10. Reflexión final

Responda brevemente:

a) ¿Qué ventaja encontró al representar el dominio como grafo?

b) ¿Qué diferencia existe entre almacenar datos y representar conocimiento?

c) ¿Qué función cumple la ontología dentro del grafo?

d) ¿Qué aporta SPARQL?

e) ¿Qué ocurriría si faltara información en el grafo bajo un supuesto de mundo abierto?

## Producto a entregar

Entregar un archivo en **PDF o Markdown** de aproximadamente **4 a 6 páginas**, acompañado del notebook o archivo de código utilizado.

Debe incluir:

a) Descripción del dominio

b) Tipos de entidades

c) Relaciones

d) Instancias

e) Al menos 15 triples RDF

f) Representación gráfica del grafo

g) Representación en RDF/Turtle o RDFLib

h) Tres consultas SPARQL y sus resultados

i) Diferencia entre ontología y grafo de conocimiento

j) Reflexión final

## Criterios de evaluación

| Criterio | Porcentaje |
|---|---:|
| Definición del dominio | 10% |
| Entidades, relaciones e instancias | 15% |
| Construcción correcta de triples RDF | 20% |
| Representación del grafo | 10% |
| RDF/Turtle o RDFLib | 15% |
| Consultas SPARQL | 15% |
| Distinción ontología vs. grafo | 10% |
| Reflexión final | 5% |
| **Total** | **100%** |

## Relación con la Unidad 3

Esta actividad integra los conceptos desarrollados en toda la Unidad 3:

```text
Lógica
  ↓
Representación del conocimiento
  ↓
Ontologías
  ↓
Inferencia
  ↓
Conocimiento incompleto
  ↓
Web Semántica y grafos de conocimiento
```

El producto puede considerarse como una primera versión del **grafo de conocimiento documentado** solicitado como producto de la unidad.
