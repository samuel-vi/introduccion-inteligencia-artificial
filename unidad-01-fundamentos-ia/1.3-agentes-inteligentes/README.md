# 1.3 Componentes principales de un agente inteligente

## Propósito

Comprender el concepto de agente inteligente, identificar los elementos que intervienen en su interacción con el entorno y analizar cómo las percepciones, acciones, objetivos y medidas de desempeño influyen en la selección de un comportamiento racional.

La idea fundamental de este subtema puede resumirse como:

**Un agente percibe su entorno y actúa sobre él.**

---

## 1. ¿Qué es un agente?

Un agente es una entidad capaz de percibir un entorno mediante sensores y actuar sobre dicho entorno mediante actuadores.

De manera general:

```text
             Percepciones
                  ↓
Entorno → Sensores → AGENTE → Actuadores → Entorno
                               ↓
                             Acción
```

Este ciclo de percepción y acción constituye uno de los conceptos fundamentales de la Inteligencia Artificial basada en agentes.

---

## 2. Agentes físicos y agentes de software

Un agente no necesariamente debe ser un robot.

Puede ser una entidad física o un sistema completamente digital.

### Agente humano

Puede percibir utilizando:

a) Vista

b) Oído

c) Tacto

d) Olfato

Y actuar mediante:

a) Manos

b) Piernas

c) Voz

---

### Agente robótico

Puede utilizar sensores como:

a) Cámaras

b) Radar

c) Lidar

d) Micrófonos

e) GPS

f) Sensores de distancia

Y actuar mediante:

a) Motores

b) Ruedas

c) Brazos robóticos

d) Sistemas de dirección

---

### Agente de software

Un agente también puede operar exclusivamente dentro de un entorno digital.

Puede recibir información mediante:

a) Archivos

b) Bases de datos

c) APIs

d) Mensajes

e) Entrada de texto

f) Entrada de voz

Y realizar acciones como:

a) Generar una respuesta

b) Consultar información

c) Modificar un archivo

d) Enviar un mensaje

e) Ejecutar una operación

> **Un agente inteligente no necesita poseer un cuerpo físico.**

---

## 3. El entorno

El entorno corresponde a aquello con lo que interactúa el agente.

Para diseñar un agente interesa especialmente la parte del entorno que:

a) Puede afectar lo que el agente percibe

b) Puede ser modificada por sus acciones

En el caso de un taxi autónomo, el entorno puede incluir:

```text
Calles
Vehículos
Peatones
Semáforos
Pasajeros
Clima
Señalización
Obstáculos
```

---

## 4. Sensores

Los sensores permiten obtener información acerca del entorno.

En un taxi autónomo pueden incluir:

a) Cámaras

b) Radar

c) Lidar

d) GPS

e) Velocímetro

f) Acelerómetros

g) Micrófonos

h) Sensores internos del vehículo

De manera general:

```text
Entorno
   ↓
Sensores
   ↓
Información
```

Es importante distinguir entre **sensor** y **percepción**.

El sensor es el mecanismo mediante el cual se obtiene información.

La percepción corresponde a la información que el agente recibe acerca del entorno.

---

## 5. Percepciones

Una percepción representa la información que el agente obtiene mediante sus sensores.

Por ejemplo:

```text
Semáforo = rojo
```

```text
Velocidad = 45 km/h
```

```text
Obstáculo = 12 metros
```

Por tanto:

```text
Sensor
   ↓
Datos
   ↓
Percepción del entorno
```

---

## 6. Secuencia de percepciones

Un agente no necesariamente toma decisiones utilizando solamente la información obtenida en el instante actual.

Puede considerar el historial de percepciones recibidas.

A este historial se le denomina **secuencia de percepciones**.

Por ejemplo:

```text
t1 → Semáforo verde

t2 → Semáforo amarillo

t3 → Semáforo rojo
```

La secuencia proporciona información temporal que puede influir en la acción seleccionada.

---

## 7. Actuadores

Los actuadores son los mecanismos mediante los cuales el agente puede influir sobre el entorno.

En un taxi autónomo pueden incluir:

a) Dirección

b) Acelerador

c) Frenos

d) Luces direccionales

e) Claxon

f) Pantalla

g) Sistema de voz

Por ejemplo:

```text
Percepción:
Semáforo = rojo
        ↓
Decisión:
Detener vehículo
        ↓
Actuador:
Freno
        ↓
Acción:
Detenerse
```

Los sensores permiten recibir información.

Los actuadores permiten ejecutar acciones.

---

## 8. Acción

Una acción es una operación seleccionada por el agente para modificar o influir sobre el entorno.

En un taxi autónomo pueden existir acciones como:

```text
Acelerar
Frenar
Girar
Detenerse
Cambiar de carril
```

El ciclo completo puede representarse como:

```text
Entorno
   ↓
Sensores
   ↓
Percepción
   ↓
Agente
   ↓
Selección de acción
   ↓
Actuadores
   ↓
Acción
   ↓
Entorno
```

---

## 9. Función de agente

Una pregunta fundamental es:

> **¿Cómo determina el agente qué acción debe ejecutar?**

La función de agente representa conceptualmente la relación entre una secuencia de percepciones y una acción.

Puede expresarse como:

```text
Secuencia de percepciones
          ↓
    Función de agente
          ↓
  Acción seleccionada
```

De manera formal:

**f: Percepciones → Acción**

Por ejemplo:

```text
Percepción:
Semáforo = rojo

        ↓

Función del agente

        ↓

Acción:
Frenar
```

---

## 10. Función de agente y programa de agente

Estos conceptos no deben confundirse.

### Función de agente

Describe de manera abstracta qué acción corresponde a cada posible secuencia de percepciones.

### Programa de agente

Es la implementación computacional que realiza dicha función.

El programa puede utilizar:

a) Reglas

b) Algoritmos de búsqueda

c) Modelos probabilísticos

d) Redes neuronales

e) Métodos de planificación

f) Combinaciones de diferentes técnicas

Por ejemplo:

```text
Percepciones
     ↓
Programa del agente
     ↓
Reglas / Modelos / Algoritmos
     ↓
Acción
```

---

## 11. Arquitectura y programa

El programa del agente necesita ejecutarse sobre una determinada infraestructura.

Una forma clásica de expresar esta relación es:

**Agente = Arquitectura + Programa**

La arquitectura proporciona los recursos físicos o computacionales sobre los cuales opera el programa.

En un taxi autónomo:

```text
Taxi autónomo
      │
      ├── Arquitectura
      │     ├── Computadora
      │     ├── Cámaras
      │     ├── Radar
      │     ├── GPS
      │     ├── Frenos
      │     └── Dirección
      │
      └── Programa
            ├── Percepción
            ├── Razonamiento
            ├── Planificación
            ├── Aprendizaje
            └── Control
```

Este concepto prepara el estudio posterior de las arquitecturas de Inteligencia Artificial.

---

## 12. Agente racional

No basta con que un agente ejecute acciones.

Se busca que seleccione acciones adecuadas de acuerdo con sus objetivos y con la información disponible.

Esto conduce al concepto de **agente racional**.

> **Un agente racional selecciona la acción que espera producir el mejor desempeño posible considerando la información disponible.**

La racionalidad depende de elementos como:

a) Medida de desempeño

b) Conocimiento previo del entorno

c) Acciones disponibles

d) Secuencia de percepciones

De manera simplificada:

```text
Percepciones
+
Conocimiento
+
Acciones disponibles
+
Medida de desempeño
        ↓
Selección racional de una acción
```

---

## 13. Racionalidad no significa perfección

Un agente racional no conoce necesariamente todo lo que ocurrirá en el futuro.

Por ello:

**Racionalidad ≠ Omnisciencia**

Considere el siguiente ejemplo:

```text
Semáforo = verde
Vía = aparentemente libre
Velocidad = permitida
```

El agente decide avanzar.

Si posteriormente aparece de manera inesperada un peatón que no podía observarse, la decisión original no necesariamente fue irracional.

La racionalidad debe evaluarse considerando la información disponible cuando se tomó la decisión.

---

## 14. Medida de desempeño

Para evaluar si el agente está realizando adecuadamente su tarea se utiliza una **medida de desempeño**.

Esta establece los criterios mediante los cuales se valoran los resultados obtenidos.

En un taxi autónomo podría considerar:

a) Seguridad

b) Tiempo de viaje

c) Cumplimiento de normas

d) Comodidad

e) Consumo energético

f) Costo

g) Impacto sobre otros usuarios

Una medida de desempeño mal definida puede generar comportamientos no deseados.

Por ejemplo, evaluar únicamente:

```text
Llegar lo más rápido posible
```

podría favorecer acciones peligrosas.

Una medida más adecuada podría considerar:

```text
Seguridad
+
Tiempo
+
Cumplimiento de normas
+
Comodidad
```

---

# 15. PEAS: especificación del entorno de tarea

Una forma estructurada de definir la tarea de un agente es mediante **PEAS**.

PEAS corresponde a:

| Elemento | Significado |
|---|---|
| **P** | Performance measure — Medida de desempeño |
| **E** | Environment — Entorno |
| **A** | Actuators — Actuadores |
| **S** | Sensors — Sensores |

PEAS permite responder cuatro preguntas fundamentales:

```text
¿Cómo evaluaremos al agente?

¿Dónde opera?

¿Cómo puede actuar?

¿Cómo obtiene información?
```

---

## 16. Ejemplo PEAS: taxi autónomo

| PEAS | Taxi autónomo |
|---|---|
| **P — Medida de desempeño** | Seguridad, rapidez, legalidad, comodidad y eficiencia |
| **E — Entorno** | Calles, vehículos, peatones, pasajeros, tráfico y clima |
| **A — Actuadores** | Dirección, acelerador, freno, señales y claxon |
| **S — Sensores** | Cámaras, radar, lidar, GPS y sensores del vehículo |

El análisis PEAS permite especificar con mayor claridad qué necesita el agente para realizar su tarea.

---

# 17. Características del entorno

No todos los agentes operan bajo las mismas condiciones.

El entorno puede analizarse mediante distintas dimensiones.

---

## 17.1 Totalmente observable vs. parcialmente observable

### Totalmente observable

El agente puede obtener toda la información relevante para seleccionar una acción.

### Parcialmente observable

Existe información relevante que no puede percibir completamente.

Por ejemplo, un taxi autónomo puede observar otros vehículos, pero no conocer directamente las intenciones de todos los conductores.

---

## 17.2 Agente único vs. multiagente

### Agente único

El comportamiento del agente no depende significativamente de otros agentes inteligentes.

Ejemplo:

```text
Resolver un crucigrama
```

### Multiagente

Existen otros agentes cuyas decisiones influyen en el entorno.

Ejemplos:

a) Ajedrez

b) Tráfico vehicular

c) Negociación

d) Robots colaborativos

Los agentes pueden competir, colaborar o combinar ambas formas de interacción.

---

## 17.3 Determinista vs. no determinista

### Determinista

El siguiente estado queda determinado por:

```text
Estado actual + Acción
```

### No determinista

La misma acción puede producir diferentes resultados.

El tráfico real constituye un ejemplo de entorno que no puede considerarse completamente determinista.

---

## 17.4 Episódico vs. secuencial

### Episódico

Cada decisión puede considerarse relativamente independiente.

```text
Percepción → Acción
```

### Secuencial

Las decisiones actuales influyen en situaciones futuras.

```text
Acción actual
      ↓
Nuevo estado
      ↓
Condiciona decisiones futuras
```

La conducción autónoma constituye un problema secuencial.

---

## 17.5 Estático vs. dinámico

### Estático

El entorno no cambia mientras el agente está tomando una decisión.

### Dinámico

El entorno puede cambiar mientras el agente procesa información.

En el tráfico:

```text
El agente analiza
        ↓
Mientras tanto
        ↓
Otros vehículos continúan moviéndose
```

---

## 17.6 Discreto vs. continuo

### Discreto

Los estados y acciones pueden representarse mediante valores separados.

Ejemplo:

```text
Ajedrez
```

### Continuo

Las variables pueden tomar valores dentro de intervalos.

Ejemplo:

```text
Velocidad = 47.3 km/h
Ángulo = 12.6°
Distancia = 8.41 m
```

La conducción presenta numerosas variables continuas.

---

## 17.7 Conocido vs. desconocido

Esta característica se refiere a si el agente conoce cómo funciona el entorno.

### Conocido

El agente conoce las consecuencias de sus acciones o las reglas del entorno.

### Desconocido

El agente debe aprender cómo funciona el entorno.

Es importante distinguir:

```text
Observable
≠
Conocido
```

Un entorno puede ser completamente observable y, al mismo tiempo, desconocido para el agente.

---

# 18. Caracterización del taxi autónomo

Podemos resumir su entorno de la siguiente manera:

| Propiedad | Caracterización |
|---|---|
| Observabilidad | Parcialmente observable |
| Número de agentes | Multiagente |
| Evolución | No determinista |
| Dependencia temporal | Secuencial |
| Cambio | Dinámico |
| Variables | Principalmente continuas |
| Conocimiento | Puede incluir elementos conocidos y aprendidos |

Esta combinación explica por qué la conducción autónoma constituye un problema complejo de Inteligencia Artificial.

---

# 19. ¿Por qué importa conocer el entorno?

Las características del entorno influyen directamente en el diseño del agente.

Un entorno relativamente sencillo:

```text
Observable
+
Determinista
+
Estático
```

puede permitir soluciones simples.

En cambio:

```text
Parcialmente observable
+
Multiagente
+
No determinista
+
Dinámico
```

puede requerir mecanismos para:

a) Representar estados

b) Manejar incertidumbre

c) Predecir acontecimientos

d) Planificar

e) Aprender

f) Tomar decisiones

---

# 20. Visión integrada del agente inteligente

Los conceptos estudiados pueden integrarse mediante el siguiente esquema:

```text
                 ENTORNO
                    ↓
                 Sensores
                    ↓
               Percepciones
                    ↓
          Secuencia de percepciones
                    ↓
          ┌─────────────────────┐
          │       AGENTE        │
          │                     │
          │ Conocimiento        │
          │ Objetivos           │
          │ Razonamiento        │
          │ Aprendizaje         │
          │ Selección de acción │
          └─────────────────────┘
                    ↓
                 Acción
                    ↓
                Actuadores
                    ↓
                 ENTORNO
```

El comportamiento se evalúa mediante una **medida de desempeño**.

La racionalidad consiste en seleccionar acciones que, dada la información disponible, contribuyan al mejor desempeño esperado.

---

# 21. Relación con los enfoques estudiados en 1.2

Un agente no obliga a utilizar un único paradigma de Inteligencia Artificial.

Internamente puede utilizar:

```text
Agente
   │
   ├── Reglas simbólicas
   │
   ├── Modelos probabilísticos
   │
   ├── Redes neuronales
   │
   └── Combinaciones de técnicas
```

Por ello, los enfoques estudiados en 1.2 pueden formar parte del mecanismo utilizado por un agente para seleccionar acciones.

---

# 22. Relación con las arquitecturas de IA

Hasta ahora hemos analizado al agente desde una perspectiva general:

```text
Percibir → Procesar → Actuar
```

Sin embargo, todavía queda una pregunta:

> **¿Cómo se organiza internamente el sistema que realiza ese procesamiento?**

Esta cuestión será retomada en el subtema **1.5 Arquitecturas clásicas y modernas**, donde se estudiarán:

a) Soar

b) ACT-R

c) BDI

d) Arquitecturas híbridas

---

# Síntesis

Los componentes fundamentales de un agente pueden representarse como:

```text
Entorno
   ↓
Sensores
   ↓
Percepciones
   ↓
Agente
   ↓
Acciones
   ↓
Actuadores
   ↓
Entorno
```

A estos elementos se incorporan:

**Medida de desempeño + Racionalidad**

Para especificar sistemáticamente la tarea del agente puede utilizarse:

**PEAS = Performance + Environment + Actuators + Sensors**

> **Un agente inteligente no se define únicamente por procesar información, sino por su capacidad para percibir un entorno, seleccionar acciones y actuar de acuerdo con una medida de desempeño y la información disponible.**

---

## Actividades de aprendizaje

Los ejercicios prácticos de este subtema estarán disponibles en:

[Actividad: PEAS y caracterización del entorno](actividades/actividad-peas-entorno.md)

[Actividad integradora: Diseño de un agente inteligente](actividades/actividad-diseno-agente.md)

[Notebook: Agente percepción–acción](notebooks/agente-percepcion-accion.ipynb)

---

## Recursos del subtema

[Recursos y lecturas](recursos/)

---

## Fuentes base

Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.

Poole, D. L., & Mackworth, A. K. (2023). *Artificial Intelligence: Foundations of Computational Agents* (3rd ed.). Cambridge University Press.

---

[← Volver a la Unidad 1](../)
