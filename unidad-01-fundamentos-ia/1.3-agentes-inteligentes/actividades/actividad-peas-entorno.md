# Actividad de aprendizaje

## PEAS y caracterización del entorno de un agente inteligente

## Propósito

Aplicar los conceptos de agente inteligente, PEAS y características del entorno mediante el análisis de un sistema capaz de percibir información y realizar acciones para alcanzar un objetivo.

---

## Instrucciones

Selecciona **uno** de los siguientes agentes:

### Caso A. Robot aspirador doméstico

Un robot autónomo debe recorrer una vivienda, identificar zonas que requieren limpieza, evitar obstáculos y administrar el uso de su batería.

### Caso B. Robot móvil de almacén

Un robot debe transportar productos entre diferentes zonas de un almacén evitando obstáculos, personas y otros robots.

### Caso C. Asistente digital de agenda

Un asistente de software debe consultar la agenda de un usuario, identificar compromisos, responder solicitudes y apoyar en la organización de actividades.

### Caso D. Dron para inspección de infraestructura

Un dron debe recorrer una zona determinada, obtener imágenes de una infraestructura y detectar áreas que requieren revisión.

### Caso E. Sistema inteligente de control de temperatura

Un sistema debe mantener determinadas condiciones de temperatura dentro de un edificio utilizando información proveniente de sensores ambientales.

---

# Parte 1. Identificación del agente

Describe brevemente el agente seleccionado.

Incluye:

a) Nombre del agente

b) Objetivo principal

c) Tarea que debe realizar

d) Entorno en el que opera

e) Usuarios o sistemas con los que interactúa

---

# Parte 2. Especificación PEAS

Completa la siguiente matriz:

| Elemento | Descripción |
|---|---|
| **P — Medida de desempeño** | |
| **E — Entorno** | |
| **A — Actuadores** | |
| **S — Sensores** | |

---

## P — Medida de desempeño

Define cómo se determinará si el agente realiza correctamente su tarea.

Evita utilizar únicamente criterios generales como:

```text
"Funciona correctamente"
```

Utiliza indicadores concretos.

Por ejemplo:

```text
Tiempo
Precisión
Consumo energético
Seguridad
Número de errores
Cumplimiento del objetivo
```

Explica al menos **tres criterios de desempeño**.

---

## E — Entorno

Identifica los elementos relevantes del entorno en el que opera el agente.

Considera:

a) Objetos

b) Personas

c) Otros agentes

d) Condiciones físicas o digitales

e) Restricciones

f) Situaciones que pueden afectar el comportamiento del agente

---

## A — Actuadores

Identifica cómo puede actuar el agente sobre el entorno.

Ejemplos:

```text
Moverse
Girar
Enviar una notificación
Modificar información
Encender un dispositivo
Detenerse
Generar una respuesta
```

Recuerda que los actuadores pueden ser físicos o digitales.

---

## S — Sensores

Identifica cómo obtiene información el agente.

Ejemplos:

```text
Cámara
GPS
Sensor de temperatura
Sensor de proximidad
Micrófono
Entrada de texto
Base de datos
API
```

Distingue entre:

**Sensor**

y

**Percepción**

Por ejemplo:

```text
Sensor:
Cámara

Percepción:
Obstáculo detectado a 2 metros
```

Incluye al menos **tres ejemplos de percepciones** que podría recibir el agente.

---

# Parte 3. Caracterización del entorno

Clasifica el entorno del agente utilizando las siguientes dimensiones.

| Dimensión | Clasificación | Justificación |
|---|---|---|
| Observabilidad | Totalmente observable / Parcialmente observable | |
| Número de agentes | Agente único / Multiagente | |
| Evolución | Determinista / No determinista | |
| Dependencia temporal | Episódico / Secuencial | |
| Cambio | Estático / Dinámico | |
| Variables | Discretas / Continuas | |
| Conocimiento | Conocido / Desconocido | |

No es suficiente seleccionar una categoría.

**Cada clasificación debe estar justificada de acuerdo con las características del agente seleccionado.**

---

# Parte 4. Percepciones y acciones

Propón al menos **cinco situaciones** en las que el agente reciba una percepción y deba seleccionar una acción.

Completa la tabla:

| Percepción | Acción posible | Justificación |
|---|---|---|
| | | |
| | | |
| | | |
| | | |
| | | |

Ejemplo:

```text
Percepción:
Nivel de batería = 10 %

Acción:
Ir a estación de carga

Justificación:
El agente necesita conservar energía suficiente para continuar operando.
```

---

# Parte 5. Medida de desempeño y racionalidad

Analiza la siguiente pregunta:

> **¿Qué significa que el agente seleccionado actúe racionalmente?**

Explica tu respuesta considerando:

a) Percepciones disponibles

b) Conocimiento del entorno

c) Acciones disponibles

d) Medida de desempeño

Posteriormente describe una situación en la que:

```text
La acción seleccionada produzca un mal resultado
```

pero:

```text
La decisión pueda seguir considerándose racional
```

Explica por qué.

---

# Producto esperado

Entrega un documento que incluya:

a) Descripción del agente seleccionado

b) Matriz PEAS

c) Caracterización del entorno

d) Ejemplos de percepciones y acciones

e) Análisis de racionalidad

f) Conclusión

---

# Reflexión final

Redacta una reflexión de máximo **150 palabras** respondiendo:

> **¿Por qué es importante analizar el entorno antes de diseñar un agente inteligente?**

---

# Recursos de apoyo

[Consultar contenido del subtema 1.3](../)

[Consultar recursos complementarios](../recursos/)

---

[← Volver al subtema 1.3](../)
