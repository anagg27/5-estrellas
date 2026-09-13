# Respuestas — Ejercitario Unidad 03

---

## Tema 1 · Rigor y formalidad

**1. Explica con tus propias palabras la diferencia entre "rigor" y "formalidad" en el desarrollo de software. Da un ejemplo de cada uno.**

_Respuesta:_ El rigor es una actitud cuidadosa, disciplinada y sistemática al trabajar en cada tarea del desarrollo, mientras que la formalidad va un paso más allá e involucra el uso de notaciones precisas con fundamento matemático para eliminar ambigüedades.  
Ejemplo de rigor: Definir una lista detallada de pasos de revisión de código (code review) y seguirla estrictamente antes de fusionar cualquier cambio al proyecto.
Ejemplo de formalidad: Especificar las precondiciones y poscondiciones de una interfaz utilizando lógica matemática o lenguajes de especificación formal.


**2. ¿Por qué no conviene formalizar por completo todos los aspectos de un proyecto de software? Menciona un caso donde sí valga la pena hacerlo.**

_Respuesta:_ No conviene formalizar todo por completo porque la formalización requiere un alto costo en tiempo, esfuerzo y especialización, lo cual resulta innecesario e ineficiente para partes secundarias o simples del sistema. Debe aplicarse principalmente donde el costo o riesgo de un error sea muy alto.  
Caso donde sí vale la pena: En módulos críticos de seguridad o salud, como el software de un marcapasos, un sistema de control de tráfico aéreo o la integración del módulo de pagos y transferencias en un sistema bancario.


---

## Tema 2 · Separación de intereses

**3. En tus propias palabras, ¿qué significa "separar intereses" en el diseño de un sistema? Da un ejemplo distinto al visto en clase.**

_Respuesta:_ Significa dividir un problema complejo abordando por separado sus distintos aspectos o preocupaciones independientes, reduciendo la carga cognitiva para trabajar en una parte a la vez.  
Ejemplo: En un sistema de gestión escolar, separar el módulo encargado de la notificación y generación de mensajes del módulo que administra las calificaciones académicas. Si cambia el proveedor de correos, la lógica de cálculo de notas no se ve afectada.


**4. Para una aplicación de reservas de vuelos, identifica al menos tres "intereses" o aspectos distintos que deberían mantenerse separados, y explica brevemente por qué.**

_Respuesta:_ 
Interfaz de usuario (UI): La pantalla donde el pasajero selecciona fechas y asientos. Debe estar separada para poder rediseñar la experiencia visual sin modificar las reglas de reserva.  
Lógica de negocio de reservas: Reglas sobre disponibilidad de asientos, cálculo de tarifas, políticas de equipaje y promociones. Debe ser independiente de la vista y de la base de datos.  
Integración con pasarela de pagos: El proceso de cobro mediante tarjeta o medios externos. Se aísla para que cambios en los proveedores de pago no afecten el catálogo ni el flujo de búsqueda de vuelos.


---

## Tema 3 · Modularidad

**5. Explica con tus propias palabras la relación entre modularidad, acoplamiento y cohesión.**

_Respuesta:_ La modularidad es la subdivisión del software en partes o módulos con funciones claras. Una buena modularización busca alcanzar bajo acoplamiento (que los módulos dependan lo menos posible unos de otros) y alta cohesión (que los elementos dentro de un mismo módulo pertenezcan a un propósito único y bien definido).


**6. Completa el siguiente cuadro indicando si cada situación es un ejemplo de "alto acoplamiento" o de "baja cohesión", y justifica tu respuesta.**

| Situación | ¿Acoplamiento o cohesión? | Justificación |
| --- | --- | --- |
| Un módulo de "utilidades" que mezcla validaciones, envío de emails y cálculos financieros | Baja cohesión | Agrupa responsabilidades y tareas de distintos dominios que no están fuertemente relacionadas entre sí dentro del mismo módulo. |
| Dos módulos que se llaman constantemente entre sí y comparten variables globales | Alto acoplamiento | Existe una fuerte interdependencia entre ambos módulos, provocando que los cambios de uno afecten al otro. |
| Un módulo de "reportes" que además valida los permisos del usuario | Baja cohesión | Mezcla dos intereses o funciones distintas (generar informes vs. seguridad/autorización) dentro de un solo módulo. |
| Un módulo de autenticación que solo se encarga de validar credenciales | Alta cohesión / Bajo acoplamiento | Es una situación ideal: tiene alta cohesión al cumplir un propósito único bien definido, y bajo acoplamiento con el resto del sistema. |

**7. ¿Por qué una interfaz bien definida entre módulos reduce el impacto de los cambios internos de cada uno?**

_Respuesta:_ Porque la interfaz actúa como un contrato que oculta los detalles de implementación interna, mientras los datos requeridos y los resultados devueltos por la interfaz se mantengan intactos, el código interno del módulo puede reescribirse o mejorarse sin propagar modificaciones al resto del sistema.


---

## Tema 4 · Abstracción

Relaciona cada nivel de abstracción con su descripción correspondiente (completá con el número que corresponda a cada letra).

**8. Relaciona cada nivel con su descripción:**

| Nivel | N.º de descripción |
| --- | --- |
| A. Negocio / Requisitos | 2 |
| B. Diseño / Arquitectura | 3 |
| C. Implementación / Código | 1 |

1. Instrucciones concretas, escritas en un lenguaje de programación.
2. Qué problema resuelve el sistema para el usuario, sin detalles técnicos.
3. Cómo se organizan los componentes del sistema y cómo interactúan entre sí.

**9. Da un ejemplo de una situación cotidiana (no necesariamente de software) donde se apliquen distintos niveles de abstracción.**

_Respuesta:_ Conducir un automóvil:
Nivel Negocio / Requisitos: Necesito desplazarme del punto A al punto B de manera cómoda y segura.
Nivel Diseño / Arquitectura: Utilizo el volante para dirigir, el acelerador para avanzar y el freno para detener el auto.
Nivel Implementación / Código: La inyección electrónica de combustible, la transmisión de engranajes y la presión hidráulica del sistema de frenado.


---

## Tema 5 · Anticipación al cambio

**10. ¿Qué significa "anticipar el cambio" en el diseño de software? ¿Implica predecir exactamente qué va a cambiar en el futuro?**

_Respuesta:_ Significa diseñar previendo que el software va a evolucionar y adaptar sus componentes para reducir el costo de esos cambios. No implica adivinar ni predecir el futuro exacto, sino identificar las partes más volátiles del sistema y aislares mediante modularidad e interfaces.


**11. Para un sistema de pagos en línea, identifica una parte que probablemente cambie en el futuro y propone cómo aislarla del resto del sistema.**

_Respuesta:_ Parte propensa al cambio: El proveedor de la pasarela de pagos.
Cómo aislarla: Definiendo una interfaz o capa de abstracción común. De esta forma, las distintas pasarelas se implementan como adaptadores independientes y el sistema principal interactúa únicamente con la interfaz, sin importar la pasarela configurada.


---

## Tema 6 · Generalidad

**12. ¿Cuál es el riesgo de generalizar demasiado una solución? Da un ejemplo concreto de una solución "sobre-generalizada".**

_Respuesta:_ El riesgo principal es agregar complejidad innecesaria en el código, dificultando su comprensión, mantenimiento y desarrollo.  
Ejemplo de sobre-generalización: Crear un motor de reglas de cálculo personalizable súper complejo con lenguaje de expresiones propio solo para aplicar un descuento simple del 10% según el tipo de cliente.


---

## Tema 7 · Incrementalidad

**13. Explica la diferencia entre construir un sistema de forma incremental y construirlo todo de una vez ("big bang").**

_Respuesta:_ Incremental: Consiste en desarrollar y entregar el software en versiones sucesivas y funcionales. Permite obtener retroalimentación temprana del cliente y detectar/corregir errores a menor costo.  
"Big Bang": Consiste en intentar construir todo el sistema completo en una sola etapa masiva y probarlo/entregarlo al final. Esto eleva los riesgos, ya que los fallos o desalineaciones con las necesidades del cliente se descubren cuando el costo de corrección es máximo.


**14. Reflexión final: de los siete principios vistos en la Unidad 3, ¿cuál te parece más difícil de aplicar en la práctica, y por qué?**

_Respuesta:_ El principio de Anticipación al cambio suele ser el más difícil de aplicar en la práctica. La dificultad radica en encontrar el punto justo: si no se anticipa el cambio, el software se vuelve rígido y frágil; pero si se sobrediseña buscando cubrir cualquier escenario futuro imaginable, se cae en sobreingeniería y complejidad innecesaria. Saber cuándo abstraer y cuándo mantener las cosas simples requiere mucha experiencia en el dominio del problema.

