# 2.1 Formulación de problemas para Inteligencia Artificial

## Propósito

Comprender cómo transformar una necesidad del mundo real en un problema suficientemente definido para establecer **qué debe resolver un sistema de Inteligencia Artificial antes de seleccionar una técnica o algoritmo**.

---

## 1. ¿Qué significa formular un problema?

Una necesidad suele expresarse inicialmente de manera general.

Por ejemplo:

> **Mejorar la movilidad dentro de una ciudad utilizando Inteligencia Artificial.**

Esta descripción todavía no define un problema computacional concreto.

A partir de ella podrían plantearse problemas diferentes:

a) Predecir el nivel de tráfico

b) Detectar congestión vehicular

c) Encontrar la ruta más corta

d) Planificar una secuencia de desplazamientos

e) Detectar situaciones anómalas

Por tanto, una misma necesidad puede originar distintos problemas de Inteligencia Artificial.

Russell y Norvig señalan que, antes de buscar una solución, es necesario formular el objetivo y construir una representación adecuada del problema [1].

---

## 2. Elementos básicos de la formulación

Para este curso utilizaremos la siguiente estructura:

| Elemento | Pregunta |
|---|---|
| **Objetivo** | ¿Qué debe conseguir el sistema? |
| **Entradas** | ¿Qué información está disponible? |
| **Salida** | ¿Qué resultado debe producir? |
| **Restricciones** | ¿Qué condiciones deben respetarse? |
| **Criterio de éxito** | ¿Cómo se evaluará la solución? |
| **Entorno** | ¿En qué condiciones opera? |
| **Tipo de problema** | ¿Qué clase de problema de IA representa? |

El proceso puede resumirse como:

```text
Necesidad
    ↓
Objetivo
    ↓
Entradas y salida
    ↓
Restricciones
    ↓
Criterio de éxito
    ↓
Abstracción
    ↓
Tipo de problema
    ↓
Representación
```

> Esta estructura es una síntesis didáctica utilizada en la asignatura para facilitar la formulación inicial de problemas.

---

## 3. Objetivo, entradas y salida

El **objetivo** establece qué debe lograr el sistema.

Ejemplo:

> Encontrar una ruta entre un origen y un destino minimizando la distancia recorrida.

### Entradas

```text
Origen
Destino
Mapa
Distancias
Calles disponibles
```

### Salida

```text
Origen → Punto A → Punto B → Destino
```

Definir claramente las entradas y la salida permite convertir una necesidad general en un problema susceptible de representarse computacionalmente.

Poole y Mackworth destacan que un problema computacional requiere especificar adecuadamente la información disponible, las posibles acciones y el objetivo que debe alcanzarse [2].

---

## 4. Restricciones y criterio de éxito

Las soluciones deben respetar las condiciones reales del problema.

En el ejemplo de rutas podrían existir restricciones como:

a) Calles cerradas

b) Sentidos de circulación

c) Distancia máxima

d) Tiempo disponible

También es necesario establecer el **criterio de éxito**.

Por ejemplo:

```text
Minimizar distancia
```

no necesariamente significa:

```text
Minimizar tiempo
```

Una ruta más corta puede tardar más debido al tráfico.

Por ello:

> **El criterio de éxito debe representar lo que realmente se desea alcanzar u optimizar.**

---

## 5. Abstracción

Los problemas reales contienen información que no siempre es relevante para su solución.

Para calcular una ruta pueden ser importantes:

```text
Lugares
Calles
Distancias
Restricciones
```

pero probablemente no:

```text
Color del automóvil
Nombre del conductor
Música reproducida
```

La **abstracción** consiste en conservar los elementos necesarios para resolver el problema y omitir aquellos que no afectan la solución.

Russell y Norvig utilizan este principio al representar problemas mediante estados y acciones relevantes, evitando modelar todos los detalles del mundo real [1].

---

## 6. Identificación del tipo de problema

Una vez definido el problema, conviene identificar qué clase de tarea de IA representa.

| Tipo de problema | Ejemplo |
|---|---|
| **Clasificación** | Spam / No spam |
| **Predicción** | Estimar una demanda futura |
| **Clustering** | Descubrir grupos de usuarios |
| **Detección de anomalías** | Identificar comportamiento inusual |
| **Búsqueda** | Encontrar una ruta |
| **Planificación** | Determinar una secuencia de acciones |
| **Satisfacibilidad** | Encontrar valores que cumplan restricciones |
| **Búsqueda adversarial** | Tomar decisiones frente a un oponente |

Esta clasificación ayuda a determinar posteriormente qué representación y técnicas pueden resultar apropiadas.

---

## 7. Problema y algoritmo no son lo mismo

Una formulación incorrecta sería:

> “El problema consiste en utilizar A*.”

A* es un algoritmo, no el problema.

Una formulación más adecuada sería:

> **Encontrar una ruta entre un origen y un destino minimizando el costo del recorrido.**

La secuencia correcta es:

```text
Problema
    ↓
Representación
    ↓
Selección de técnica
    ↓
Algoritmo
```

La selección del algoritmo ocurre **después de comprender y representar el problema**.

---

## 8. Ejemplo integrado

### Situación

Una persona necesita desplazarse dentro de una ciudad.

### Objetivo

Encontrar una ruta que minimice la distancia.

### Entradas

```text
Origen
Destino
Mapa
Distancias
```

### Salida

```text
Secuencia de lugares hasta llegar al destino
```

### Restricciones

```text
Utilizar únicamente calles disponibles
Respetar sentidos de circulación
```

### Criterio de éxito

```text
Llegar al destino con la menor distancia posible
```

### Tipo de problema

```text
Búsqueda
```

Una vez formulado el problema, la siguiente pregunta es:

> **¿Cómo representarlo para que un algoritmo pueda resolverlo?**

Esto conduce al estudio de **espacios de estado y operadores**.

---

## Idea clave

> **Formular correctamente un problema significa definir qué debe resolver el sistema antes de decidir cómo lo resolverá.**

---

## Recurso visual

[Consultar proceso de formulación de un problema](imagenes/proceso-formulacion-problema.png)

---

## Referencias

[1] Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.

[2] Poole, D. L., & Mackworth, A. K. (2023). *Artificial Intelligence: Foundations of Computational Agents* (3rd ed.). Cambridge University Press.  
https://www.cs.ubc.ca/~poole/aibook/3e/html/ArtInt3e.html

[3] Google for Developers. *Problem Framing for Machine Learning*.  
https://developers.google.com/machine-learning/problem-framing

---

## Recursos complementarios

[Consultar recursos del subtema](recursos/)

---

## Actividad de aprendizaje

[Formulación de un problema de Inteligencia Artificial](actividades/actividad-formulacion-problema.md)

---

[← Volver a la Unidad 2](../)
