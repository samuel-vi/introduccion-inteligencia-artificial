
# Práctica 3.2 — Construcción de una ontología en Protégé con OWL 2

## Unidad 3. Representación del conocimiento y razonamiento

### Subtema 3.2 Redes semánticas, marcos y ontologías (OWL)

---

## Propósito

Construir una ontología pequeña en **Protégé** para representar un dominio de red informática mediante **clases, subclases, individuos, propiedades de objeto y propiedades de datos**, y utilizar un razonador para observar cómo puede obtenerse conocimiento implícito a partir de los axiomas definidos.

Al finalizar la práctica, el estudiante deberá distinguir claramente entre:

a) Una **clase**, que representa una categoría

b) Un **individuo**, que representa una entidad concreta

c) Una **propiedad de objeto**, que relaciona individuos

d) Una **propiedad de datos**, que relaciona un individuo con un valor

e) Un **axioma**, que establece conocimiento formal sobre el dominio

f) Una **inferencia**, que permite obtener conocimiento que no fue declarado explícitamente

---

# 1. Situación a representar

Se desea modelar una pequeña red informática formada por computadoras, routers y servidores.

El conocimiento inicial del dominio es el siguiente:

a) Toda computadora es un dispositivo

b) Todo router es un dispositivo

c) Todo servidor es un dispositivo

d) PC1 es una computadora

e) Router1 es un router

f) Servidor1 es un servidor

g) PC1 está conectado a Router1

h) Servidor1 está conectado a Router1

i) PC1 tiene la dirección IP `192.168.1.10`

j) Router1 tiene la dirección IP `192.168.1.1`

k) Servidor1 tiene la dirección IP `192.168.1.20`

Además, queremos que el sistema pueda reconocer automáticamente qué dispositivos se encuentran conectados a otro dispositivo.

---

# 2. Modelo conceptual esperado

Antes de abrir Protégé, observe la estructura que se desea construir.

```text
                    Dispositivo
                   /     |      \
                  /      |       \
        Computadora    Router    Servidor
             |            |          |
            PC1        Router1    Servidor1
              \           ↑          /
               \          |         /
                └── conectadoA ────┘
```

También se definirán las direcciones IP de cada individuo.

---

# 3. Crear la ontología

Abra **Protégé Desktop** y cree una nueva ontología.

Puede utilizar como IRI base, por ejemplo:

```text
http://example.org/red-informatica
```

Guarde el proyecto con un nombre como:

```text
red-informatica.owl
```

> La IRI funciona como identificador de la ontología. Para esta práctica se utiliza una dirección de ejemplo y no es necesario que exista como sitio Web.

---

# 4. Crear las clases

En la pestaña **Classes**, cree la siguiente jerarquía:

```text
owl:Thing
└── Dispositivo
    ├── Computadora
    ├── Router
    └── Servidor
```

## Interpretación

`Dispositivo` es la clase más general de nuestro pequeño dominio.

Las clases:

```text
Computadora
Router
Servidor
```

son especializaciones de `Dispositivo`.

En términos conceptuales:

```text
Computadora subClassOf Dispositivo
Router      subClassOf Dispositivo
Servidor    subClassOf Dispositivo
```

Esto significa que cualquier individuo que pertenezca a `Computadora`, `Router` o `Servidor` también puede ser reconocido como un `Dispositivo`.

---

# 5. Crear una propiedad de objeto

En la pestaña **Object properties**, cree:

```text
conectadoA
```

Una propiedad de objeto permite establecer una relación entre dos individuos.

En esta práctica:

```text
PC1 conectadoA Router1
```

significa que el individuo `PC1` se encuentra conectado al individuo `Router1`.

Configure:

| Elemento | Valor |
|---|---|
| Propiedad | `conectadoA` |
| Dominio | `Dispositivo` |
| Rango | `Dispositivo` |

## ¿Qué significa dominio y rango?

El **dominio** indica qué tipo de entidad puede aparecer como origen de la relación.

El **rango** indica qué tipo de entidad puede aparecer como destino.

Por tanto:

```text
Dispositivo conectadoA Dispositivo
```

expresa que la relación conecta dispositivos entre sí.

> En OWL, dominio y rango tienen significado lógico. No deben interpretarse solamente como restricciones de formulario.

---

# 6. Crear una propiedad de datos

En la pestaña **Data properties**, cree:

```text
tieneDireccionIP
```

Configure:

| Elemento | Valor |
|---|---|
| Propiedad | `tieneDireccionIP` |
| Dominio | `Dispositivo` |
| Tipo de dato | `xsd:string` |

Una propiedad de datos relaciona un individuo con un valor literal.

Ejemplo:

```text
PC1 tieneDireccionIP "192.168.1.10"
```

Aquí `PC1` es un individuo y `"192.168.1.10"` es un valor de texto.

---

# 7. Crear los individuos

En la pestaña **Individuals by class**, cree los siguientes individuos.

## PC1

Clase:

```text
Computadora
```

Propiedades:

```text
conectadoA Router1
tieneDireccionIP "192.168.1.10"
```

## Router1

Clase:

```text
Router
```

Propiedad:

```text
tieneDireccionIP "192.168.1.1"
```

## Servidor1

Clase:

```text
Servidor
```

Propiedades:

```text
conectadoA Router1
tieneDireccionIP "192.168.1.20"
```

---

# 8. Verificar el conocimiento explícito

Hasta este punto hemos declarado explícitamente que:

```text
PC1 es Computadora
Router1 es Router
Servidor1 es Servidor
```

y que:

```text
PC1 conectadoA Router1
Servidor1 conectadoA Router1
```

Observe que no fue necesario declarar:

```text
PC1 es Dispositivo
Router1 es Dispositivo
Servidor1 es Dispositivo
```

Estas afirmaciones pueden obtenerse a partir de la jerarquía de clases.

---

# 9. Crear una clase definida

Ahora agregaremos una clase que permita observar una inferencia más interesante.

Cree la clase:

```text
DispositivoConectado
```

En lugar de definirla solamente como subclase, establezca una condición equivalente:

```text
Dispositivo
and
conectadoA some Dispositivo
```

La interpretación en lenguaje natural es:

> Un DispositivoConectado es un dispositivo que está conectado a por lo menos un dispositivo.

Conceptualmente:

```text
DispositivoConectado
≡
Dispositivo AND conectadoA SOME Dispositivo
```

No es necesario memorizar todavía la sintaxis formal. Lo importante es comprender la condición.

---

# 10. Ejecutar el razonador

Seleccione un razonador disponible en Protégé, por ejemplo **HermiT**, y ejecute la clasificación de la ontología.

Después revise nuevamente los individuos.

El sistema debería poder inferir que:

```text
PC1 pertenece a Dispositivo
Servidor1 pertenece a Dispositivo
Router1 pertenece a Dispositivo
```

Además, debido a la definición de `DispositivoConectado`, debería reconocer como miembros de esa clase a:

```text
PC1
Servidor1
```

porque ambos poseen una relación:

```text
conectadoA Router1
```

---

# 11. Conocimiento explícito e implícito

Esta práctica permite distinguir dos tipos de conocimiento.

## Conocimiento explícito

Es el conocimiento introducido directamente.

Por ejemplo:

```text
PC1 es Computadora
PC1 conectadoA Router1
```

## Conocimiento implícito

Es conocimiento que puede obtenerse mediante razonamiento.

Por ejemplo:

```text
PC1 es Dispositivo
PC1 es DispositivoConectado
```

Estas afirmaciones no tuvieron que declararse individualmente.

Se derivan de:

```text
Computadora subClassOf Dispositivo
```

y:

```text
DispositivoConectado
≡
Dispositivo AND conectadoA SOME Dispositivo
```

Esta diferencia entre conocimiento explícito e implícito será fundamental en el estudio posterior de los sistemas de inferencia.

---

# 12. Visualizar la ontología

Si su instalación de Protégé dispone de una vista gráfica, utilícela para observar la jerarquía y las relaciones.

La estructura conceptual debe aproximarse a:

```text
Dispositivo
├── Computadora
│   └── PC1
├── Router
│   └── Router1
└── Servidor
    └── Servidor1
```

y las relaciones:

```text
PC1 ─────────► Router1
     conectadoA

Servidor1 ───► Router1
     conectadoA
```

La visualización ayuda a relacionar las ontologías con las **redes semánticas** estudiadas al inicio del subtema.

---

# 13. Relación con redes semánticas y marcos

## Como red semántica

Parte del conocimiento puede visualizarse como:

```text
PC1 ──instancia-de──► Computadora
Computadora ──subclase-de──► Dispositivo
PC1 ──conectado-a──► Router1
```

El énfasis está en las relaciones.

## Como marco

También podemos describir:

```text
MARCO INSTANCIA: PC1

Clase: Computadora
direccion-IP: 192.168.1.10
conectado-a: Router1
```

El énfasis está en las propiedades del objeto.

## Como ontología OWL

En OWL se integran:

```text
Clases
Jerarquías
Individuos
Propiedades
Axiomas
Restricciones
```

en una representación formal que puede ser procesada por un razonador.

---

# 14. Ejercicio de ampliación

Amplíe la ontología incorporando un nuevo dispositivo.

Cree:

```text
PC2
```

como individuo de:

```text
Computadora
```

Asigne:

```text
tieneDireccionIP "192.168.1.11"
```

y establezca:

```text
PC2 conectadoA Router1
```

Ejecute nuevamente el razonador.

Responda:

a) ¿PC2 es reconocido como `Dispositivo`?

b) ¿PC2 es reconocido como `DispositivoConectado`?

c) ¿Fue necesario declarar explícitamente ambas clases?

d) ¿Qué axiomas permitieron obtener esas conclusiones?

---

# 15. Reto opcional: detectar una inconsistencia

Este ejercicio debe realizarse solamente después de guardar una copia de la ontología correcta.

Declare las clases:

```text
Computadora
Router
Servidor
```

como clases mutuamente disjuntas.

Esto significa que un mismo individuo no debería pertenecer simultáneamente a dos de esas categorías.

Posteriormente, asigne temporalmente:

```text
PC1
```

también a la clase:

```text
Router
```

Ejecute el razonador y observe el resultado.

## Reflexione

a) ¿Por qué aparece una inconsistencia?

b) ¿Qué conocimiento declarado provoca el conflicto?

c) ¿Por qué la detección automática de inconsistencias puede ser útil en sistemas reales?

Al terminar, elimine la asignación incorrecta y vuelva a ejecutar el razonador.

---

# 16. Evidencias de la práctica

Entregue las siguientes evidencias:

a) Archivo de la ontología:

```text
red-informatica.owl
```

b) Captura de la jerarquía de clases

c) Captura de la propiedad `conectadoA`

d) Captura de los individuos `PC1`, `Router1` y `Servidor1`

e) Captura donde se observe la inferencia de `DispositivoConectado`

f) Una explicación breve, de aproximadamente media cuartilla, donde responda:

> ¿Qué diferencia existe entre declarar conocimiento explícitamente y obtenerlo mediante inferencia en una ontología?

---

# 17. Producto esperado

Al terminar la práctica, la ontología debe contener al menos:

| Tipo | Elementos |
|---|---|
| Clases principales | Dispositivo, Computadora, Router, Servidor |
| Clase definida | DispositivoConectado |
| Propiedad de objeto | conectadoA |
| Propiedad de datos | tieneDireccionIP |
| Individuos | PC1, Router1, Servidor1 |
| Axioma jerárquico | Computadora, Router y Servidor son subclases de Dispositivo |
| Axioma de equivalencia | DispositivoConectado ≡ Dispositivo y conectadoA algún Dispositivo |

---

# 18. Criterios de evaluación

| Criterio | Porcentaje |
|---|---:|
| Jerarquía de clases correctamente construida | 20 % |
| Individuos correctamente definidos | 15 % |
| Propiedad de objeto correctamente configurada | 15 % |
| Propiedad de datos correctamente configurada | 10 % |
| Definición de `DispositivoConectado` | 15 % |
| Uso del razonador y evidencia de inferencias | 15 % |
| Explicación y reflexión final | 10 % |
| **Total** | **100 %** |

---

# 19. Preguntas de cierre

Antes de concluir la práctica, responda:

a) ¿Qué diferencia existe entre una clase y un individuo?

b) ¿Qué diferencia existe entre una propiedad de objeto y una propiedad de datos?

c) ¿Qué información aporta una relación `subClassOf`?

d) ¿Qué significa que una clase esté definida mediante condiciones necesarias y suficientes?

e) ¿Qué conocimiento fue inferido por el razonador?

f) ¿Qué ventaja ofrece una ontología frente a almacenar solamente una lista de datos?

g) ¿Cómo se relaciona esta práctica con las redes semánticas y los marcos?

---

# 20. Conexión con el subtema 3.3

En esta práctica se utilizó un razonador para obtener conocimiento implícito.

Sin embargo, todavía no se ha estudiado con detalle **cómo funcionan los mecanismos de inferencia**.

En el siguiente subtema se analizarán:

## 3.3 Sistemas de inferencia: hacia adelante y hacia atrás

La pregunta cambiará de:

> **¿Cómo representamos el conocimiento?**

a:

> **¿Cómo utiliza un sistema ese conocimiento para obtener nuevas conclusiones?**

---

## Recursos de apoyo

a) [Protégé](https://protege.stanford.edu/software/)

b) [Documentación de Protégé Desktop](https://protegeproject.github.io/protege/)

c) [OWL 2 Primer — W3C](https://www.w3.org/TR/owl2-primer/)

d) [Ontology Development 101 — Stanford](https://protege.stanford.edu/publications/ontology_development/ontology101.pdf)

---

[← Volver al subtema 3.2](../README.md)
