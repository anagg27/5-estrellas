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

Arquitectónico = Son las  partes que hay y cómo se conectan. Ves el sistema desde arriba detallado como funciona cada parte por dentro. Ves el código, clases y tablas.Ejemplo Reservas de Vuelos Arquitectónico: El sistema tiene 3 servicios, App Web, Servicio de Vuelos y Servicio de Pagos, que se hablan por API. Usa una base de datos PostgreSQL. 
Detallado: En el Servicio de Pagos, la clase Reserva { id, vueloId, estado } tiene el método pagar() que valida la tarjeta, si falla cambia estado a CANCELADA y libera el asiento.


**2.** *(Verdadero o Falso — justifique su respuesta)*
"El diseño de software tiene una única solución óptima para cada especificación."

falso. No existe una única solución óptima. Frente a una misma especificación, distintos diseñadores producen distintas soluciones válidas; el diseño se evalúa por calidad relativa, no por unicidad. que seria diseño arquitectónico, diseño detallado y proceso iterativo.

## Tema 2 — Técnicas de modularización

**3.** Defina el criterio de ocultamiento de información de Parnas y explique por qué reduce el impacto de los cambios futuros sobre el sistema.

 Parnas (1972): cada módulo debe ocultar una decisión de diseño que probablemente cambiará, exponiendo solo la interfaz mínima necesaria.
reduce el impacto de los cambios porque si el cambio está escondido adentro de un solo módulo, el resto del sistema no se entera y no se rompe.Si no ocultas, todos dependen de los detalles. Cambias algo y se cae todo el sistema en cadena.

**4.** Compare la descomposición top-down y bottom-up: mencione una ventaja y una desventaja de cada enfoque.

Top-Down: Empiezas desde el sistema grande y lo vas partiendo en módulos más chicos. 
Ventaja: Ves todo el panorama desde el inicio, no te olvidas de partes importantes.
Desventaja: Puedes diseñar módulos que después son muy difíciles de implementar abajo.

Bottom-Up: Empiezas desde piezas pequeñas y útiles que ya tienes y las vas combinando para armar el sistema grande.
Ventaja: Reutilizas mucho, son piezas ya probadas y estables.
Desventaja: Puedes terminar con un sistema que funciona pero no cumple bien lo que el usuario realmente quería.

**5.** *(Aplicación)* Dado un sistema de gestión de biblioteca, proponga una modularización por tipos de datos abstractos, indicando al menos dos módulos junto con su interfaz pública (operaciones que exponen).

Para biblioteca Tipo de Dato Abstracto.
Módulo 1: Libro 
crear(titulo, autor, isbn)
buscar(id)
prestar(id)
devolver(id)
Módulo 2:Socio
registrar(nombre, ci)
buscar(id)
prestarLibro(socioId, libroId)
tieneDeuda(id)bool
Cada uno esconde sus datos internos. Solo se usa por su interfaz.

## Tema 3 — Notaciones de diseño

**6.** ¿Qué información transmite un diagrama de estructura (structure chart) que no transmite un diagrama de clases UML, y viceversa?
Diagrama de estructura (structure chart): Transmite la notación del diseño estructurado clásico: representa la jerarquía de módulos y el flujo de control (invocaciones) mediante cajas y líneas, con flechas etiquetadas para indicar el flujo de datos y control. Su limitación es que no describe bien el paradigma orientado a objetos.  
Diagrama de clases UML: Transmite la estructura estática del paradigma orientado a objetos, mostrando las clases, sus atributos, métodos y relaciones (como asociación, herencia y composición). 
![Uploading image.png…]()

**7.** Escriba en PDL (pseudocódigo) el algoritmo para calcular el promedio de una lista de calificaciones, excluyendo los valores nulos.
PROCEDIMIENTO calcularPromedio(calificaciones)
    suma = 0
    cantidad = 0
    PARA CADA calificacion EN calificaciones HACER
        SI calificacion ES DIFERENTE DE NULO ENTONCES
            suma = suma + calificacion
            cantidad = cantidad + 1
        FIN SI
    FIN PARA
    SI cantidad > 0 ENTONCES
        RETORNAR suma / cantidad
    SINO
        RETORNAR error("lista sin calificaciones válidas")
    FIN SI
FIN PROCEDIMIENTO
**8.** Complete el siguiente enunciado:

> El diagrama UML de **__secuencia__** documenta la interacción dinámica entre objetos concretos a lo largo del tiempo, mientras que el diagrama de **___clases__** documenta la estructura estática de clases, atributos y relaciones.

---

## Tema 4 — El paradigma orientado a objetos (Análisis y Diseño OO)

**9.** Defina encapsulamiento, herencia y polimorfismo, aportando un ejemplo propio para cada concepto (no utilice los ejemplos vistos en clase).
Encapsulamiento: Los datos y las operaciones que los manipulan se agrupan en una unidad; el estado interno se protege del acceso directo .
Ejemplo: Una clase Termostato que encapsula el atributo privado temperaturaActual y expone operaciones públicas como ajustarTemperatura().
Herencia: Una clase puede especializar a otra, reutilizando y extendiendo su estructura y comportamiento.
Ejemplo: Una superclase DispositivoElectronico de la cual hereda una subclase Smartphone, extendiendo su estructura con atributos específicos como sistemaOperativo.
Polimorfismo: Objetos de distintas clases responden de forma distinta a un mismo mensaje u operación.
Ejemplo: Una operación conectar() compartida por clases como Impresora y Auricular, donde cada una ejecuta su propia lógica de conexión de manera diferente.

**10.** Explique la diferencia entre Análisis Orientado a Objetos (AOO) y Diseño Orientado a Objetos (DOO). ¿En qué etapa aparecen típicamente las clases de solución, como las de acceso a base de datos?
Análisis Orientado a Objetos (AOO): Se enfoca en identificar qué objetos existen en el dominio del problema (clases de negocio y sus relaciones). Es independiente de la tecnología y su resultado es un modelo conceptual del dominio.
Diseño Orientado a Objetos (DOO): Se enfoca en cómo se estructuran esos objetos en la solución, considerando la plataforma y agregando clases de solución. Su resultado es un modelo de diseño listo para implementar.
Las clases de solución (como las de acceso a base de datos) aparecen típicamente en la etapa de Diseño Orientado a Objetos (DOO)

**11.** *(Aplicación — tarjeta CRC)* Elabore una tarjeta CRC para la clase `Factura` en un sistema de facturación electrónica, indicando al menos tres responsabilidades y dos colaboradores.
Clase: Factura
Responsabilidades:
Calcular el total de la factura 
Agregar o quitar ítems facturados
Validar los datos fiscales del cliente 
Colaboradores:
Cliente 
Ítem de factura 
**12.** A partir de la siguiente especificación textual:

> "El sistema debe permitir que un Cliente realice un Pedido compuesto por uno o más Ítems, y que un Vendedor apruebe dicho Pedido."

Identifique las clases candidatas aplicando la técnica de análisis de sustantivos/verbos, indicando qué sustantivos sugieren clases y qué verbos sugieren operaciones.
Sustantivos (sugieren clases): Cliente, Pedido, Ítem, Vendedor
Verbos (sugieren operaciones): realice (gestionar/crear pedido), apruebe (aprobar pedido)
**13.** Explique el principio de sustitución de Liskov y proponga un contraejemplo: un caso de diseño en el que este principio se viole.
Principio de sustitución de Liskov: Una subclase debe poder usarse siempre donde se espera la superclase sin alterar el correcto funcionamiento del sistema.   Contraejemplo (violación): Tener una superclase Rectangulo con métodos setAncho() y setAlto(), y una subclase Cuadrado. Si el Cuadrado sobrescribe los métodos para forzar que ancho y alto sean siempre iguales, al sustituir un Rectangulo por un Cuadrado en un fragmento de código que espera modificar ancho y alto de forma independiente, el comportamiento fallará, violando el principio de sustitución.  
**14.** *(Verdadero o Falso — justifique su respuesta)*
"El polimorfismo permite que distintas subclases implementen de forma diferente un mismo método heredado de la superclase."
Verdadero
Justificación: El material define el polimorfismo indicando que objetos de distintas clases responden de forma distinta a un mismo mensaje u operación. Esto se visualiza de forma directa en el diagrama de clases del PPT, donde las subclases Vendedor y Gerente heredan de Empleado y redefinen el método calcularSueldo() con comportamientos distintos

## Tema 5 — Diseño de la interfaz del usuario

**15.** Mencione tres heurísticas de usabilidad de Nielsen y explique cómo aplicaría cada una al diseño de un formulario de registro de usuarios.

Visibilidad del estado: el sistema debe informar siempre qué está pasando. En el registro, mostraría una barra de progreso si el formulario tiene varios pasos. También mostraría un indicador de carga al enviar los datos y un mensaje claro de que la cuenta se creó.

Prevención de errores: el diseño evita que el error ocurra. Usaría el tipo de campo correcto, validaría en el momento y mostraría el formato esperado como ayuda. Deshabilitaría el botón “Registrarse” hasta que los campos obligatorios estén completos y pediría confirmar la contraseña.

Consistencia: los mismos elementos se comportan igual en toda la interfaz. Todos los campos tendrían el mismo estilo, las etiquetas la misma posición y los botones primarios el mismo color y texto que en el resto del sistema. Los mensajes de error aparecerían siempre en el mismo lugar y con el mismo formato.

**16.** Explique por qué la separación entre interfaz y lógica de negocio (por ejemplo, mediante el patrón MVC) facilita el mantenimiento del software a largo plazo.

La interfaz no debe contener lógica de negocio, para poder cambiar una sin afectar la otra. Con MVC, el Modelo guarda los datos y la lógica del dominio, la Vista se ocupa de la presentación y el Controlador coordina la entrada del usuario y actualiza modelo y vista. Esto facilita el mantenimiento a largo plazo porque:

Los cambios quedan localizados, hay bajo acoplamiento y alta cohesión, se puede reutilizar, se puede trabajar en paralelo y es más adaptable.

**17.** Ordene y describa brevemente las tres etapas típicas de prototipado de interfaces, de menor a mayor fidelidad.

Wireframe: boceto de baja fidelidad que define la distribución de los elementos en pantalla, sin estilo visual.

Mockup: representación visual estática, con estilo (colores, tipografías) y contenido aproximado.

Prototipo interactivo: simulación navegable de los flujos reales, sin la lógica de negocio completa.

---

## Cuadro de clasificación

Clasifique cada elemento según el paradigma de diseño al que pertenece principalmente, marcando con una X la columna correspondiente.

| Elemento | Estructurado | Orientado a objetos | Ambos |
|---|---|---|---|
| Diagrama de estructura (structure chart) | X | | |
| Diagrama de clases UML | | X | |
| Tarjeta CRC | | X | |
| PDL / pseudocódigo | | | X |
| Diagrama de secuencia | | X | |
| DFD (Diagrama de Flujo de Datos) | X | | |

---

## Cuadro de relación

Relacione cada concepto de la columna A con su definición correspondiente de la columna B, escribiendo en la tercera columna la letra que corresponda.

| Columna A | Columna B | Respuesta |
|---|---|---|
| 1. Encapsulamiento | a. Los elementos de un módulo están fuertemente relacionados y contribuyen a una única tarea | c |
| 2. Herencia | b. Grado de independencia entre los módulos de un sistema | d |
| 3. Polimorfismo | c. Los datos y las operaciones que los manipulan se agrupan en una unidad, protegiendo el estado interno | e |
| 4. Cohesión | d. Una clase especializa a otra, reutilizando y extendiendo su estructura y comportamiento | a |
| 5. Acoplamiento | e. Objetos de distintas clases responden de forma distinta a un mismo mensaje | b |
