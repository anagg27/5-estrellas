# Unidad 4 — Diseño del Software

## Ejercitario

| Campo | Detalle |
|---|---|
| **Materia** | Ingeniería de Software 1 |
| **Unidad** | 4 — Diseño del software |
| **Temas cubiertos** | Actividad del diseño y sus objetivos · Técnicas de modularización · Notaciones de diseño · Paradigma orientado a objetos · Diseño de la interfaz de usuario |
| **Cantidad de preguntas** | 17 |

---

## Tema 1 — Actividad del diseño del software y sus objetivos

**1.** Explique con sus propias palabras la diferencia entre diseño arquitectónico y diseño detallado. Dé un ejemplo de cada uno para un sistema de reservas de vuelos.

**2.** *(Verdadero o Falso — justifique su respuesta)*
"El diseño de software tiene una única solución óptima para cada especificación."

---

## Tema 2 — Técnicas de modularización

**3.** Defina el criterio de ocultamiento de información de Parnas y explique por qué reduce el impacto de los cambios futuros sobre el sistema.

**4.** Compare la descomposición top-down y bottom-up: mencione una ventaja y una desventaja de cada enfoque.

**5.** *(Aplicación)* Dado un sistema de gestión de biblioteca, proponga una modularización por tipos de datos abstractos, indicando al menos dos módulos junto con su interfaz pública (operaciones que exponen).

---

## Tema 3 — Notaciones de diseño

**6.** ¿Qué información transmite un diagrama de estructura (structure chart) que no transmite un diagrama de clases UML, y viceversa?

**7.** Escriba en PDL (pseudocódigo) el algoritmo para calcular el promedio de una lista de calificaciones, excluyendo los valores nulos.

**8.** Complete el siguiente enunciado:

> El diagrama UML de **____________** documenta la interacción dinámica entre objetos concretos a lo largo del tiempo, mientras que el diagrama de **____________** documenta la estructura estática de clases, atributos y relaciones.

---

## Tema 4 — El paradigma orientado a objetos (Análisis y Diseño OO)

**9.** Defina encapsulamiento, herencia y polimorfismo, aportando un ejemplo propio para cada concepto (no utilice los ejemplos vistos en clase).

**10.** Explique la diferencia entre Análisis Orientado a Objetos (AOO) y Diseño Orientado a Objetos (DOO). ¿En qué etapa aparecen típicamente las clases de solución, como las de acceso a base de datos?

**11.** *(Aplicación — tarjeta CRC)* Elabore una tarjeta CRC para la clase `Factura` en un sistema de facturación electrónica, indicando al menos tres responsabilidades y dos colaboradores.

**12.** A partir de la siguiente especificación textual:

> "El sistema debe permitir que un Cliente realice un Pedido compuesto por uno o más Ítems, y que un Vendedor apruebe dicho Pedido."

Identifique las clases candidatas aplicando la técnica de análisis de sustantivos/verbos, indicando qué sustantivos sugieren clases y qué verbos sugieren operaciones.

**13.** Explique el principio de sustitución de Liskov y proponga un contraejemplo: un caso de diseño en el que este principio se viole.

**14.** *(Verdadero o Falso — justifique su respuesta)*
"El polimorfismo permite que distintas subclases implementen de forma diferente un mismo método heredado de la superclase."

---

## Tema 5 — Diseño de la interfaz del usuario

**15.** Mencione tres heurísticas de usabilidad de Nielsen y explique cómo aplicaría cada una al diseño de un formulario de registro de usuarios.

**16.** Explique por qué la separación entre interfaz y lógica de negocio (por ejemplo, mediante el patrón MVC) facilita el mantenimiento del software a largo plazo.

**17.** Ordene y describa brevemente las tres etapas típicas de prototipado de interfaces, de menor a mayor fidelidad.

---

## Cuadro de clasificación

Clasifique cada elemento según el paradigma de diseño al que pertenece principalmente, marcando con una X la columna correspondiente.

| Elemento | Estructurado | Orientado a objetos | Ambos |
|---|---|---|---|
| Diagrama de estructura (structure chart) | | | |
| Diagrama de clases UML | | | |
| Tarjeta CRC | | | |
| PDL / pseudocódigo | | | |
| Diagrama de secuencia | | | |
| DFD (Diagrama de Flujo de Datos) | | | |

---

## Cuadro de relación

Relacione cada concepto de la columna A con su definición correspondiente de la columna B, escribiendo en la tercera columna la letra que corresponda.

| Columna A | Columna B | Respuesta |
|---|---|---|
| 1. Encapsulamiento | a. Los elementos de un módulo están fuertemente relacionados y contribuyen a una única tarea | |
| 2. Herencia | b. Grado de independencia entre los módulos de un sistema | |
| 3. Polimorfismo | c. Los datos y las operaciones que los manipulan se agrupan en una unidad, protegiendo el estado interno | |
| 4. Cohesión | d. Una clase especializa a otra, reutilizando y extendiendo su estructura y comportamiento | |
| 5. Acoplamiento | e. Objetos de distintas clases responden de forma distinta a un mismo mensaje | |
