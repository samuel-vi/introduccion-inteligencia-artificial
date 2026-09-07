# Recursos complementarios — 3.1 Lógica proposicional y lógica de primer orden

## Unidad 3. Representación del conocimiento y razonamiento

### Propósito

Los siguientes recursos complementan el contenido académico del subtema **3.1 Lógica proposicional y lógica de primer orden**. La selección prioriza materiales académicos y universitarios que permitan reforzar la representación del conocimiento, la semántica lógica, las bases de conocimiento y la transición de la lógica proposicional a la lógica de primer orden.

> **Importante:** En la Unidad 2 ya se estudiaron satisfacibilidad, CNF y DPLL. Por ello, estos recursos deben utilizarse principalmente para comprender la lógica como **lenguaje de representación del conocimiento y fundamento del razonamiento simbólico**, evitando repetir el tratamiento algorítmico de SAT.

---

## 1. Fuente principal del curso

### a) Russell y Norvig — *Artificial Intelligence: A Modern Approach*

**Referencia**

Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.

**Lecturas recomendadas para este subtema**

a) **Capítulo 7. Logical Agents**
   - 7.1 Knowledge-Based Agents
   - 7.3 Logic
   - 7.4 Propositional Logic: A Very Simple Logic

b) **Capítulo 8. First-Order Logic**
   - 8.1 Representation Revisited
   - 8.2 Syntax and Semantics of First-Order Logic
   - 8.3 Using First-Order Logic

c) **Sección opcional**
   - 8.4 Knowledge Engineering in First-Order Logic, para observar cómo se construyen representaciones de dominios más estructurados

**Enfoque recomendado**

Estas secciones permiten estudiar cómo un agente basado en conocimiento utiliza una base de conocimiento, cómo se distinguen sintaxis y semántica y por qué la lógica de primer orden proporciona una representación más expresiva mediante objetos, predicados, relaciones, variables y cuantificadores.

**Sitio oficial del libro**

https://aima.cs.berkeley.edu/global-index.html

> El Capítulo 9, dedicado a inferencia en lógica de primer orden, se retomará principalmente en el subtema **3.3 Sistemas de inferencia: hacia adelante y hacia atrás**.

---

## 2. Open Logic Project — *forall x: Calgary*

**Recurso**

*forall x: Calgary. An Introduction to Formal Logic*

https://forallx.openlogicproject.org/

**Apartados de interés**

a) Lógica proposicional y tablas de verdad

b) Construcción e interpretación de fórmulas

c) Introducción a lógica de primer orden

d) Predicados y nombres

e) Cuantificadores universal y existencial

f) Interpretaciones y semántica

**Utilidad pedagógica**

Es un texto abierto de lógica formal con explicaciones progresivas y ejercicios. Resulta especialmente útil cuando se requiere reforzar la traducción entre lenguaje natural y expresiones lógicas.

**Consulta directa de lógica de primer orden**

https://forallx.openlogicproject.org/html/Pt5.html

---

## 3. Stanford University — CS221: Artificial Intelligence

### a) Material de lógica de primer orden

**Recurso**

Stanford CS221 — *Logic II*

https://web.stanford.edu/class/archive/cs/cs221/cs221.1196/lectures/logic2-6pp.pdf

**Temas de interés**

a) Semántica de la lógica de primer orden

b) Modelos

c) Predicados y relaciones

d) Variables y cuantificadores

e) Relación entre sintaxis, semántica e inferencia

**Utilidad pedagógica**

Permite observar el tratamiento de la lógica desde una asignatura universitaria de Inteligencia Artificial y refuerza la relación entre modelos lógicos y representación del mundo.

### b) Ejercicios de representación lógica

**Recurso**

Stanford CS221 — *From Language to Logic*

https://web.stanford.edu/class/archive/cs/cs221/cs221.1196/assignments/logic/index.html

**Utilidad pedagógica**

Contiene ejercicios para transformar expresiones en lenguaje natural a lógica proposicional y lógica de primer orden. Puede utilizarse como práctica adicional para comprobar si el estudiante distingue correctamente proposiciones, predicados y cuantificadores.

---

## 4. Open Logic Project — *Sets, Logic, Computation*

**Recurso**

https://slc.openlogicproject.org/

**Utilidad**

Este material profundiza en lógica de primer orden, sintaxis, semántica y consecuencias lógicas. Tiene un nivel más formal que el requerido para el contenido base del subtema, por lo que se recomienda como **lectura de profundización** para estudiantes interesados en fundamentos matemáticos.

---

## 5. Stanford Encyclopedia of Philosophy — Classical Logic

**Recurso**

*Classical Logic*

https://plato.stanford.edu/entries/logic-classical/

**Utilidad**

Ofrece una revisión rigurosa de los componentes de un sistema lógico, especialmente la relación entre:

a) Lenguaje formal

b) Sintaxis

c) Sistemas deductivos

d) Semántica

e) Validez

Se recomienda como recurso de profundización conceptual y no como lectura introductoria principal.

---

## 6. Ruta sugerida de consulta

Para complementar el estudio del subtema se recomienda seguir este orden:

a) Revisar primero el contenido académico del repositorio

b) Consultar Russell y Norvig, capítulos 7 y 8, para relacionar lógica con agentes y bases de conocimiento

c) Utilizar *forall x: Calgary* para reforzar sintaxis, predicados y cuantificadores

d) Resolver algunos ejercicios de Stanford CS221 para practicar la formalización de conocimiento

e) Consultar Open Logic Project o Stanford Encyclopedia of Philosophy únicamente cuando se requiera mayor profundidad formal

---

## 7. Preguntas guía para la lectura

Al revisar los recursos, el estudiante debe ser capaz de responder:

a) ¿Qué diferencia existe entre almacenar datos y representar conocimiento?

b) ¿Qué función cumple una base de conocimiento en un sistema de IA?

c) ¿Cuál es la diferencia entre sintaxis y semántica?

d) ¿Qué representa la expresión `KB ⊨ α`?

e) ¿Por qué la lógica proposicional resulta limitada para representar dominios con numerosos objetos?

f) ¿Qué aportan los predicados, variables y cuantificadores a la lógica de primer orden?

g) ¿Cómo puede una regla general representar conocimiento aplicable a múltiples objetos?

h) ¿Por qué una representación más expresiva puede implicar un razonamiento computacionalmente más complejo?

---

## 8. Recursos que se retomarán posteriormente

Algunos conceptos relacionados aparecen en las fuentes recomendadas, pero **no es necesario profundizar en ellos todavía**:

a) Forward chaining

b) Backward chaining

c) Unificación

d) Resolución en lógica de primer orden

e) Sistemas de reglas de producción

Estos contenidos se desarrollarán principalmente en **3.3 Sistemas de inferencia: hacia adelante y hacia atrás**.

Asimismo, la representación mediante ontologías, OWL y estructuras semánticas se estudiará a partir del **3.2 Redes semánticas, marcos y ontologías (OWL)**.

---

## Referencias

Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.

Magnus, P. D., Button, T., Loftis, J. R., Thomas-Bolduc, A., Trueman, R., & Zach, R. (2021). *forall x: Calgary. An Introduction to Formal Logic*. Open Logic Project.

Stanford University. (2019). *CS221: Artificial Intelligence — Logic*. Stanford University.

Open Logic Project. *Sets, Logic, Computation: An Open Introduction to Logic*.

Stanford Encyclopedia of Philosophy. *Classical Logic*.

---

[← Volver al contenido del subtema 3.1](../README.md)
