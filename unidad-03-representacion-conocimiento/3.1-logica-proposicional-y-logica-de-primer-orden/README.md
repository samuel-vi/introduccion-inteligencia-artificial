# 3.1 Lógica proposicional y lógica de primer orden

## Unidad 3. Representación del conocimiento y razonamiento

### Propósito del subtema

Comprender cómo la lógica proposicional y la lógica de primer orden permiten representar conocimiento de manera formal y cómo dicha representación hace posible que un sistema de Inteligencia Artificial derive información que no fue almacenada explícitamente.

> **Enfoque del subtema:** En la Unidad 2 ya se estudiaron satisfacibilidad, CNF y DPLL. En este subtema la lógica se aborda principalmente como lenguaje de representación del conocimiento y como fundamento del razonamiento simbólico.

---

## 1. ¿Por qué necesita conocimiento un sistema de Inteligencia Artificial?

En la Unidad 2 se estudiaron sistemas capaces de buscar soluciones mediante técnicas como BFS, DFS, A*, minimax, planificación y satisfacibilidad. En esos casos, el problema se definía mediante estados, operadores, restricciones u objetivos.

Sin embargo, existen problemas donde no basta con buscar. Un sistema inteligente también puede necesitar **representar lo que sabe acerca de un dominio y utilizar ese conocimiento para obtener nuevas conclusiones**.

Considere un sistema de apoyo para diagnóstico de una red informática que conoce lo siguiente:

- El router `R1` está operativo
- El equipo `PC1` está conectado a `R1`
- Si un equipo está conectado a un router operativo, entonces puede acceder a la red

A partir de esta información, el sistema debería poder responder:

> ¿PC1 tiene acceso a la red?

La respuesta no necesita estar almacenada directamente. Puede **deducirse** a partir del conocimiento disponible.

Esto introduce una idea central de la IA simbólica:

**Representar conocimiento → Razonar sobre él → Obtener nuevo conocimiento**

---

## 2. Representación del conocimiento

Una computadora puede almacenar datos como:

```text
router = "R1"
estado = "operativo"
```

Pero una representación de conocimiento debe permitir expresar también relaciones y reglas:

```text
R1 es un router
R1 está operativo
PC1 está conectado a R1

Si un equipo está conectado a un router operativo,
entonces tiene acceso a la red
```

La diferencia es importante:

- **Los datos** describen valores o hechos particulares
- **El conocimiento** incorpora significado, relaciones y reglas que pueden utilizarse para razonar

---

## 3. Base de conocimiento

Una **base de conocimiento** (*Knowledge Base*, KB) es un conjunto de afirmaciones que representan lo que un sistema conoce acerca de un dominio.

Una base de conocimiento suele contener:

### a) Hechos

Describen situaciones particulares.

```text
R1 está operativo
PC1 está conectado a R1
```

### b) Reglas

Expresan relaciones generales entre hechos.

```text
SI un equipo está conectado a un router operativo
ENTONCES tiene acceso a la red
```

Conceptualmente:

```text
Información del dominio
        ↓
Base de conocimiento
        ↓
     Inferencia
        ↓
   Conclusiones
```

---

## 4. Lógica proposicional

La **lógica proposicional** permite representar conocimiento mediante proposiciones que pueden tomar uno de dos valores de verdad: **verdadero** o **falso**.

Definamos:

\[
R = \text{R1 está operativo}
\]

\[
C = \text{PC1 está conectado a R1}
\]

\[
A = \text{PC1 tiene acceso a la red}
\]

Cada símbolo representa una afirmación completa del dominio.

---

## 5. Conectores lógicos

Las proposiciones pueden combinarse mediante operadores lógicos.

| Operador | Símbolo | Ejemplo | Interpretación |
|---|---|---|---|
| Negación | ¬ | ¬R | R1 no está operativo |
| Conjunción | ∧ | R ∧ C | R1 está operativo y PC1 está conectado |
| Disyunción | ∨ | R ∨ S | R1 o R2 está operativo |
| Implicación | → | R → A | Si R ocurre, entonces A |
| Bicondicional | ↔ | P ↔ Q | P ocurre si y solo si Q |

Por ejemplo:

\[
(R \land C) \rightarrow A
\]

se interpreta como:

> Si R1 está operativo y PC1 está conectado a R1, entonces PC1 tiene acceso a la red.

La lógica permite transformar conocimiento expresado en lenguaje natural en una representación formal que puede ser procesada por un sistema computacional.

---

## 6. Ejemplo de una base de conocimiento proposicional

Supongamos que tenemos:

\[
R
\]

R1 está operativo.

\[
C
\]

PC1 está conectado a R1.

Además:

\[
(R \land C) \rightarrow A
\]

Si R1 está operativo y PC1 está conectado, entonces PC1 tiene acceso a la red.

Por tanto:

\[
A
\]

PC1 tiene acceso a la red.

La conclusión no necesitaba estar almacenada explícitamente. El sistema puede derivarla a partir de los hechos y reglas disponibles.

---

## 7. Sintaxis y semántica

Cuando se utiliza lógica como lenguaje de representación conviene distinguir dos conceptos.

### Sintaxis

La sintaxis establece **cómo pueden escribirse correctamente las expresiones**.

Por ejemplo:

\[
R \land C
\]

es una expresión correctamente formada.

### Semántica

La semántica establece **qué significa una expresión y bajo qué condiciones es verdadera**.

Por ejemplo:

\[
R \land C
\]

es verdadera únicamente cuando `R` y `C` son verdaderas.

En términos simples:

**Sintaxis = cómo se escribe**

**Semántica = qué significa**

---

## 8. Implicación lógica e inferencia

Si una base de conocimiento contiene:

\[
R
\]

\[
C
\]

\[
(R \land C) \rightarrow A
\]

entonces puede concluirse:

\[
A
\]

La notación:

\[
KB \models A
\]

indica que **A es una consecuencia lógica de la base de conocimiento KB**.

Es importante distinguir dos conceptos:

### Implicación lógica

Es una relación semántica. Una conclusión debe ser verdadera en todos los modelos donde la base de conocimiento sea verdadera.

### Inferencia

Es el procedimiento utilizado para encontrar o demostrar una conclusión.

Los mecanismos específicos de inferencia se estudiarán con mayor profundidad en el subtema **3.3 Sistemas de inferencia: hacia adelante y hacia atrás**.

---

## 9. Limitaciones de la lógica proposicional

La lógica proposicional funciona adecuadamente cuando el dominio puede representarse mediante un número manejable de hechos concretos.

Supongamos que existen cien equipos. Sería necesario definir proposiciones como:

\[
C_1 = \text{PC1 está conectado}
\]

\[
C_2 = \text{PC2 está conectado}
\]

\[
C_3 = \text{PC3 está conectado}
\]

Además, sería necesario repetir reglas similares:

\[
C_1 \land R \rightarrow A_1
\]

\[
C_2 \land R \rightarrow A_2
\]

\[
C_3 \land R \rightarrow A_3
\]

Pero el conocimiento que queremos expresar realmente es general:

> Cualquier equipo conectado a un router operativo tiene acceso a la red.

Para expresar conocimiento de este tipo necesitamos un lenguaje más estructurado: la **lógica de primer orden**.

---

## 10. Lógica de primer orden

La **lógica de primer orden** (*First-Order Logic*, FOL) amplía la lógica proposicional y permite representar explícitamente:

- Objetos
- Propiedades
- Relaciones
- Variables
- Funciones
- Cuantificadores

En lógica proposicional podríamos representar:

\[
PC1ConectadoR1
\]

En lógica de primer orden podemos escribir:

\[
Conectado(PC1,R1)
\]

Ahora la expresión posee una estructura explícita:

- `Conectado` representa una relación
- `PC1` representa un objeto
- `R1` representa otro objeto

---

## 11. Constantes

Las **constantes** representan objetos específicos del dominio.

Ejemplos:

\[
PC1
\]

\[
Router1
\]

\[
Servidor1
\]

Cada constante identifica una entidad concreta.

---

## 12. Predicados

Los **predicados** permiten representar propiedades o relaciones.

### Propiedades

\[
Operativo(Router1)
\]

significa:

> Router1 está operativo.

Otro ejemplo:

\[
Servidor(Servidor1)
\]

significa:

> Servidor1 es un servidor.

### Relaciones

\[
Conectado(PC1,Router1)
\]

significa:

> PC1 está conectado a Router1.

Otro ejemplo:

\[
Administra(Ana,Servidor1)
\]

significa:

> Ana administra Servidor1.

---

## 13. Variables

Una **variable** representa un objeto cualquiera del dominio.

Por ejemplo:

\[
x
\]

Puede utilizarse en:

\[
Equipo(x)
\]

que puede interpretarse como:

> x es un equipo.

Las variables permiten construir reglas generales cuando se combinan con cuantificadores.

---

## 14. Cuantificador universal

El símbolo:

\[
\forall
\]

significa **para todo**.

Por ejemplo:

> Todos los servidores son dispositivos.

puede representarse como:

\[
\forall x\;(Servidor(x) \rightarrow Dispositivo(x))
\]

Esto evita enumerar cada servidor individualmente.

---

## 15. Ejemplo con una red informática

Queremos representar la regla:

> Todo equipo conectado a un router operativo tiene acceso a la red.

Podemos escribir:

\[
\forall x\forall r
((Equipo(x) \land Router(r) \land Conectado(x,r) \land Operativo(r))
\rightarrow TieneAcceso(x))
\]

La expresión puede interpretarse por partes:

- `Equipo(x)`: x es un equipo
- `Router(r)`: r es un router
- `Conectado(x,r)`: x está conectado a r
- `Operativo(r)`: r está operativo
- `TieneAcceso(x)`: x tiene acceso a la red

Una sola regla puede aplicarse a cualquier número de equipos y routers.

---

## 16. Cuantificador existencial

El símbolo:

\[
\exists
\]

significa **existe al menos uno**.

Por ejemplo:

> Existe un router que no está operativo.

puede expresarse como:

\[
\exists x\;(Router(x) \land \neg Operativo(x))
\]

Otro ejemplo:

> Existe algún equipo conectado a Router1.

\[
\exists x\;(Equipo(x) \land Conectado(x,Router1))
\]

---

## 17. Ejemplo integrado: base de conocimiento de una red

### Paso 1. Objetos del dominio

```text
PC1
PC2
Router1
```

### Paso 2. Hechos

\[
Equipo(PC1)
\]

\[
Equipo(PC2)
\]

\[
Router(Router1)
\]

\[
Conectado(PC1,Router1)
\]

\[
Conectado(PC2,Router1)
\]

\[
Operativo(Router1)
\]

### Paso 3. Regla general

\[
\forall x\forall r
((Equipo(x) \land Router(r) \land Conectado(x,r) \land Operativo(r))
\rightarrow TieneAcceso(x))
\]

### Paso 4. Consulta

Queremos determinar:

\[
TieneAcceso(PC1)?
\]

Como se conoce que:

\[
Conectado(PC1,Router1)
\]

Y:

\[
Operativo(Router1)
\]

el conocimiento disponible permite concluir:

\[
TieneAcceso(PC1)
\]

También puede concluirse:

\[
TieneAcceso(PC2)
\]

sin necesidad de escribir una regla independiente para PC2.

---

## 18. Segundo ejemplo: contexto universitario

Considere un sistema académico que conoce:

\[
Estudiante(Ana)
\]

\[
Inscrito(Ana,IA)
\]

y dispone de la regla:

> Todo estudiante inscrito en una asignatura puede acceder a sus recursos.

Podemos representar:

\[
\forall x\forall y
((Estudiante(x) \land Inscrito(x,y))
\rightarrow PuedeAcceder(x,y))
\]

Dado que:

\[
Estudiante(Ana)
\]

Y:

\[
Inscrito(Ana,IA)
\]

se puede concluir:

\[
PuedeAcceder(Ana,IA)
\]

El mismo conocimiento puede aplicarse a cientos de estudiantes sin crear reglas particulares para cada uno.

---

## 19. Lógica proposicional frente a lógica de primer orden

| Característica | Lógica proposicional | Lógica de primer orden |
|---|---|---|
| Unidad básica | Proposición | Objetos y predicados |
| Objetos explícitos | No | Sí |
| Relaciones entre objetos | Indirectas | Explícitas |
| Variables | No | Sí |
| Cuantificadores | No | Sí |
| Reglas generales | Limitadas | Sí |
| Expresividad | Menor | Mayor |
| Complejidad de razonamiento | Generalmente menor | Generalmente mayor |

La lógica de primer orden proporciona una representación más estructurada, pero una mayor expresividad también puede aumentar la complejidad del razonamiento.

---

## 20. Relación con SAT estudiado en la Unidad 2

En la Unidad 2 la lógica proposicional apareció principalmente en el contexto de los problemas de satisfacibilidad.

En SAT la pregunta era:

> ¿Existe alguna asignación de valores de verdad que satisfaga una fórmula?

En esta unidad la pregunta cambia:

> ¿Cómo podemos representar conocimiento mediante lógica y qué conclusiones pueden derivarse de él?

Por tanto:

```text
Unidad 2
Lógica → Satisfacibilidad → Búsqueda de una asignación

Unidad 3
Lógica → Representación del conocimiento → Razonamiento
```

No es necesario repetir CNF, DPLL ni los procedimientos de resolución de SAT ya estudiados.

---

## 21. Limitaciones de la lógica clásica

La lógica proposicional y la lógica de primer orden funcionan especialmente bien cuando el conocimiento puede expresarse mediante afirmaciones claramente verdaderas o falsas.

Sin embargo, los dominios reales pueden contener:

- Información incompleta
- Excepciones a reglas generales
- Conocimiento que cambia
- Información contradictoria
- Incertidumbre

Por ejemplo:

> Si un router está encendido, normalmente proporciona servicio.

La palabra **normalmente** introduce la posibilidad de excepciones, como una falla interna o una configuración incorrecta.

Estos problemas se estudiarán posteriormente en el subtema **3.4 Razonamiento no monótono e incierto** y, desde una perspectiva probabilística, en la Unidad 5.

---

## 22. Errores frecuentes

### a) Confundir implicación con equivalencia

\[
Servidor(x) \rightarrow Dispositivo(x)
\]

significa que todo servidor es un dispositivo. No significa que todo dispositivo sea un servidor.

### b) Confundir un hecho particular con una regla general

\[
Operativo(Router1)
\]

describe solamente a Router1.

Mientras que:

\[
\forall x\;(Router(x) \rightarrow Operativo(x))
\]

afirma que todos los routers están operativos.

### c) Utilizar proposiciones cuando las relaciones son relevantes

En lógica proposicional:

\[
AnaAdministraServidor1
\]

En lógica de primer orden:

\[
Administra(Ana,Servidor1)
\]

La segunda representación captura explícitamente la relación entre los objetos.

### d) Interpretar ausencia de conocimiento como falsedad

Si la base de conocimiento no contiene:

\[
Operativo(Router2)
\]

no significa necesariamente:

\[
\neg Operativo(Router2)
\]

Puede significar simplemente que el sistema no dispone de información suficiente para determinar el estado de Router2.

---

## 23. Síntesis conceptual

El proceso fundamental estudiado en este subtema es:

```text
Mundo real
    ↓
Objetos, propiedades y relaciones
    ↓
Representación lógica
    ↓
Base de conocimiento
    ↓
Razonamiento
    ↓
Nuevo conocimiento
```

La **lógica proposicional** proporciona una forma sencilla de representar hechos y reglas.

La **lógica de primer orden** amplía esta capacidad mediante objetos, predicados, relaciones, variables y cuantificadores.

El objetivo no es únicamente manipular símbolos, sino comprender cómo la lógica permite convertir conocimiento de un dominio en una representación formal que un sistema de IA puede utilizar para razonar.

---

## 24. Conexión con el siguiente subtema

La lógica permite representar conocimiento con precisión, pero cuando un dominio crece puede resultar útil organizar conceptos, categorías, atributos y relaciones mediante estructuras explícitas.

Por ejemplo:

```text
Dispositivo
   ├── Router
   ├── Servidor
   └── Equipo
```

junto con relaciones como:

```text
Es-un
Parte-de
Conectado-a
Administra
```

Esta necesidad conduce al siguiente subtema:

**3.2 Redes semánticas, marcos y ontologías (OWL)**

---

## Resultados de aprendizaje esperados

Al finalizar este subtema, el estudiante será capaz de:

- Explicar la función de la lógica como lenguaje de representación del conocimiento en IA
- Diferenciar lógica proposicional y lógica de primer orden
- Representar hechos y reglas mediante expresiones lógicas sencillas
- Identificar objetos, propiedades, relaciones, variables y cuantificadores en un dominio
- Interpretar una pequeña base de conocimiento y las conclusiones que pueden derivarse de ella
- Reconocer las limitaciones de la lógica clásica frente a conocimiento incompleto o incierto

---

## Referencias principales

- Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson. Capítulos 7, 8 y 9
- Tecnológico Nacional de México. *Temario de la asignatura Introducción a la Inteligencia Artificial*. Maestría en Sistemas Computacionales
- Tecnológico Nacional de México, Instituto Tecnológico de Zitácuaro. *Instrumentación Didáctica de Asignaturas de Posgrado: Introducción a la Inteligencia Artificial*. Periodo agosto-diciembre 2026

---

## Navegación

[← Unidad 3. Representación del conocimiento y razonamiento](../README.md)

**Siguiente:** [3.2 Redes semánticas, marcos y ontologías (OWL)](../3.2-redes-semanticas-marcos-ontologias/README.md)
