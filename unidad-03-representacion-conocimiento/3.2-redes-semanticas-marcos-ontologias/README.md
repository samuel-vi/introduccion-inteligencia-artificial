
# 3.2 Redes semánticas, marcos y ontologías (OWL)

## Unidad 3. Representación del conocimiento y razonamiento

### Propósito del subtema

Comprender diferentes formas estructuradas de representar conocimiento mediante **redes semánticas, marcos y ontologías**, identificando sus componentes, diferencias y aplicaciones, así como reconocer el papel de **OWL** como lenguaje para representar ontologías computables.

La idea central del subtema es pasar de representar conocimiento mediante expresiones lógicas a organizarlo explícitamente mediante **conceptos, propiedades, relaciones y jerarquías**.

---

## 1. De la lógica a las representaciones estructuradas

En el subtema 3.1 se estudió que un sistema de Inteligencia Artificial puede representar conocimiento mediante hechos y reglas.

Por ejemplo:

- PC1 es un equipo
- Router1 es un router
- PC1 está conectado a Router1
- Router1 está operativo

También puede establecerse una regla como:

> Si un equipo está conectado a un router operativo, entonces puede tener acceso a la red.

La lógica permite representar estas afirmaciones con precisión.

Sin embargo, cuando un sistema debe manejar cientos de elementos, por ejemplo:

- Computadoras
- Routers
- Servidores
- Impresoras
- Usuarios
- Servicios

y además relaciones como:

- es-un
- está-conectado-a
- administra
- forma-parte-de
- proporciona-servicio

resulta útil contar con representaciones que permitan observar de manera explícita **cómo están organizados los conceptos y cómo se relacionan entre sí**.

Aquí aparecen las **redes semánticas**, los **marcos** y las **ontologías**.

Podemos pensar entonces en la siguiente progresión:

**Lógica → conceptos y relaciones → estructuras de conocimiento**

La lógica no desaparece. Lo que cambia es la forma en que se organiza y presenta el conocimiento.

---

# 2. Redes semánticas

## ¿Qué es una red semántica?

Una **red semántica** representa conocimiento mediante un grafo compuesto por **nodos y arcos**.

Los nodos representan normalmente:

- Conceptos
- Instancias

Los arcos representan:

- Relaciones entre conceptos o instancias

Ejemplo:

```text
PC1 ──instancia-de──► Computadora

PC1 ──conectado-a──► Router1

Router1 ──instancia-de──► Router

Computadora ──subclase-de──► Dispositivo
```

La principal ventaja es que permite **visualizar directamente la estructura del conocimiento**.

---

## 2.1 Nodos

Un nodo representa una entidad acerca de la cual queremos expresar conocimiento.

Ejemplos:

```text
Dispositivo
Computadora
Router
PC1
Router1
```

**Computadora** representa un concepto o categoría.

**PC1** representa una instancia concreta.

Por ejemplo:

```text
PC1 ──instancia-de──► Computadora
```

puede interpretarse como:

> PC1 es una computadora.

---

## 2.2 Arcos

Los arcos representan relaciones.

Ejemplo:

```text
PC1 ──conectado-a──► Router1
```

significa:

> PC1 está conectado a Router1.

Otro ejemplo:

```text
Computadora ──subclase-de──► Dispositivo
```

significa:

> Una computadora es un tipo de dispositivo.

El significado de una red depende tanto de los nodos como de las relaciones establecidas entre ellos.

---

## 2.3 Relaciones estructurales importantes

### Subclase-de

Permite construir jerarquías.

```text
Laptop ──subclase-de──► Computadora

Computadora ──subclase-de──► Dispositivo
```

### Instancia-de

Relaciona un objeto específico con una clase.

```text
Laptop01 ──instancia-de──► Laptop
```

### Parte-de

Representa composición.

```text
Procesador ──parte-de──► Computadora
```

Es importante distinguir `parte-de` de `subclase-de`.

Un procesador forma parte de una computadora, pero no es un tipo de computadora.

---

## 2.4 Jerarquías y herencia

Una de las ventajas de organizar conceptos jerárquicamente es la **herencia de propiedades**.

Ejemplo:

```text
Dispositivo
    │
    └── Computadora
            │
            └── Laptop
                    │
                    └── Laptop01
```

Si definimos una propiedad general:

```text
Dispositivo → necesita energía
```

las clases e instancias más específicas pueden acceder a dicha propiedad a través de la jerarquía.

Esto evita almacenar conocimiento repetitivo como:

```text
PC1 necesita energía
PC2 necesita energía
Laptop01 necesita energía
Servidor1 necesita energía
```

---

## 2.5 Ejemplo: red informática

```text
Dispositivo
    ▲
    │ subclase-de
Computadora
    ▲
    │ instancia-de
   PC1

PC1 ──conectado-a──► Router1

Router1 ──instancia-de──► Router
```

La representación permite identificar:

- Qué entidades existen
- A qué categorías pertenecen
- Cómo se relacionan

---

## 2.6 Ejemplo: sistema académico

```text
Persona
   ▲
   │
Estudiante
   ▲
   │
EstudianteMaestria
   ▲
   │
  Ana
```

Además:

```text
Ana ──inscrito-en──► InteligenciaArtificial
```

La red indica que Ana es estudiante de maestría, un estudiante de maestría es un estudiante y un estudiante es una persona.

---

## 2.7 Limitaciones de las redes semánticas

Las redes semánticas son intuitivas y visuales, pero presentan algunas limitaciones:

- No existe una única semántica universal para todas las variantes
- La interpretación de relaciones puede depender de la convención utilizada
- Una red muy grande puede resultar difícil de mantener
- Algunas relaciones complejas requieren estructuras adicionales

Esto conduce a otra forma de representación: **los marcos**.

---

# 3. Marcos o frames

## ¿Qué es un marco?

Un **marco** es una estructura utilizada para representar un concepto, objeto o situación mediante un conjunto organizado de propiedades.

Mientras que una red semántica enfatiza:

**las relaciones entre nodos**

un marco enfatiza:

**la descripción estructurada de un concepto**

Ejemplo:

```text
MARCO: Computadora

Propiedades:
tipo
sistema-operativo
memoria
procesador

Relaciones:
conectado-a
administrado-por
```

---

## 3.1 Marco clase

Representa un concepto general.

Ejemplo:

```text
MARCO CLASE: Computadora

Propiedades:
memoria
procesador
sistema-operativo
direccion-IP
```

Este marco describe qué características puede tener una computadora.

---

## 3.2 Marco instancia

Representa un objeto concreto.

Ejemplo:

```text
MARCO INSTANCIA: PC1

Clase: Computadora

memoria: 16 GB
procesador: Intel Core i7
sistema-operativo: Linux
direccion-IP: 192.168.1.10
```

La relación conceptual es:

**Computadora → clase**

**PC1 → instancia**

---

## 3.3 Ranuras, valores y facetas

Las propiedades de un marco también se conocen como **ranuras** (*slots*).

Ejemplo:

```text
MARCO: Sensor

Ranuras:
tipo
unidad-medida
rango
ubicacion
estado
```

Una instancia podría ser:

```text
Sensor01

tipo = temperatura
unidad-medida = grados Celsius
ubicacion = sala de servidores
estado = activo
```

Las **facetas** permiten describir características adicionales de una propiedad, por ejemplo:

- Tipo de valor
- Cardinalidad
- Valores permitidos
- Valores por defecto

Para este subtema basta con comprender que las facetas ayudan a especificar **cómo puede utilizarse una propiedad**.

---

## 3.4 Ejemplo: sistema IoT

### Marco clase

```text
Sensor

Propiedades:
tipo
unidad
ubicacion
estado
```

### Marco instancia

```text
SensorT01

Clase: Sensor
tipo: temperatura
unidad: grados Celsius
ubicacion: SalaServidor
estado: activo
```

También puede especializarse:

```text
Sensor
   ↓
SensorTemperatura
   ↓
SensorT01
```

Nuevamente aparece la idea:

**jerarquía + especialización + herencia**

---

# 4. De marcos a ontologías

Las redes semánticas permiten representar relaciones.

Los marcos permiten organizar propiedades alrededor de conceptos.

Pero existe otra necesidad:

> ¿Cómo podemos construir una representación formal de un dominio que pueda ser compartida, reutilizada y procesada por diferentes sistemas?

Aquí aparecen las **ontologías**.

---

# 5. Ontologías

## ¿Qué es una ontología?

En informática, una ontología describe formalmente los conceptos relevantes de un dominio y las relaciones que existen entre ellos.

Una definición ampliamente utilizada establece que una ontología es una:

> **Especificación formal de una conceptualización compartida.**

Podemos interpretar cada término.

### Conceptualización

Identificamos los elementos relevantes de un dominio.

Ejemplo:

```text
Persona
Estudiante
Profesor
Asignatura
Programa
```

### Compartida

Los términos deben tener un significado acordado por quienes utilizan la ontología.

### Formal

Las relaciones y restricciones deben expresarse con suficiente precisión para ser procesadas computacionalmente.

Una ontología no es solamente un diagrama con conceptos conectados, sino una representación estructurada con significado explícito.

---

## 5.1 Componentes de una ontología

| Elemento | Función | Ejemplo |
|---|---|---|
| Clase | Representa una categoría | Computadora |
| Individuo | Representa una entidad concreta | PC1 |
| Propiedad | Describe una característica | memoria |
| Relación | Conecta entidades | conectado-a |
| Jerarquía | Organiza clases | Laptop es subclase de Computadora |
| Axioma | Establece condiciones o restricciones | Toda laptop es computadora |

---

## 5.2 Ejemplo de ontología de una red informática

### Clases

```text
Dispositivo
Computadora
Router
Servidor
```

### Taxonomía

```text
Dispositivo
 ├── Computadora
 ├── Router
 └── Servidor
```

### Individuos

```text
PC1 → Computadora
Router1 → Router
Servidor1 → Servidor
```

### Relaciones

```text
PC1 conectado-a Router1
Servidor1 conectado-a Router1
```

### Propiedades

```text
PC1 tieneIP "192.168.1.10"
```

Ahora estamos construyendo un **modelo explícito del dominio**.

---

# 6. ¿En qué se diferencia una ontología de una red semántica?

Visualmente pueden parecer similares porque ambas utilizan conceptos y relaciones.

La diferencia principal es que una ontología busca una representación **más formal, explícita, reutilizable y compartida**.

Por ejemplo, podemos establecer:

```text
Laptop es subclase de Computadora
Computadora es subclase de Dispositivo
Laptop01 es individuo de Laptop
```

Además, pueden establecerse restricciones y axiomas sobre conceptos y propiedades.

---

# 7. OWL

## ¿Qué es OWL?

**OWL (Web Ontology Language)** es un lenguaje diseñado para representar ontologías de manera computable.

En términos sencillos:

> Una ontología describe el conocimiento que queremos representar; OWL proporciona un lenguaje estandarizado para expresarlo computacionalmente.

OWL 2 permite representar:

- Clases
- Propiedades
- Individuos
- Valores de datos
- Jerarquías
- Restricciones

---

## 7.1 Clases

Una clase representa una categoría.

Ejemplo:

```text
Dispositivo
Computadora
Router
```

Podemos establecer:

```text
Computadora es subclase de Dispositivo
Router es subclase de Dispositivo
```

---

## 7.2 Individuos

Representan objetos concretos.

Ejemplo:

```text
PC1
PC2
Router1
```

Podemos indicar:

```text
PC1 pertenece a Computadora
Router1 pertenece a Router
```

---

## 7.3 Propiedades

OWL permite representar relaciones entre entidades y propiedades asociadas con datos.

Ejemplos:

```text
conectadoA
administra
tieneDireccionIP
```

Podemos representar:

```text
PC1 conectadoA Router1
```

o:

```text
PC1 tieneDireccionIP "192.168.1.10"
```

---

## 7.4 ¿Por qué es importante OWL?

OWL permite expresar una ontología con una estructura formal que puede ser procesada por herramientas computacionales.

Esto hace posible:

- Compartir conocimiento
- Reutilizar modelos
- Verificar consistencia
- Obtener conocimiento implícito mediante razonamiento

Estos últimos aspectos se retomarán con mayor profundidad en los siguientes subtemas.

---

# 8. Ejemplo integrado

Consideremos:

- PC1 es una computadora
- Router1 es un router
- PC1 está conectado a Router1

## Red semántica

```text
PC1 ──instancia-de──► Computadora
Computadora ──subclase-de──► Dispositivo
PC1 ──conectado-a──► Router1
Router1 ──instancia-de──► Router
```

**Énfasis:** relaciones entre elementos.

---

## Marco

```text
MARCO: Computadora

Propiedades:
memoria
sistema-operativo
direccion-IP
conectado-a
```

Instancia:

```text
PC1

Clase: Computadora
memoria: 16 GB
sistema-operativo: Linux
conectado-a: Router1
```

**Énfasis:** estructura y propiedades del objeto.

---

## Ontología

```text
CLASES

Dispositivo
Computadora
Router

JERARQUIA

Computadora → Dispositivo
Router → Dispositivo

INDIVIDUOS

PC1 → Computadora
Router1 → Router

RELACION

PC1 conectado-a Router1
```

**Énfasis:** conceptualización formal y compartida del dominio.

---

# 9. Comparación general

| Característica | Red semántica | Marco | Ontología |
|---|---|---|---|
| Elemento central | Relaciones | Conceptos estructurados | Conceptualización formal |
| Representación habitual | Nodos y arcos | Ranuras y valores | Clases, propiedades e individuos |
| Jerarquías | Sí | Sí | Sí |
| Instancias | Sí | Sí | Sí |
| Herencia | Puede utilizarse | Importante | Puede formalizarse |
| Formalidad | Variable | Estructurada | Mayor formalización |
| Reutilización | Dependiente del formalismo | Dependiente del sistema | Objetivo importante |
| Lenguaje estándar Web | No necesariamente | No | OWL |

---

# 10. ¿Cuál debemos utilizar?

No existe una representación universalmente mejor.

Si el objetivo principal es visualizar relaciones entre conceptos, una **red semántica** puede resultar muy intuitiva.

Si necesitamos describir detalladamente propiedades y valores de entidades estructuradas, los **marcos** pueden resultar apropiados.

Si queremos construir una representación formal, reutilizable y compartida de un dominio, una **ontología** ofrece mayores posibilidades.

La pregunta correcta es:

> **¿Qué representación resulta adecuada para el conocimiento que necesitamos modelar?**

---

# 11. Idea fundamental

La evolución conceptual del subtema puede resumirse así:

**Red semántica**

Relaciona conceptos mediante nodos y arcos.

↓

**Marco**

Agrupa propiedades y relaciones alrededor de conceptos estructurados.

↓

**Ontología**

Formaliza conceptos, relaciones, propiedades, individuos y restricciones.

↓

**OWL**

Permite expresar ontologías de manera computable y estandarizada.

La pregunta central del subtema es:

> **¿Cómo podemos organizar el conocimiento de manera que tanto las personas como los sistemas de IA puedan comprender su estructura y relaciones?**

---

# 12. Conexión con el siguiente subtema

Hasta ahora hemos estudiado principalmente **cómo representar el conocimiento**.

El siguiente paso es estudiar **cómo utilizar ese conocimiento para obtener nuevas conclusiones**.

Esto conduce a:

## 3.3 Sistemas de inferencia: hacia adelante y hacia atrás

---

## Recursos del subtema

- [Recursos complementarios](./recursos/README.md)
- [Actividad de aprendizaje](./actividades/README.md)
- [Práctica con Protégé y OWL](./practica/README.md)
- [Imágenes](./imagenes/)

---

## Referencias principales

Gómez-Pérez, A., Fernández-López, M., Corcho, O., Suárez de Figueroa Baonza, M. C., et al. Material sobre redes semánticas, marcos y ontologías utilizado como fuente principal del subtema.

Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.

Noy, N. F., & McGuinness, D. L. (2001). *Ontology Development 101: A Guide to Creating Your First Ontology*. Stanford University.

W3C. (2012). *OWL 2 Web Ontology Language Primer (Second Edition)*.

---

[← Volver a la Unidad 3](../README.md)
