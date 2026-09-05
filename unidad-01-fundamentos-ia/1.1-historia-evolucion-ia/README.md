# 1.1 Historia y evolución de la Inteligencia Artificial

## Propósito

Comprender la evolución de la Inteligencia Artificial desde sus antecedentes teóricos hasta los sistemas contemporáneos, identificando los principales paradigmas, avances tecnológicos, limitaciones y acontecimientos que han contribuido al desarrollo de esta disciplina.

La finalidad no es memorizar fechas, sino comprender cómo han cambiado las formas de representar conocimiento, aprender, razonar y resolver problemas mediante sistemas computacionales.

---

## 1. Antecedentes de la Inteligencia Artificial

La idea de construir sistemas capaces de realizar actividades asociadas con la inteligencia humana es anterior a las computadoras modernas.

La Inteligencia Artificial se desarrolló a partir de aportaciones provenientes de diferentes disciplinas, entre ellas:

a) Filosofía

b) Matemáticas y lógica

c) Teoría de la computación

d) Psicología cognitiva

e) Neurociencia

f) Teoría de control

g) Lingüística

h) Ingeniería de computadoras

Una de las preguntas fundamentales que dieron origen al campo fue:

> **¿Es posible describir el razonamiento de manera suficientemente precisa para que una máquina pueda ejecutarlo?**

---

## 2. Alan Turing y las máquinas inteligentes

Alan Turing realizó contribuciones fundamentales al desarrollo de la computación.

En 1950 publicó el artículo **Computing Machinery and Intelligence**, en el que planteó la pregunta:

> **¿Pueden pensar las máquinas?**

Turing propuso abordar esta cuestión mediante el denominado **juego de imitación**, posteriormente conocido como **Prueba de Turing**.

La prueba plantea una interacción mediante lenguaje entre una persona y dos participantes ocultos, uno humano y otro artificial. Si el evaluador no puede distinguir consistentemente cuál es la máquina, se considera que esta presenta un comportamiento comparable al humano dentro de la prueba.

Este planteamiento ayudó a convertir el estudio de la inteligencia de las máquinas en un problema susceptible de investigación científica.

---

## 3. Dartmouth y el nacimiento formal de la IA

El año **1956** suele considerarse el nacimiento formal de la Inteligencia Artificial como disciplina.

John McCarthy, Marvin Minsky, Nathaniel Rochester y Claude Shannon promovieron el **Dartmouth Summer Research Project on Artificial Intelligence**.

En la propuesta del proyecto se utilizó explícitamente el término:

**Artificial Intelligence**

La hipótesis central era que aspectos del aprendizaje y de la inteligencia podían describirse con suficiente precisión como para ser simulados mediante máquinas.

A partir de este periodo comenzaron a desarrollarse numerosos programas destinados a resolver problemas, demostrar teoremas y reproducir procesos de razonamiento.

---

## 4. Primeros sistemas de resolución de problemas

Durante las primeras décadas de la IA surgieron sistemas destinados a reproducir estrategias humanas de resolución de problemas.

Uno de los ejemplos más representativos fue el **General Problem Solver (GPS)**, desarrollado por Allen Newell y Herbert Simon.

De manera simplificada, estos sistemas podían representar un problema mediante:

**Estado actual → Objetivo → Operadores → Nuevo estado**

Esta forma de representar problemas constituye uno de los antecedentes de los métodos de búsqueda que se estudiarán posteriormente en la Unidad 2.

---

## 5. Inteligencia Artificial simbólica

Durante una etapa importante de la historia de la IA predominó el enfoque simbólico.

Su idea fundamental consiste en representar explícitamente conocimiento mediante:

**Símbolos + Reglas + Inferencia**

Por ejemplo:

```text
SI temperatura_alta
Y humo_detectado
ENTONCES posible_incendio
```

El sistema utiliza reglas para manipular representaciones simbólicas y obtener nuevas conclusiones.

Este paradigma tuvo una gran influencia en el desarrollo de sistemas de razonamiento, representación del conocimiento y sistemas expertos.

---

## 6. Sistemas expertos

Durante las décadas de 1970 y 1980 tuvieron un importante desarrollo los **sistemas expertos**.

Estos sistemas buscaban representar el conocimiento especializado de una persona experta mediante dos componentes principales:

**Base de conocimiento + Motor de inferencia**

Entre los sistemas históricos más conocidos se encuentran:

### DENDRAL

Sistema desarrollado para apoyar el análisis de estructuras químicas.

### MYCIN

Sistema orientado al apoyo del diagnóstico de determinadas infecciones bacterianas y la recomendación de tratamientos.

Los sistemas expertos demostraron la importancia del conocimiento especializado del dominio para resolver problemas complejos.

---

## 7. Limitaciones de los primeros enfoques

Los primeros sistemas de IA encontraron diferentes dificultades.

Entre las principales se encuentran:

a) Crecimiento acelerado del número de posibles soluciones

b) Dificultad para representar problemas del mundo real

c) Complejidad para adquirir conocimiento de especialistas

d) Mantenimiento difícil de grandes bases de reglas

e) Información incompleta o incierta

f) Capacidad computacional limitada

Un concepto especialmente importante fue la **explosión combinatoria**, que ocurre cuando el número de alternativas posibles crece tan rápidamente que resulta impráctico analizarlas todas.

---

## 8. Los inviernos de la Inteligencia Artificial

Las elevadas expectativas sobre las capacidades de la IA no siempre pudieron cumplirse.

Como consecuencia se produjeron periodos de disminución de financiamiento, interés e inversión conocidos como:

**Inviernos de la Inteligencia Artificial**

Estos periodos permiten observar un patrón que ha aparecido varias veces en la historia de la disciplina:

**Grandes expectativas → Limitaciones tecnológicas → Desilusión → Nuevos avances**

El estudio de estos ciclos permite analizar de manera crítica las expectativas actuales en torno a las nuevas tecnologías de IA.

---

## 9. Del conocimiento programado al aprendizaje a partir de datos

Una transformación importante ocurrió cuando comenzaron a utilizarse con mayor intensidad métodos capaces de aprender patrones directamente a partir de datos.

En un sistema tradicional basado en reglas:

**Conocimiento humano → Reglas → Programa**

En Machine Learning:

**Datos → Algoritmo de aprendizaje → Modelo**

Por ejemplo, un sistema de detección de correo no deseado puede aprender patrones utilizando grandes cantidades de mensajes previamente clasificados.

Este cambio favoreció el desarrollo del **aprendizaje automático o Machine Learning**.

---

## 10. Redes neuronales y Deep Learning

Las redes neuronales artificiales tienen antecedentes desde las primeras etapas de la IA, pero su utilización aumentó considerablemente gracias a diferentes avances tecnológicos.

Entre ellos:

a) Mayor disponibilidad de datos

b) Incremento de la capacidad computacional

c) Desarrollo de unidades de procesamiento gráfico o GPU

d) Mejora de los algoritmos de entrenamiento

e) Disponibilidad de grandes conjuntos de datos

Estas condiciones contribuyeron al crecimiento del **Deep Learning**.

Las redes neuronales profundas permitieron avances importantes en áreas como:

a) Visión por computadora

b) Reconocimiento de voz

c) Procesamiento del lenguaje natural

d) Robótica

e) Medicina

f) Juegos

---

## 11. Deep Blue y AlphaGo

Dos acontecimientos permiten observar diferentes etapas de la evolución de la IA.

### Deep Blue

En 1997, el sistema **Deep Blue**, desarrollado por IBM, derrotó al campeón mundial de ajedrez Garry Kasparov.

Su funcionamiento se apoyaba principalmente en:

**Búsqueda + Evaluación de posiciones + Capacidad computacional**

Deep Blue no utilizaba Deep Learning como los sistemas actuales.

### AlphaGo

En 2016, **AlphaGo**, desarrollado por DeepMind, derrotó al jugador profesional Lee Sedol en el juego de Go.

AlphaGo integró diferentes técnicas, entre ellas:

**Redes neuronales + Aprendizaje + Búsqueda**

Este caso muestra que las técnicas modernas de IA pueden combinar métodos desarrollados en diferentes etapas históricas.

---

## 12. Inteligencia Artificial generativa

Una etapa reciente de la evolución de la IA corresponde al desarrollo de sistemas capaces de generar contenido.

Estos sistemas pueden producir:

a) Texto

b) Imágenes

c) Audio

d) Video

e) Código

A diferencia de un sistema orientado únicamente a clasificar una entrada, un modelo generativo puede producir nuevo contenido a partir de instrucciones, datos o representaciones aprendidas.

La IA generativa constituye actualmente una de las áreas de mayor desarrollo dentro de la Inteligencia Artificial.

---

## 13. La evolución de la IA no es lineal

Es importante evitar interpretar la evolución de la IA como una simple secuencia en la que una tecnología sustituye completamente a la anterior.

No debe entenderse únicamente como:

**IA simbólica → Machine Learning → Deep Learning → IA generativa**

Actualmente continúan utilizándose técnicas desarrolladas en diferentes etapas históricas, entre ellas:

a) Representación simbólica

b) Reglas

c) Búsqueda

d) Lógica

e) Probabilidad

f) Optimización

g) Machine Learning

h) Deep Learning

i) Aprendizaje por refuerzo

j) Métodos híbridos

Por ello, la evolución de la IA puede entenderse mejor como el desarrollo y la integración progresiva de diferentes paradigmas.

---

## Síntesis

La historia de la Inteligencia Artificial muestra diferentes formas de abordar el problema de construir sistemas capaces de realizar tareas asociadas con la inteligencia.

Entre sus principales etapas se encuentran:

**Razonamiento formal → IA simbólica → Sistemas expertos → Machine Learning → Deep Learning → IA generativa**

Sin embargo, estas etapas no representan una sustitución absoluta de los enfoques anteriores.

Las técnicas desarrolladas a lo largo de la historia continúan coexistiendo y pueden integrarse para resolver problemas complejos.

> **La historia de la Inteligencia Artificial es también la historia de diferentes formas de representar conocimiento, aprender, razonar y resolver problemas.**

---

## Recursos del subtema

Los siguientes materiales complementan el contenido de este subtema:

[Recursos y lecturas](recursos/)

[Línea de tiempo de la Inteligencia Artificial](recursos/linea-tiempo.md)

[Actividad de reflexión](actividades/actividad-reflexion.md)

---

## Fuentes base

Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.

Turing, A. M. (1950). Computing Machinery and Intelligence. *Mind, 59*(236), 433–460.

McCarthy, J., Minsky, M. L., Rochester, N., & Shannon, C. E. (1955). *A Proposal for the Dartmouth Summer Research Project on Artificial Intelligence*.

---

[← Volver a la Unidad 1](../)
