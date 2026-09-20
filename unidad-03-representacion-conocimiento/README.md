# 3.3 Sistemas de inferencia: hacia adelante y hacia atrás

## Propósito del subtema

Comprender cómo un sistema de Inteligencia Artificial puede utilizar una **base de hechos** y una **base de reglas** para obtener nuevas conclusiones, mediante los mecanismos de **encadenamiento hacia adelante** (*forward chaining*) y **encadenamiento hacia atrás** (*backward chaining*).

Este subtema da continuidad a lo estudiado previamente:

- En **3.1** se utilizaron hechos, reglas y expresiones lógicas para representar conocimiento.
- En **3.2** se estudiaron formas estructuradas de organizar conceptos, propiedades y relaciones.
- En **3.3** se estudiará cómo un sistema puede **razonar con ese conocimiento**.

La idea central puede resumirse así:

```text
Representar conocimiento
          ↓
   Hechos y reglas
          ↓
   Motor de inferencia
          ↓
 Nuevas conclusiones
```

> **Idea clave:** una base de conocimiento contiene información, pero el motor de inferencia permite utilizarla para obtener conocimiento que no estaba expresado explícitamente.

---

## 1. De representar conocimiento a razonar con él

Hasta este punto hemos estudiado distintas maneras de representar conocimiento.

Por ejemplo, podemos registrar los siguientes hechos:

```text
El equipo no enciende.
El indicador LED está apagado.
```

También podemos representar una regla:

```text
SI el equipo no enciende
Y el indicador LED está apagado
ENTONCES revisar la alimentación eléctrica.
```

Los dos primeros enunciados describen información conocida. La regla, en cambio, establece una relación entre condiciones y una posible conclusión.

Un sistema de inferencia utiliza ambos tipos de conocimiento para responder una pregunta como:

> **¿Qué debería revisarse si el equipo no enciende y el LED está apagado?**

El razonamiento sería:

```text
Equipo no enciende
        +
LED apagado
        ↓
Se cumplen las condiciones
de una regla
        ↓
Revisar alimentación eléctrica
```

La conclusión **“revisar alimentación eléctrica”** no estaba registrada como un hecho inicial. Se obtiene al aplicar una regla sobre los hechos disponibles.

A este proceso de obtener conclusiones a partir de conocimiento existente lo llamaremos **inferencia**.

### 1.1 ¿Qué significa inferir?

En el contexto de la IA simbólica, inferir significa **derivar nueva información a partir de hechos y reglas disponibles**.

Por ejemplo:

```text
Hecho 1: El suelo está seco.
Hecho 2: No está lloviendo.

Regla:
SI el suelo está seco
Y no está lloviendo
ENTONCES activar el riego.
```

A partir de los dos hechos iniciales, el sistema puede obtener:

```text
Nuevo hecho: Activar el riego.
```

El proceso puede visualizarse así:

```text
Suelo seco + No llueve
          ↓
      Aplicar regla
          ↓
     Activar riego
```

Este ejemplo es deliberadamente sencillo. Lo importante no es el sistema de riego, sino observar que una regla permite **transformar conocimiento disponible en una nueva conclusión**.

---

## 2. ¿Qué es un sistema de inferencia?

Un **sistema de inferencia** es un mecanismo que examina el conocimiento disponible y aplica reglas para determinar qué conclusiones pueden obtenerse.

En su forma más sencilla podemos imaginarlo como tres elementos:

```text
Base de hechos
      +
Base de reglas
      ↓
Motor de inferencia
      ↓
Conclusiones
```

En la práctica, el motor de inferencia compara las condiciones de las reglas con la información disponible y determina qué reglas pueden utilizarse.

### Ejemplo

Supongamos que tenemos:

```text
Hechos:
Ana está inscrita.
Ana tiene una cuenta activa.

Regla:
SI un estudiante está inscrito
Y tiene una cuenta activa
ENTONCES puede acceder al curso.
```

Como ambas condiciones se cumplen, el sistema puede obtener:

```text
Ana puede acceder al curso.
```

Visualmente:

```text
Inscrita(Ana)
      +
CuentaActiva(Ana)
      ↓
Aplicación de la regla
      ↓
PuedeAcceder(Ana)
```

Este mecanismo es la base de muchos sistemas simbólicos y sistemas expertos.

---

## 3. Componentes básicos de un sistema de inferencia

Para entender cómo funciona un sistema de inferencia, utilizaremos cuatro componentes básicos:

```text
Base de hechos
      +
Base de reglas
      ↓
Motor de inferencia
      ↓
Memoria de trabajo / conocimiento derivado
```

### 3.1 Base de hechos

La **base de hechos** contiene información que el sistema considera disponible en un momento determinado.

Ejemplo:

```text
equipo_no_enciende
led_apagado
```

Los hechos constituyen el punto de partida del razonamiento.

### 3.2 Base de reglas

La **base de reglas** contiene conocimiento que establece qué conclusión puede obtenerse cuando determinadas condiciones se cumplen.

Ejemplo:

```text
SI equipo_no_enciende
Y led_apagado
ENTONCES revisar_alimentacion
```

Una regla tiene dos partes principales:

```text
CONDICIONES  →  CONCLUSIÓN
```

También pueden denominarse:

```text
Antecedente  →  Consecuente
```

### 3.3 Motor de inferencia

El **motor de inferencia** es el componente encargado de utilizar los hechos y las reglas.

De manera simplificada realiza el siguiente proceso:

```text
1. Examinar los hechos disponibles
              ↓
2. Buscar reglas cuyas condiciones se cumplan
              ↓
3. Aplicar una regla
              ↓
4. Obtener una nueva conclusión
              ↓
5. Incorporar el nuevo conocimiento
```

Más adelante veremos que el orden en que se realiza este razonamiento depende de la estrategia utilizada:

- **Encadenamiento hacia adelante:** comienza con los hechos.
- **Encadenamiento hacia atrás:** comienza con una meta o pregunta.

### 3.4 Memoria de trabajo

Durante el proceso de inferencia pueden aparecer nuevos hechos.

La **memoria de trabajo** representa el conjunto de información que está disponible durante el razonamiento, incluyendo hechos iniciales y, dependiendo del sistema, conclusiones obtenidas.

Ejemplo:

```text
Estado inicial:
equipo_no_enciende
led_apagado
```

Después de aplicar una regla:

```text
equipo_no_enciende
led_apagado
revisar_alimentacion
```

La nueva información puede ser utilizada en pasos posteriores.

---

## 4. Reglas de producción

Una forma sencilla de representar conocimiento procedimental en sistemas simbólicos es mediante **reglas de producción**.

Su estructura general es:

```text
SI condición
ENTONCES conclusión
```

También pueden contener varias condiciones:

```text
SI condición_1
Y condición_2
ENTONCES conclusión
```

### 4.1 Antecedente y consecuente

Podemos dividir una regla en:

```text
SI A Y B  →  ENTONCES C
```

donde:

- **A y B** forman el antecedente o conjunto de condiciones.
- **C** es el consecuente o conclusión.

Ejemplo:

```text
SI suelo_seco
Y no_llueve
ENTONCES activar_riego
```

### 4.2 ¿Cuándo puede aplicarse una regla?

Una regla puede aplicarse cuando sus condiciones se encuentran satisfechas por los hechos disponibles.

Ejemplo:

```text
Hechos:
suelo_seco
no_llueve
```

Regla:

```text
SI suelo_seco
Y no_llueve
ENTONCES activar_riego
```

Como ambas condiciones están presentes, la regla puede producir:

```text
activar_riego
```

Si solamente conocemos:

```text
suelo_seco
```

no podemos aplicar esa regla todavía, porque falta verificar:

```text
no_llueve
```

> **Una regla no se ejecuta simplemente porque exista. Sus condiciones deben satisfacerse de acuerdo con el conocimiento disponible.**

### 4.3 Un mismo conocimiento puede participar en varias reglas

Considere:

```text
R1:
SI suelo_seco
Y no_llueve
ENTONCES activar_riego

R2:
SI activar_riego
ENTONCES abrir_valvula
```

Con los hechos:

```text
suelo_seco
no_llueve
```

podemos obtener una cadena sencilla:

```text
suelo_seco + no_llueve
          ↓
         R1
          ↓
    activar_riego
          ↓
         R2
          ↓
     abrir_valvula
```

Este ejemplo muestra por qué hablamos de **encadenamiento**: la conclusión obtenida por una regla puede utilizarse para satisfacer las condiciones de otra.

---

## Síntesis hasta este punto

| Elemento | Función |
|---|---|
| Hecho | Representa información conocida |
| Regla | Relaciona condiciones con una conclusión |
| Base de hechos | Almacena los hechos disponibles |
| Base de reglas | Almacena las reglas del dominio |
| Motor de inferencia | Determina qué reglas pueden aplicarse |
| Memoria de trabajo | Mantiene información disponible y derivada |
| Inferencia | Proceso mediante el cual se obtienen nuevas conclusiones |

La estructura general es:

```text
HECHOS + REGLAS
      ↓
MOTOR DE INFERENCIA
      ↓
NUEVAS CONCLUSIONES
```

A partir de esta base estudiaremos dos estrategias:

```text
                   SISTEMAS DE INFERENCIA
                           │
              ┌────────────┴────────────┐
              ↓                         ↓
     Hacia adelante                Hacia atrás
   Forward chaining              Backward chaining
              │                         │
        Parte de datos              Parte de una meta
```

---

## 5. Encadenamiento hacia adelante

> Se desarrollará en la siguiente etapa del subtema.

## 6. Encadenamiento hacia atrás

> Se desarrollará en la siguiente etapa del subtema.

## 7. Comparación: forward chaining vs. backward chaining

> Se desarrollará en la siguiente etapa del subtema.

## 8. Variables y equiparación

> Se desarrollará en la siguiente etapa del subtema.

## 9. Unificación básica

> Se desarrollará en la siguiente etapa del subtema.

## 10. Ejemplo integrado de sistema experto

> Se desarrollará en la siguiente etapa del subtema.

## 11. Implementación computacional

> Se desarrollará en la siguiente etapa del subtema.

## 12. Limitaciones de la inferencia determinista

> Se desarrollará en la siguiente etapa del subtema.

## 13. Conexión con el subtema 3.4

> Se desarrollará en la siguiente etapa del subtema.

---

## Referencias base

- Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.
- Temario oficial de la asignatura **Introducción a la Inteligencia Artificial**, Maestría en Sistemas Computacionales, TecNM.
- Instrumentación Didáctica de Asignaturas de Posgrado, TecNM, revisión 001.

---

## Navegación

- [← Volver a la Unidad 3](../README.md)
- [← Subtema 3.2: Redes semánticas, marcos y ontologías](../3.2-redes-semanticas-marcos-ontologias/README.md)
