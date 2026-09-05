# Actividad integradora

## Diseño conceptual de una arquitectura de Inteligencia Artificial

## Propósito

Integrar los conceptos estudiados en los subtemas 1.3 y 1.5 mediante el diseño conceptual de la arquitectura interna de un agente inteligente.

La finalidad es relacionar:

**Agente → Arquitectura → Procesamiento → Decisión → Acción**

No es necesario implementar completamente el sistema.

---

# 1. Selección del agente

Retoma un agente diseñado previamente en el subtema 1.3 o selecciona uno nuevo.

Ejemplos:

a) Robot móvil de almacén

b) Asistente digital

c) Robot de inspección

d) Sistema de control inteligente

e) Agente para administración de recursos computacionales

f) Sistema autónomo de navegación

Describe brevemente:

a) Objetivo del agente

b) Entorno en el que opera

c) Información que percibe

d) Acciones que puede realizar

---

# 2. Necesidades de procesamiento

Identifica qué capacidades necesita internamente el agente.

Selecciona las que correspondan:

a) Representación de conocimiento

b) Memoria

c) Manejo de objetivos

d) Selección de acciones

e) Planificación

f) Aprendizaje

g) Respuesta inmediata

h) Razonamiento

i) Adaptación

j) Manejo de incertidumbre

Explica por qué cada capacidad seleccionada es importante.

---

# 3. Selección de arquitectura

Analiza las arquitecturas estudiadas:

```text
Soar
ACT-R
BDI
Arquitectura híbrida
```

Selecciona la que consideres más adecuada para el agente.

Justifica tu elección considerando:

a) Tipo de problema

b) Objetivos del agente

c) Necesidad de planificación

d) Necesidad de reacción rápida

e) Tipo de conocimiento

f) Uso de memoria

g) Necesidad de aprendizaje

---

# 4. Diseño conceptual

Construye un esquema general de la arquitectura propuesta.

Puedes utilizar como referencia una estructura como:

```text
             PERCEPCIÓN
                  ↓
        ┌───────────────────┐
        │   ARQUITECTURA    │
        │                   │
        │ Memoria           │
        │ Conocimiento      │
        │ Objetivos         │
        │ Razonamiento      │
        │ Planificación     │
        │ Aprendizaje       │
        └───────────────────┘
                  ↓
               ACCIÓN
```

Modifica el esquema de acuerdo con la arquitectura seleccionada.

---

# 5. Componentes principales

Completa la siguiente tabla:

| Componente | Función dentro del agente |
|---|---|
| Percepción | |
| Memoria | |
| Representación del conocimiento | |
| Objetivos | |
| Mecanismo de decisión | |
| Planificación | |
| Aprendizaje | |
| Acción | |

Si algún componente no es necesario, justifica por qué.

---

# 6. Flujo de decisión

Describe paso a paso qué ocurre desde que el agente recibe una percepción hasta que ejecuta una acción.

Por ejemplo:

```text
Percepción
    ↓
Actualizar información
    ↓
Consultar memoria
    ↓
Evaluar objetivos
    ↓
Seleccionar alternativa
    ↓
Ejecutar acción
```

Incluye al menos **un escenario concreto**.

---

# 7. Ejemplo de funcionamiento

Describe una situación específica.

Por ejemplo:

```text
Situación:
Un robot móvil detecta un obstáculo inesperado.

Percepción:
Obstáculo a 1 metro.

Procesamiento:
La arquitectura evalúa la situación.

Decisión:
Detenerse y buscar una ruta alternativa.

Acción:
Detener movimiento y replantear trayectoria.
```

Explica qué componentes de la arquitectura participan en cada etapa.

---

# 8. ¿Sería necesaria una arquitectura híbrida?

Aunque hayas seleccionado Soar, ACT-R o BDI, analiza:

> **¿Sería útil combinar esta arquitectura con un componente reactivo, deliberativo, probabilístico o de aprendizaje?**

Explica:

a) Qué mecanismo adicional incorporarías

b) Qué problema resolvería

c) Cómo se integraría con la arquitectura principal

d) Qué ventaja aportaría

---

# 9. Limitaciones

Identifica al menos **tres posibles limitaciones** de tu propuesta.

Pueden relacionarse con:

a) Complejidad

b) Costo computacional

c) Necesidad de datos

d) Dificultad para representar conocimiento

e) Tiempo de respuesta

f) Escalabilidad

g) Interpretabilidad

h) Incertidumbre del entorno

---

# Producto esperado

Elabora un documento que incluya:

a) Descripción del agente

b) Necesidades de procesamiento

c) Arquitectura seleccionada

d) Justificación de la selección

e) Diagrama conceptual

f) Componentes principales

g) Flujo de decisión

h) Ejemplo de funcionamiento

i) Análisis de una posible solución híbrida

j) Limitaciones

k) Conclusiones

---

# Reflexión final

Redacta una reflexión de máximo **200 palabras**:

> **¿Cómo influye la arquitectura interna de un agente en su capacidad para percibir, razonar, aprender y actuar?**

---

# Recursos de apoyo

[Consultar contenido del subtema 1.5](../)

[Consultar recursos complementarios](../recursos/)

[Consultar Soar](../imagenes/soar-ciclo-operadores.png)

[Consultar ACT-R](../imagenes/act-r-arquitectura.png)

[Consultar BDI](../imagenes/bdi-ciclo.png)

[Consultar arquitectura híbrida](../imagenes/arquitectura-hibrida.png)

---

[← Volver al subtema 1.5](../)
