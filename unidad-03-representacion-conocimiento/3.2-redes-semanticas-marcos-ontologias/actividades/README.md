# Actividad de aprendizaje 3.2 — Modelado comparativo de un dominio

## Unidad 3. Representación del conocimiento y razonamiento

### Subtema 3.2 Redes semánticas, marcos y ontologías (OWL)

---

## Propósito

Aplicar los conceptos estudiados en el subtema 3.2 mediante la representación de un mismo dominio utilizando:

a) Una **red semántica**

b) Un **marco**

c) Una **ontología**

El objetivo es que el estudiante compare las tres formas de representación y explique qué información resulta más clara, estructurada o formal en cada una.

---

# 1. Situación de aprendizaje

Seleccione un dominio pequeño que contenga:

- Al menos 4 conceptos
- Al menos 2 niveles jerárquicos
- Al menos 3 relaciones
- Al menos 3 individuos o instancias
- Al menos 3 propiedades

El dominio debe ser suficientemente sencillo para poder representarlo de manera completa.

Puede elegir uno de los siguientes:

a) **Dominio académico**  
Ejemplo: Persona, Estudiante, Profesor, Asignatura, Programa

b) **Sistema IoT**  
Ejemplo: Dispositivo, Sensor, SensorTemperatura, Gateway, Ubicación

c) **Sistema de biblioteca**  
Ejemplo: Recurso, Libro, Revista, Usuario, Préstamo

d) **Sistema apícola**  
Ejemplo: Apiario, Colmena, Sensor, Apicultor, Medición

e) Otro dominio relacionado con su área de interés, previa justificación breve

---

# 2. Parte A — Identificación del conocimiento

Antes de modelar, describa el dominio mediante una tabla como la siguiente:

| Tipo de elemento | Ejemplo |
|---|---|
| Conceptos | Sensor, Dispositivo |
| Instancias | SensorT01 |
| Propiedades | ubicación, estado |
| Relaciones | conectado-a, instalado-en |
| Jerarquías | SensorTemperatura subclase-de Sensor |

Incluya como mínimo:

a) 4 conceptos

b) 3 individuos

c) 3 propiedades

d) 3 relaciones

e) 2 relaciones jerárquicas

---

# 3. Parte B — Red semántica

Construya una red semántica del dominio seleccionado.

La red deberá incluir:

a) Conceptos

b) Instancias

c) Relaciones `subclase-de`

d) Relaciones `instancia-de`

e) Al menos una relación propia del dominio

Ejemplo:

```text
SensorTemperatura ──subclase-de──► Sensor

SensorT01 ──instancia-de──► SensorTemperatura

SensorT01 ──instalado-en──► Sala1
```

## Pregunta de análisis

Explique:

> ¿Qué conocimiento resulta fácil de comprender visualmente mediante la red semántica?

---

# 4. Parte C — Marco

Seleccione uno de los conceptos principales del dominio y represéntelo mediante un **marco clase**.

Posteriormente represente uno de sus individuos mediante un **marco instancia**.

Ejemplo:

```text
MARCO CLASE: Sensor

Propiedades:
tipo
ubicacion
estado
unidad-medida
```

Instancia:

```text
MARCO INSTANCIA: SensorT01

Clase: SensorTemperatura
ubicacion: Sala1
estado: activo
unidad-medida: grados Celsius
```

## Pregunta de análisis

Explique:

> ¿Qué información resulta más clara en un marco que en una red semántica?

---

# 5. Parte D — Ontología

Transforme el dominio en una pequeña ontología.

Defina:

a) Clases

b) Subclases

c) Individuos

d) Propiedades de objeto

e) Propiedades de datos

f) Al menos un axioma o restricción sencilla

Ejemplo:

```text
Clase: Sensor
Clase: SensorTemperatura

SensorTemperatura subClassOf Sensor

Individuo:
SensorT01 type SensorTemperatura

Propiedad de objeto:
instaladoEn

Propiedad de datos:
tieneEstado
```

La ontología puede representarse de forma conceptual en el documento y, opcionalmente, implementarse en Protégé.

---

# 6. Parte E — Comparación

Compare las tres representaciones.

Complete una tabla como la siguiente:

| Criterio | Red semántica | Marco | Ontología |
|---|---|---|---|
| Claridad visual | | | |
| Representación de relaciones | | | |
| Representación de propiedades | | | |
| Jerarquías | | | |
| Instancias | | | |
| Formalización | | | |
| Posibilidad de inferencia | | | |

No se busca identificar una representación como “la mejor”, sino explicar **qué aporta cada una**.

---

# 7. Parte F — Reflexión

Responda brevemente:

a) ¿Qué diferencia existe entre un concepto y una instancia?

b) ¿Qué diferencia existe entre una relación `subclase-de` y una relación `parte-de`?

c) ¿Qué ventaja ofrecen los marcos cuando un concepto tiene muchas propiedades?

d) ¿Qué aporta una ontología que no aparece necesariamente en una red semántica?

e) ¿Por qué OWL resulta útil para representar ontologías computables?

f) ¿Qué representación elegiría para su dominio y por qué?

---

# 8. Producto a entregar

Entregue un documento de **3 a 5 páginas**, en formato PDF o Markdown, que incluya:

a) Descripción breve del dominio

b) Identificación de conceptos, propiedades, relaciones e instancias

c) Red semántica

d) Marco clase

e) Marco instancia

f) Ontología conceptual

g) Tabla comparativa

h) Reflexión final

Si se implementó la ontología en Protégé, puede anexarse también el archivo `.owl`.

---

# 9. Criterios de evaluación

| Criterio | Porcentaje |
|---|---:|
| Identificación correcta de conceptos, relaciones e instancias | 15 % |
| Red semántica | 20 % |
| Marco clase e instancia | 20 % |
| Ontología conceptual | 25 % |
| Comparación entre representaciones | 10 % |
| Reflexión y argumentación | 10 % |
| **Total** | **100 %** |

---

# 10. Evidencia de aprendizaje esperada

Al finalizar la actividad, el estudiante deberá ser capaz de:

a) Representar un mismo dominio mediante diferentes formalismos

b) Distinguir concepto, clase, instancia, propiedad y relación

c) Explicar la función de jerarquías y herencia

d) Diferenciar redes semánticas, marcos y ontologías

e) Reconocer el papel de OWL en la formalización computable del conocimiento

---

# 11. Relación con el siguiente subtema

Esta actividad se centra en **cómo estructurar y representar conocimiento**.

En el subtema 3.3 se estudiará cómo un sistema puede utilizar ese conocimiento para obtener nuevas conclusiones mediante:

- Encadenamiento hacia adelante
- Encadenamiento hacia atrás
- Reglas
- Hechos
- Consultas

---

## Referencias de apoyo

- Material del subtema 3.2
- Noy, N. F., & McGuinness, D. L. (2001). *Ontology Development 101*
- W3C. *OWL 2 Web Ontology Language Primer*
- Protégé — Stanford University

---

[← Volver al subtema 3.2](../README.md)
