# Actividad integradora

## Diseño conceptual de un agente inteligente

## Propósito

Integrar los conceptos estudiados en el subtema 1.3 mediante el diseño conceptual de un agente inteligente capaz de percibir un entorno, seleccionar acciones y actuar de acuerdo con una medida de desempeño.

La actividad no requiere implementar completamente el sistema.

El objetivo es diseñar correctamente:

**Agente + Entorno + Percepciones + Acciones + Racionalidad**

---

# 1. Selección del problema

Selecciona un problema que pueda ser abordado mediante un agente inteligente.

Puedes utilizar alguno de los siguientes ejemplos:

a) Robot para entrega de materiales en un edificio

b) Sistema inteligente para control de iluminación

c) Asistente para organización de actividades académicas

d) Robot para inspección de instalaciones

e) Sistema de recomendación de acciones para ahorro energético

f) Agente para administración de recursos computacionales

g) Sistema para supervisión de una línea de producción

También puedes proponer otro problema, siempre que pueda representarse mediante un agente que perciba información y realice acciones.

---

# 2. Descripción del problema

Describe brevemente:

a) Situación que se desea atender

b) Objetivo del agente

c) Usuarios involucrados

d) Entorno en el que funcionará

e) Resultado esperado

La descripción debe permitir comprender claramente:

> **¿Qué problema resolverá el agente y para qué?**

---

# 3. Especificación PEAS

Define el entorno de tarea utilizando PEAS.

| Elemento | Descripción |
|---|---|
| **P — Medida de desempeño** | |
| **E — Entorno** | |
| **A — Actuadores** | |
| **S — Sensores** | |

---

## 3.1 Medida de desempeño

Define al menos **cuatro criterios** que permitan evaluar el comportamiento del agente.

Pueden incluir:

a) Precisión

b) Tiempo

c) Seguridad

d) Consumo energético

e) Número de errores

f) Costo

g) Cumplimiento del objetivo

h) Satisfacción del usuario

Explica por qué cada criterio es importante.

---

## 3.2 Entorno

Describe los elementos relevantes del entorno.

Considera:

a) Personas

b) Objetos

c) Otros agentes

d) Sistemas externos

e) Condiciones físicas o digitales

f) Restricciones

g) Situaciones imprevistas

---

## 3.3 Sensores

Identifica cómo obtiene información el agente.

Para cada sensor, indica una posible percepción.

| Sensor o fuente de información | Ejemplo de percepción |
|---|---|
| | |
| | |
| | |
| | |

Recuerda que un agente de software también puede utilizar como fuentes:

```text
APIs
Bases de datos
Archivos
Mensajes
Formularios
Servicios web
```

---

## 3.4 Actuadores

Identifica las formas en que el agente puede actuar.

Completa:

| Actuador o mecanismo | Acción que puede realizar |
|---|---|
| | |
| | |
| | |
| | |

Los actuadores pueden ser físicos o digitales.

---

# 4. Caracterización del entorno

Clasifica el entorno:

| Dimensión | Clasificación | Justificación |
|---|---|---|
| Observabilidad | Total / Parcial | |
| Número de agentes | Único / Multiagente | |
| Evolución | Determinista / No determinista | |
| Dependencia temporal | Episódico / Secuencial | |
| Cambio | Estático / Dinámico | |
| Variables | Discretas / Continuas | |
| Conocimiento | Conocido / Desconocido | |

Cada clasificación debe incluir una explicación.

---

# 5. Percepciones y acciones

Describe al menos **cinco situaciones** posibles.

| Situación | Percepción | Acción seleccionada | Justificación |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |

---

# 6. Función del agente

Describe conceptualmente cómo el agente transforma percepciones en acciones.

Puede representarse mediante:

```text
Percepciones
      ↓
Procesamiento
      ↓
Evaluación de alternativas
      ↓
Selección de acción
      ↓
Acción
```

También puedes expresar:

```text
f: Secuencia de percepciones → Acción
```

Explica qué información necesita considerar el agente antes de seleccionar una acción.

---

# 7. Racionalidad

Responde:

> **¿Qué significaría que tu agente actuara racionalmente?**

Considera:

a) Información disponible

b) Objetivo del agente

c) Acciones disponibles

d) Medida de desempeño

e) Incertidumbre del entorno

Describe además una situación en la que el agente tome una decisión razonable pero el resultado final sea negativo debido a información que no podía conocer.

Explica por qué la decisión inicial podría seguir considerándose racional.

---

# 8. Representación conceptual

Construye un esquema general de tu agente.

Puedes utilizar la siguiente estructura:

```text
                    ENTORNO
                       ↓
                    Sensores
                       ↓
                  Percepciones
                       ↓
            ┌───────────────────┐
            │      AGENTE       │
            │                   │
            │ Conocimiento      │
            │ Procesamiento     │
            │ Decisión          │
            └───────────────────┘
                       ↓
                    Acción
                       ↓
                   Actuadores
                       ↓
                    ENTORNO
```

Puedes modificar el esquema para representar las características específicas de tu propuesta.

---

# 9. Técnica de Inteligencia Artificial

A partir de los enfoques estudiados en el subtema 1.2, analiza qué mecanismos podrían utilizarse dentro del agente.

Puedes considerar:

a) Reglas simbólicas

b) Modelos probabilísticos

c) Machine Learning

d) Redes neuronales

e) Búsqueda

f) Planificación

g) Combinaciones de técnicas

No es necesario implementar estos métodos.

Justifica qué técnica o combinación sería adecuada y qué función realizaría dentro del agente.

---

# 10. Posible arquitectura

Propón una organización conceptual de los principales componentes del sistema.

Por ejemplo:

```text
Sensores
   ↓
Módulo de percepción
   ↓
Modelo del entorno
   ↓
Módulo de decisión
   ↓
Acción
   ↓
Actuadores
```

Describe brevemente la función de cada componente.

Esta propuesta será útil posteriormente para relacionar el diseño con las arquitecturas estudiadas en el subtema 1.5.

---

# Producto esperado

Elabora un documento que incluya:

a) Descripción del problema

b) Objetivo del agente

c) Especificación PEAS

d) Caracterización del entorno

e) Percepciones y acciones

f) Función del agente

g) Análisis de racionalidad

h) Representación conceptual

i) Técnica de IA propuesta

j) Posible arquitectura

k) Conclusiones

---

# Reflexión final

Redacta una reflexión de máximo **200 palabras**:

> **¿Qué aspectos deben definirse antes de seleccionar los algoritmos o tecnologías que utilizará un agente inteligente?**

Relaciona tu respuesta con los conceptos revisados en los subtemas 1.2 y 1.3.

---

# Recursos de apoyo

[Consultar contenido del subtema 1.3](../)

[Consultar recursos complementarios](../recursos/)

[Consultar notebook Agente percepción–acción](../notebooks/agente-percepcion-accion.ipynb)

---

[← Volver al subtema 1.3](../)
