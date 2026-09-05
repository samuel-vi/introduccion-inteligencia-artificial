# Recursos complementarios

## 1.3 Componentes principales de un agente inteligente

Los siguientes recursos permiten ampliar los conceptos relacionados con agentes inteligentes, racionalidad, sensores, actuadores, medidas de desempeño, PEAS y características de los entornos de tarea.

---

## Lectura fundamental

### Artificial Intelligence: A Modern Approach

**Autores:** Stuart Russell y Peter Norvig  
**Edición:** 4.ª edición  
**Editorial:** Pearson

### Capítulo recomendado

**Capítulo 2. Intelligent Agents**

Se recomienda revisar particularmente:

a) Agents and Environments

b) Good Behavior: The Concept of Rationality

c) The Nature of Environments

d) The Structure of Agents

### Propósito

Profundizar en los conceptos de:

a) Agente

b) Percepción

c) Secuencia de percepciones

d) Acción

e) Función de agente

f) Programa de agente

g) Racionalidad

h) Medida de desempeño

i) PEAS

j) Entornos de tarea

---

## Artificial Intelligence: Foundations of Computational Agents

**Autores:** David L. Poole y Alan K. Mackworth  
**Edición:** 3.ª edición  
**Editorial:** Cambridge University Press

Este libro presenta la Inteligencia Artificial desde la perspectiva de agentes computacionales que actúan en un entorno.

### Propósito

Complementar el concepto de agente mediante ejemplos computacionales y modelos de interacción entre agentes y entornos.

Recurso disponible en línea:

https://www.cs.ubc.ca/~poole/aibook/3e/html/ArtInt3e.html

---

## AIPython

Poole y Mackworth proporcionan ejemplos y código educativo en Python para estudiar agentes y entornos.

Recurso:

https://artint.info/3e/resources/

### Propósito

Observar cómo pueden representarse mediante programación conceptos como:

```text
Agente
+
Entorno
+
Percepción
+
Acción
```

Este recurso será útil como complemento de la práctica de programación del subtema.

---

## UC Berkeley — CS188: Introduction to Artificial Intelligence

El curso CS188 de la University of California, Berkeley, contiene recursos académicos relacionados con los fundamentos de la Inteligencia Artificial y el diseño de agentes.

Recurso:

https://inst.eecs.berkeley.edu/~cs188/textbook/

### Propósito

Complementar el análisis de:

a) Agentes racionales

b) Entornos

c) Toma de decisiones

d) Búsqueda

e) Aprendizaje

Los conceptos revisados en este recurso aparecerán nuevamente en las siguientes unidades del curso.

---

# PEAS

PEAS permite describir sistemáticamente el entorno de tarea de un agente.

```text
P → Performance measure
E → Environment
A → Actuators
S → Sensors
```

En español:

```text
P → Medida de desempeño
E → Entorno
A → Actuadores
S → Sensores
```

Antes de diseñar un agente conviene responder:

a) ¿Cómo se evaluará su desempeño?

b) ¿En qué entorno funcionará?

c) ¿Qué acciones puede realizar?

d) ¿Qué información puede percibir?

---

## Ejemplos para practicar PEAS

Además del taxi autónomo revisado en el contenido principal, pueden analizarse agentes como:

### Robot aspirador

```text
P → Limpieza, tiempo, energía, seguridad
E → Habitaciones, muebles, personas, obstáculos
A → Ruedas, aspirador
S → Sensores de proximidad, suciedad y posición
```

### Robot de almacén

```text
P → Entregas correctas, rapidez, seguridad, consumo energético
E → Almacén, productos, trabajadores, otros robots
A → Motores, sistema de carga
S → Cámaras, proximidad, posición, lectores de códigos
```

### Asistente digital

```text
P → Exactitud, utilidad, tiempo de respuesta
E → Usuario, aplicaciones, documentos y servicios digitales
A → Mensajes, consultas, creación o modificación de información
S → Texto, voz, archivos y datos provenientes de aplicaciones
```

Estos ejemplos deben considerarse únicamente como puntos de partida. Una especificación PEAS completa depende de la tarea concreta asignada al agente.

---

# Características de los entornos

Los entornos de tarea pueden analizarse mediante diferentes dimensiones.

| Dimensión | Posibilidades |
|---|---|
| Observabilidad | Totalmente observable / Parcialmente observable |
| Número de agentes | Agente único / Multiagente |
| Evolución | Determinista / No determinista |
| Dependencia temporal | Episódico / Secuencial |
| Cambio | Estático / Dinámico |
| Variables | Discretas / Continuas |
| Conocimiento | Conocido / Desconocido |

Estas características afectan directamente la complejidad del problema y las técnicas necesarias para diseñar al agente.

---

# Racionalidad

Un agente racional no tiene que conocer el futuro ni seleccionar siempre una acción que posteriormente resulte perfecta.

Debe tomar la mejor decisión posible considerando:

```text
Percepciones disponibles
+
Conocimiento previo
+
Acciones disponibles
+
Medida de desempeño
```

Por ello:

```text
Racionalidad ≠ Omnisciencia
```

Este concepto resulta importante para evaluar correctamente el comportamiento de los sistemas inteligentes.

---

# Preguntas para orientar el estudio

Al revisar un agente, considera:

a) ¿Cuál es el objetivo del agente?

b) ¿Qué información puede percibir?

c) ¿Qué información importante no puede percibir?

d) ¿Qué acciones tiene disponibles?

e) ¿Cómo se mide su desempeño?

f) ¿El entorno cambia mientras el agente toma decisiones?

g) ¿Existen otros agentes en el entorno?

h) ¿Las acciones actuales afectan decisiones futuras?

i) ¿Existe incertidumbre?

j) ¿Qué tendría que aprender el agente?

---

# Recursos relacionados

[Actividad: PEAS y caracterización del entorno](../actividades/actividad-peas-entorno.md)

[Actividad integradora: Diseño de un agente inteligente](../actividades/actividad-diseno-agente.md)

[Notebook: Agente percepción–acción](../notebooks/agente-percepcion-accion.ipynb)

---

[← Volver al subtema 1.3](../)
