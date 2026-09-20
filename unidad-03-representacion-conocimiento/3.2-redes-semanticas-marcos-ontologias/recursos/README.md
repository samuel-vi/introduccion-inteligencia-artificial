
# Recursos complementarios — 3.2 Redes semánticas, marcos y ontologías (OWL)

## Propósito

Estos recursos complementan el apunte del subtema **3.2 Redes semánticas, marcos y ontologías (OWL)**. La selección busca que el estudiante pueda profundizar en los conceptos centrales sin depender de bibliografía cerrada o de pago.

La recomendación es utilizarlos de forma progresiva: comenzar con la representación mediante redes semánticas y marcos, continuar con los fundamentos de ontologías y finalizar con OWL 2 y Protégé.

---

## 1. Lectura principal del subtema

### Redes semánticas, marcos y ontologías

**Recurso del curso:** capítulos sobre **Redes semánticas y marcos** y **Ontologías**.

Este material constituye la lectura principal para comprender:

- Formalismos de representación del conocimiento
- Redes semánticas
- Nodos, arcos, conceptos e instancias
- Relaciones `subclase-de`, `instancia` y `parte-de`
- Jerarquías y herencia de propiedades
- Marcos clase y marcos instancia
- Ranuras, propiedades y facetas
- Componentes de una ontología
- Clases, relaciones, axiomas e instancias
- Metodologías para el desarrollo de ontologías

> **Importante:** la sección dedicada a OWL en este documento corresponde principalmente a una etapa anterior del estándar. Para estudiar OWL se utilizará como referencia actual el **OWL 2 Primer del W3C**.

Si el archivo PDF se almacena en esta misma carpeta del repositorio, puede enlazarse de la siguiente manera:

[Consultar PDF del curso](./Redes%20Semanticas%20y%20ontologias.pdf)

---

## 2. Ontology Development 101

**Autores:** Natalya F. Noy y Deborah L. McGuinness  
**Institución:** Stanford University  
**Acceso:** Abierto

Este documento es especialmente útil para comprender cómo se construye una ontología a partir de un dominio.

### Temas recomendados

- ¿Por qué desarrollar una ontología?
- Identificación del dominio
- Definición de clases
- Construcción de jerarquías
- Propiedades de las clases
- Restricciones
- Creación de instancias

### Preguntas de lectura

a) ¿Cuál es la diferencia entre una clase y una instancia?

b) ¿Por qué una jerarquía de clases no debe construirse únicamente a partir de nombres semejantes?

c) ¿Qué papel cumplen las propiedades en una ontología?

d) ¿Por qué no existe necesariamente una única forma correcta de modelar un dominio?

[Consultar Ontology Development 101](https://protege.stanford.edu/publications/ontology_development/ontology101.pdf)

---

## 3. OWL 2 Web Ontology Language Primer

**Organización:** World Wide Web Consortium (W3C)  
**Documento:** *OWL 2 Web Ontology Language Primer (Second Edition)*  
**Acceso:** Abierto  
**Estado:** W3C Recommendation

OWL 2 es un lenguaje para representar conocimiento complejo acerca de entidades, grupos de entidades y relaciones entre ellas.

El *Primer* constituye la referencia principal del subtema para estudiar OWL 2.

### Temas recomendados

- Clases
- Individuos
- Propiedades
- Jerarquías
- Axiomas
- Restricciones
- Relaciones entre clases
- Conocimiento explícito e implícito

No es necesario estudiar toda la especificación técnica. Para este subtema interesa principalmente comprender **qué puede representarse con OWL 2 y cómo se relaciona con una ontología conceptual**.

### Preguntas de lectura

a) ¿Qué elementos básicos puede representar una ontología OWL 2?

b) ¿Qué diferencia existe entre una clase, un individuo y una propiedad?

c) ¿Por qué OWL permite obtener conocimiento que no fue declarado explícitamente?

d) ¿Qué relación existe entre OWL y RDF?

[Consultar OWL 2 Primer](https://www.w3.org/TR/owl2-primer/)

[Consultar versión PDF](https://www.w3.org/2012/pdf/REC-owl2-primer-20121211.pdf)

---

## 4. Protégé

**Institución:** Stanford University  
**Tipo:** Editor de ontologías  
**Acceso:** Gratuito y de código abierto

Protégé es un entorno para desarrollar y explorar ontologías OWL.

Será utilizado posteriormente en la práctica del subtema para crear una ontología pequeña y observar cómo se representan de manera computable las ideas estudiadas en el apunte.

### En Protégé se trabajará con

- Clases
- Subclases
- Individuos
- Propiedades de objetos
- Propiedades de datos
- Jerarquías
- Axiomas básicos
- Visualización de la ontología
- Razonamiento básico

Protégé está disponible como aplicación de escritorio y como editor Web. Ambas opciones soportan OWL 2.

[Protégé](https://protege.stanford.edu/software/)

[Documentación de Protégé Desktop](https://protegeproject.github.io/protege/)

[Guía de inicio](https://protegeproject.github.io/protege/getting-started/)

---

# Ruta de estudio recomendada

Para evitar estudiar los recursos de manera aislada, se recomienda seguir esta secuencia:

**1. Apunte del tema 3.2**  
Comprender la relación entre redes semánticas, marcos, ontologías y OWL.

↓

**2. Capítulos del PDF del curso**  
Profundizar en redes semánticas, marcos y fundamentos de ontologías.

↓

**3. Ontology Development 101**  
Comprender cómo se modela un dominio mediante clases, propiedades e instancias.

↓

**4. OWL 2 Primer**  
Identificar cómo una ontología puede representarse mediante un lenguaje formal y computable.

↓

**5. Protégé**  
Construir una pequeña ontología y aplicar los conceptos estudiados.

---

# Guía de estudio

Al terminar la revisión de los recursos, el estudiante debería poder responder:

a) ¿Qué diferencia existe entre representar conocimiento mediante lógica y mediante una red semántica?

b) ¿Qué representan los nodos y los arcos de una red semántica?

c) ¿Qué diferencia existe entre `subclase-de`, `instancia-de` y `parte-de`?

d) ¿Qué es un marco y qué información puede almacenar?

e) ¿Qué diferencia existe entre un marco clase y un marco instancia?

f) ¿Qué es una ontología en Inteligencia Artificial?

g) ¿Cuáles son los componentes principales de una ontología?

h) ¿Qué diferencia existe entre una taxonomía y una ontología?

i) ¿Qué función cumple OWL?

j) ¿Qué papel tiene Protégé en el desarrollo de ontologías?

---

# Para profundizar

Si se desea ampliar el tema, pueden consultarse también los documentos de referencia de OWL 2 publicados por el W3C:

- **OWL 2 Document Overview**
- **OWL 2 Quick Reference Guide**
- **OWL 2 New Features and Rationale**

[Documentación de OWL 2](https://www.w3.org/TR/owl-overview/)

---

## Referencias

Noy, N. F., & McGuinness, D. L. (2001). *Ontology Development 101: A Guide to Creating Your First Ontology*. Stanford University.

World Wide Web Consortium. (2012). *OWL 2 Web Ontology Language Primer (Second Edition)*. W3C Recommendation.

Stanford Center for Biomedical Informatics Research. *Protégé*. Stanford University.

---

[← Volver al subtema 3.2](../README.md)
