# 1.2 Definiciones y enfoques de la Inteligencia Artificial

## Propósito

Comprender las principales formas de definir la Inteligencia Artificial y distinguir los enfoques simbólico, conexionista y estadístico/probabilístico, identificando cómo representan el conocimiento, cómo obtienen soluciones y en qué tipos de problemas pueden utilizarse.

---

## 1. ¿Qué es la Inteligencia Artificial?

No existe una única definición universal de Inteligencia Artificial.

A lo largo de la evolución de la disciplina han surgido diferentes formas de entender qué significa construir un sistema inteligente.

Una manera ampliamente utilizada para organizar estas perspectivas consiste en considerar dos preguntas:

a) ¿El objetivo es reproducir el comportamiento humano o alcanzar un comportamiento racional?

b) ¿El interés se encuentra en la forma de pensar o en la forma de actuar?

A partir de estas dimensiones pueden identificarse cuatro perspectivas:

| Perspectiva | Pregunta principal |
|---|---|
| Pensar humanamente | ¿Puede una máquina pensar de manera similar a una persona? |
| Actuar humanamente | ¿Puede una máquina comportarse de manera similar a una persona? |
| Pensar racionalmente | ¿Puede una máquina razonar correctamente? |
| Actuar racionalmente | ¿Puede una máquina seleccionar acciones que produzcan buenos resultados? |

Estas perspectivas ayudan a comprender **qué esperamos de un sistema de Inteligencia Artificial**.

Sin embargo, no deben confundirse con los paradigmas utilizados para construirlo.

---

## 2. Pensar humanamente

Este enfoque busca comprender y reproducir mediante modelos computacionales algunos procesos asociados con el pensamiento humano.

Tiene una relación importante con disciplinas como:

a) Psicología cognitiva

b) Neurociencia

c) Ciencia cognitiva

d) Inteligencia Artificial

Para estudiar cómo resuelven problemas las personas pueden utilizarse experimentos, observación del comportamiento y modelos cognitivos.

Posteriormente pueden desarrollarse sistemas computacionales que intenten representar dichos procesos.

Este enfoque tiene relación con arquitecturas cognitivas que se estudiarán posteriormente, como **ACT-R** y **Soar**.

---

## 3. Actuar humanamente

Este enfoque se concentra principalmente en el comportamiento observable de una máquina.

Una referencia histórica importante es la **Prueba de Turing**, propuesta a partir del denominado juego de imitación.

En este enfoque pueden ser necesarias capacidades como:

a) Procesamiento del lenguaje natural

b) Representación del conocimiento

c) Razonamiento

d) Aprendizaje

e) Percepción

f) Interacción con el entorno

La pregunta fundamental es:

> **¿El comportamiento producido por la máquina puede considerarse comparable con un comportamiento inteligente humano?**

---

## 4. Pensar racionalmente

El enfoque de pensamiento racional busca construir sistemas capaces de obtener conclusiones mediante procesos de razonamiento formal.

Su fundamento histórico se encuentra principalmente en la lógica.

Por ejemplo:

```text
Todos los mamíferos son animales
La ballena es un mamífero
--------------------------------
La ballena es un animal
```

De manera simplificada:

**Conocimiento → Reglas de inferencia → Conclusión**

Este enfoque se relaciona con áreas como:

a) Lógica

b) Representación del conocimiento

c) Sistemas basados en reglas

d) Demostración automática de teoremas

e) Planificación

Una de sus dificultades aparece cuando el conocimiento disponible es incompleto, ambiguo o incierto.

---

## 5. Actuar racionalmente

Otra perspectiva consiste en construir sistemas capaces de seleccionar acciones que contribuyan al logro de determinados objetivos.

Un sistema puede:

```text
Percibir el entorno
        ↓
Analizar la situación
        ↓
Evaluar alternativas
        ↓
Seleccionar una acción
        ↓
Actuar
        ↓
Evaluar el resultado
```

Esta perspectiva resulta especialmente importante en la Inteligencia Artificial contemporánea y se relaciona con el concepto de **agente racional**.

El tema será desarrollado con mayor profundidad en el subtema:

**1.3 Componentes principales de un agente inteligente**

Para efectos de este curso podemos utilizar la siguiente definición operativa:

> **La Inteligencia Artificial estudia métodos y sistemas capaces de percibir, representar, razonar, aprender o actuar para alcanzar determinados objetivos.**

Esta definición se utiliza como una síntesis didáctica para la asignatura.

---

# 6. Enfoques para construir sistemas de Inteligencia Artificial

Una vez analizadas diferentes formas de entender la Inteligencia Artificial, podemos estudiar cómo se construyen los sistemas capaces de realizar tareas inteligentes.

En este subtema se consideran tres enfoques principales:

**Simbólico**

**Conexionista**

**Estadístico/probabilístico**

Estos enfoques no son necesariamente excluyentes. Un sistema puede utilizar técnicas provenientes de más de uno.

---

# 7. Enfoque simbólico

El enfoque simbólico representa explícitamente conceptos, objetos, relaciones y conocimiento.

Su idea fundamental puede sintetizarse como:

**Símbolos + Reglas + Inferencia**

Por ejemplo, en un sistema destinado a identificar correo electrónico no deseado podrían definirse reglas como:

```text
SI el mensaje contiene "ganaste un premio"
Y contiene "haz clic aquí"
ENTONCES clasificar como spam
```

El conocimiento del sistema se encuentra representado de manera explícita.

## ¿Cómo obtiene una solución?

Puede utilizar mecanismos como:

a) Aplicación de reglas

b) Inferencia lógica

c) Búsqueda

d) Manipulación de símbolos

e) Planificación

## Aplicaciones representativas

a) Sistemas expertos

b) Sistemas basados en reglas

c) Motores de inferencia

d) Sistemas de planificación

e) Representación del conocimiento

## Ventajas

a) El conocimiento puede representarse explícitamente

b) Las reglas pueden ser comprensibles para las personas

c) Algunas conclusiones pueden explicarse mediante las reglas utilizadas

d) Permite incorporar conocimiento proporcionado por especialistas

## Limitaciones

a) La adquisición manual del conocimiento puede resultar compleja

b) Las bases de reglas pueden crecer considerablemente

c) Resulta difícil anticipar todas las situaciones posibles

d) Puede presentar dificultades ante información ambigua o incierta

---

# 8. Enfoque conexionista

El enfoque conexionista se encuentra históricamente inspirado en modelos de procesamiento mediante unidades interconectadas.

Su expresión más representativa en la actualidad son las:

**Redes neuronales artificiales**

En lugar de introducir directamente una gran cantidad de reglas, el sistema puede aprender patrones utilizando ejemplos.

En el caso de detección de spam:

```text
Correos electrónicos etiquetados
              ↓
        Red neuronal
              ↓
       Entrenamiento
              ↓
     Modelo aprendido
              ↓
       Spam / No spam
```

Durante el entrenamiento se ajustan numerosos parámetros internos.

Por ello, el conocimiento no necesariamente aparece como una lista explícita de reglas.

Puede encontrarse distribuido entre:

**Pesos + Activaciones + Representaciones internas**

## Aplicaciones representativas

a) Reconocimiento de imágenes

b) Procesamiento del lenguaje natural

c) Reconocimiento de voz

d) Detección de objetos

e) Sistemas generativos

f) Grandes modelos de lenguaje

## Ventajas

a) Puede aprender relaciones complejas a partir de datos

b) Es adecuado para información de alta dimensionalidad

c) Ha demostrado buenos resultados en problemas de percepción

d) Puede aprender características automáticamente

## Limitaciones

a) Puede requerir grandes cantidades de datos

b) El entrenamiento puede demandar recursos computacionales importantes

c) Sus decisiones pueden resultar difíciles de interpretar

d) La incorporación directa de conocimiento explícito puede ser compleja

---

# 9. Enfoque estadístico y probabilístico

Muchos problemas reales contienen incertidumbre.

En esos casos no siempre es adecuado expresar una conclusión únicamente como:

```text
Spam
```

o:

```text
No spam
```

También puede resultar útil estimar:

```text
P(Spam | contenido del mensaje) = 0.92
```

Es decir:

> Existe una probabilidad estimada del 92 % de que el mensaje corresponda a spam.

El enfoque estadístico/probabilístico utiliza modelos matemáticos para representar y analizar:

a) Incertidumbre

b) Variabilidad

c) Relaciones entre variables

d) Evidencia disponible

e) Probabilidad de diferentes resultados

## Aplicaciones representativas

a) Redes bayesianas

b) Naive Bayes

c) Modelos probabilísticos

d) Modelos de Markov

e) Regresión

f) Métodos estadísticos de aprendizaje

## Ventajas

a) Permite representar incertidumbre explícitamente

b) Puede expresar diferentes grados de confianza

c) Cuenta con fundamentos matemáticos sólidos

d) Resulta útil cuando existe información incompleta o ruidosa

## Limitaciones

a) Puede requerir estimar numerosas probabilidades

b) Algunos métodos requieren determinados supuestos estadísticos

c) Algunos procesos de inferencia pueden ser computacionalmente costosos

d) La calidad de los resultados depende de los datos y del modelo utilizado

---

# 10. Comparación de los enfoques

| Característica | Simbólico | Conexionista | Estadístico/probabilístico |
|---|---|---|---|
| Representación | Símbolos y reglas | Parámetros y representaciones distribuidas | Variables y distribuciones |
| Fuente del conocimiento | Expertos y reglas | Principalmente datos | Datos y conocimiento previo |
| Mecanismo principal | Inferencia y búsqueda | Aprendizaje | Estimación e inferencia probabilística |
| Incertidumbre | Generalmente limitada en modelos clásicos | Puede aprenderse de forma implícita | Puede representarse explícitamente |
| Interpretabilidad | Generalmente alta | Frecuentemente menor | Depende del modelo |
| Ejemplo | Sistema basado en reglas | Red neuronal | Naive Bayes |

> **Esta comparación es una simplificación didáctica. Existen técnicas y sistemas que combinan características de varios enfoques.**

---

# 11. Un mismo problema desde tres enfoques

Consideremos el siguiente problema:

> **Determinar si un correo electrónico recibido corresponde a spam o a un mensaje legítimo.**

El problema es el mismo.

Lo que cambia es la manera de abordarlo.

## Enfoque simbólico

Un especialista puede establecer reglas:

```text
SI contiene "premio"
Y contiene "haz clic"
ENTONCES spam
```

El conocimiento se introduce principalmente mediante reglas explícitas.

---

## Enfoque conexionista

Se proporciona al sistema una colección de correos previamente etiquetados:

```text
Correos etiquetados
        ↓
Red neuronal
        ↓
Aprendizaje de patrones
        ↓
Spam / No spam
```

El sistema aprende regularidades a partir de los ejemplos disponibles.

---

## Enfoque estadístico/probabilístico

El sistema puede estimar:

```text
P(Spam | características del mensaje)
```

Por ejemplo:

```text
P(Spam | mensaje) = 0.92
```

El resultado expresa explícitamente un grado de probabilidad.

---

# 12. Los enfoques pueden combinarse

No debe interpretarse:

**Simbólico vs. Conexionista vs. Probabilístico**

como tres alternativas completamente independientes.

Un sistema moderno puede combinar diferentes aproximaciones.

Por ejemplo:

```text
Modelo de aprendizaje
        ↓
Identificación de patrones
        ↓
Reglas
        ↓
Decisión
```

También pueden integrarse:

```text
Red neuronal
+
Modelo probabilístico
+
Reglas
```

A estos sistemas se les puede considerar **híbridos** cuando integran de manera deliberada diferentes paradigmas o mecanismos.

---

# 13. Inteligencia Artificial, Machine Learning y Deep Learning

Otro aspecto importante consiste en distinguir estos conceptos.

**Machine Learning no es sinónimo de Inteligencia Artificial.**

Machine Learning constituye un área de la Inteligencia Artificial dedicada al desarrollo de sistemas capaces de mejorar su comportamiento o construir modelos a partir de datos o experiencia.

De manera simplificada:

```text
Inteligencia Artificial
        │
        ├── Búsqueda
        │
        ├── Representación del conocimiento
        │
        ├── Razonamiento
        │
        ├── Planificación
        │
        ├── Machine Learning
        │       │
        │       └── Deep Learning
        │
        └── Otros métodos
```

Por lo tanto:

**Machine Learning ⊂ Inteligencia Artificial**

y:

**Deep Learning ⊂ Machine Learning**

Estas relaciones son útiles como una representación introductoria, aunque las fronteras entre áreas pueden variar dependiendo de la clasificación empleada.

---

# 14. Simbólico y subsimbólico

También es frecuente encontrar la distinción entre:

**Simbólico**

y

**Subsimbólico**

En un sistema simbólico, conceptos como:

```text
Correo
Remitente
Mensaje
Spam
```

pueden tener una representación explícita.

En un sistema subsimbólico, el conocimiento puede encontrarse distribuido entre numerosos valores numéricos o parámetros internos.

Las redes neuronales constituyen uno de los ejemplos más representativos de procesamiento subsimbólico.

Es importante señalar que:

> **Subsimbólico no es sinónimo de probabilístico.**

Son formas diferentes de caracterizar un sistema.

---

# 15. ¿Cuál enfoque debe utilizarse?

No existe un enfoque universalmente superior.

La selección depende del problema y de las condiciones disponibles.

Entre los factores que pueden considerarse se encuentran:

a) Tipo de problema

b) Cantidad y calidad de los datos

c) Disponibilidad de conocimiento experto

d) Nivel de incertidumbre

e) Necesidad de explicar las decisiones

f) Recursos computacionales

g) Restricciones del sistema

Por ejemplo:

### Cuando existen reglas claras y conocimiento especializado

**Puede resultar adecuado considerar métodos simbólicos.**

### Cuando existen grandes cantidades de datos complejos

**Pueden resultar adecuados métodos de aprendizaje y enfoques conexionistas.**

### Cuando resulta necesario representar explícitamente la incertidumbre

**Pueden resultar adecuados métodos probabilísticos.**

En muchos problemas reales puede ser conveniente combinar diferentes enfoques.

---

# 16. Relación con las siguientes unidades

Los enfoques estudiados en este subtema aparecerán nuevamente durante el curso.

```text
Unidad 1
Introducción a los enfoques de IA
        ↓
Unidad 3
Representación del conocimiento y razonamiento
        ↓
Unidad 4
Aprendizaje automático
        ↓
Unidad 5
Modelos probabilísticos
```

Por esta razón, el objetivo del 1.2 no es profundizar todavía en algoritmos específicos.

La intención es que el estudiante sea capaz de **reconocer las diferencias conceptuales entre los principales enfoques de Inteligencia Artificial**.

---

## Síntesis

El subtema puede resumirse mediante dos preguntas fundamentales.

### ¿Qué entendemos por Inteligencia Artificial?

Puede estudiarse desde diferentes perspectivas:

**Pensar humanamente**

**Actuar humanamente**

**Pensar racionalmente**

**Actuar racionalmente**

### ¿Cómo pueden construirse sistemas inteligentes?

Mediante diferentes enfoques:

**Simbólico**

**Conexionista**

**Estadístico/probabilístico**

El mismo problema puede ser abordado de diferentes maneras dependiendo del enfoque seleccionado.

> **La Inteligencia Artificial no corresponde a una única técnica. Integra diferentes formas de representar conocimiento, aprender de los datos, razonar bajo incertidumbre y seleccionar acciones para alcanzar objetivos.**

---

## Recursos del subtema

Los materiales complementarios de este subtema estarán disponibles en:

[Recursos y lecturas](recursos/)

[Actividad de aplicación de enfoques de IA](actividades/actividad-enfoques-ia.md)

---

## Fuentes base

Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.

Poole, D. L., & Mackworth, A. K. (2023). *Artificial Intelligence: Foundations of Computational Agents* (3rd ed.). Cambridge University Press.

Mitchell, T. M. (1997). *Machine Learning*. McGraw-Hill.

Goodfellow, I., Bengio, Y., & Courville, A. (2016). *Deep Learning*. MIT Press.

---

[← Volver a la Unidad 1](../)
