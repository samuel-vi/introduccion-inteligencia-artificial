# Recursos complementarios

## 1.5 Arquitecturas clásicas y modernas de Inteligencia Artificial

Los siguientes recursos permiten ampliar el estudio de las arquitecturas **Soar, ACT-R, BDI e híbridas**, así como comprender sus diferentes objetivos y mecanismos de funcionamiento.

---

## Soar

### Soar Cognitive Architecture

Soar es una arquitectura cognitiva orientada al desarrollo de agentes capaces de resolver problemas, utilizar conocimiento y aprender de la experiencia.

Entre sus principales conceptos se encuentran:

a) Estados

b) Operadores

c) Memoria de trabajo

d) Conocimiento procedimental

e) Aprendizaje

Sitio oficial:

https://soar.eecs.umich.edu/

### Lectura recomendada

Laird, J. E. (2012). *The Soar Cognitive Architecture*. MIT Press.

### Recurso visual

[Consultar ciclo conceptual de Soar](../imagenes/soar-ciclo-operadores.png)

---

## ACT-R

### ACT-R Cognitive Architecture

ACT-R es una arquitectura cognitiva desarrollada para representar y estudiar mecanismos asociados con la cognición humana.

Permite modelar procesos relacionados con:

a) Percepción

b) Memoria

c) Recuperación de conocimiento

d) Reglas de producción

e) Selección de acciones

Sitio oficial:

https://act-r.psy.cmu.edu/

### Lectura recomendada

Anderson, J. R. (2007). *How Can the Human Mind Occur in the Physical Universe?* Oxford University Press.

### Recurso visual

[Consultar arquitectura conceptual ACT-R](../imagenes/act-r-arquitectura.png)

---

## BDI

### Beliefs, Desires and Intentions

La arquitectura BDI modela agentes deliberativos utilizando tres conceptos principales:

```text
Beliefs
+
Desires
+
Intentions
```

En español:

```text
Creencias
+
Deseos
+
Intenciones
```

El agente utiliza sus creencias acerca del entorno, evalúa diferentes objetivos y selecciona aquellos con los cuales decide comprometerse.

### Lectura recomendada

Rao, A. S., & Georgeff, M. P. (1995). *BDI Agents: From Theory to Practice*.

### Recurso visual

[Consultar ciclo conceptual BDI](../imagenes/bdi-ciclo.png)

---

## Arquitecturas híbridas

Las arquitecturas híbridas integran diferentes mecanismos de procesamiento.

Una combinación frecuente es:

```text
Reactividad
+
Deliberación
```

El componente reactivo permite responder rápidamente ante acontecimientos del entorno.

El componente deliberativo permite:

a) Representar objetivos

b) Evaluar alternativas

c) Planificar

d) Seleccionar acciones

Un mecanismo de coordinación determina cómo interactúan ambos componentes.

### Recurso visual

[Consultar arquitectura híbrida](../imagenes/arquitectura-hibrida.png)

---

# Comparación conceptual

| Arquitectura | Pregunta que ayuda a responder |
|---|---|
| **Soar** | ¿Qué operador debo aplicar al estado actual para avanzar hacia el objetivo? |
| **ACT-R** | ¿Cómo pueden modelarse computacionalmente procesos asociados con la cognición humana? |
| **BDI** | ¿Qué creo, qué quiero y con qué objetivo decido comprometerme? |
| **Híbrida** | ¿Cómo combinar una respuesta rápida con razonamiento y planificación? |

---

# ¿Qué arquitectura consultar?

## Si el interés es resolución de problemas

Revisar principalmente:

**Soar**

## Si el interés es modelado cognitivo humano

Revisar principalmente:

**ACT-R**

## Si el interés es diseño de agentes orientados a objetivos

Revisar principalmente:

**BDI**

## Si el problema necesita reacción y planificación

Revisar:

**Arquitecturas híbridas**

Esta orientación es únicamente introductoria. La selección de una arquitectura depende de las características específicas del problema.

---

# Preguntas para orientar el estudio

Al analizar una arquitectura considera:

a) ¿Cuál es su objetivo principal?

b) ¿Cómo representa información?

c) ¿Qué tipos de memoria utiliza?

d) ¿Cómo selecciona acciones?

e) ¿Cómo representa objetivos?

f) ¿Puede aprender?

g) ¿Puede planificar?

h) ¿Qué tipo de aplicaciones resulta adecuado para ella?

i) ¿Qué ventajas ofrece?

j) ¿Qué limitaciones presenta?

---

# Recursos relacionados

[Actividad: Comparación de arquitecturas](../actividades/actividad-comparativa-arquitecturas.md)

[Actividad: Diseño conceptual de una arquitectura](../actividades/actividad-diseno-arquitectura.md)

---

[← Volver al subtema 1.5](../)
