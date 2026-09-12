# Respuestas — Ejercitario Unidad 01

> Completen cada pregunta debajo de su enunciado. Pueden borrar este bloque de instrucciones una vez que empiecen.

---

## Tema 1 · Ingeniería de software: una visión previa

**1. En tus propias palabras, define qué es la Ingeniería de Software.**

_Respuesta:_ Para mí, la ingeniería de software es básicamente la disciplina que agarra todo el desarrollo,
la operación y el mantenimiento de un sistema y le aplica un enfoque súper metódico,
ordenado y medible.


**2. Explica con un ejemplo la diferencia entre "programar" y "hacer ingeniería de software".**

_Respuesta:_ Programar: Escribir una función en Python para calcular el precio final con impuestos de un carrito
de compras.
Hacer ingeniería de software: Diseñar y desplegar una plataforma de comercio electrónico completa
que gestione miles de transacciones concurrentes, integre pasarelas de pago seguras, almacene
datos de forma estructurada, incluya pruebas automatizadas continuas y permita que un equipo de
desarrolladores colabore de manera sincronizada sin comprometer la estabilidad del sistema.


**3. Menciona dos razones por las cuales la ingeniería de software es necesaria en el desarrollo de sistemas actuales.**

Gestión de la complejidad y escalabilidad: Los sistemas modernos son masivos y están compuestos
por múltiples servicios interconectados. La ingeniería de software proporciona metodologías,
patrones de diseño y herramientas que permiten que las aplicaciones crezcan de forma ordenada,
mantenible y sostenible.
Garantía de calidad y confiabilidad: A través de procesos estructurados de pruebas, control de
versiones y gestión de riesgos, asegura que el software sea seguro, tolerante a fallos y funcione de
manera predecible bajo alta demanda, minimizando errores críticos.

---

## Tema 2 · El rol de la IS en el diseño de sistemas (+ impacto de la IA)

**4. Enumera los elementos que conforman un sistema basado en computadora, además del software.**

_Respuesta:_Un sistema basado en computadora integra varios elementos; el software es solo uno de ellos.
Software
Hardware
Personas
Bases de datos
Documentación
Procedimientos


**5. Describe brevemente la diferencia entre una visión sistémica y una visión aislada del software en el diseño de sistemas.**

_Respuesta:_Visión aislada

El software se piensa como un producto independiente,
Desconectado del entorno donde va a operar.
Visión sistémica
El software se diseña como parte de un sistema completo:
personas, procesos, datos y hardware trabajando juntos.


**6. Elige una herramienta de inteligencia artificial aplicada al desarrollo de software (por ejemplo, un asistente de código o de testing) e indica:**
- Qué tarea del ingeniero de software apoya o transforma.
- Un beneficio concreto que ofrece.
- Un riesgo o desafío que introduce su uso.

_Respuesta:_ Qué tarea apoya o transforma:
Apoya y transforma la tarea de escritura de código y generación de boilerplate (código repetitivo o
estructural), así como la redacción inicial de pruebas unitarias y la documentación de funciones.

Un beneficio concreto que ofrece:
Aumenta significativamente la velocidad de desarrollo al autocompletar bloques de código
complejos o sugerir implementaciones basadas en comentarios en lenguaje natural, reduciendo el
tiempo dedicado a buscar sintaxis o escribir estructuras repetitivas.

Un riesgo o desafío que introduce su uso:
Introduce el riesgo de introducir vulnerabilidades de seguridad o código obsoleto/ineficiente, ya que
la IA puede sugerir fragmentos que parecen correctos pero que contienen fallos lógicos o malas
prácticas que el desarrollador pasa por alto si no realiza una revisión rigurosa.


---

## Tema 3 · Historia de la ingeniería de software

**7. En tu opinión, ¿por qué la "crisis del software" de 1968 marcó un punto de inflexión para la disciplina?**

_Respuesta:_ Fue clave porque expuso que el desarrollo ya no podía seguir siendo una actividad improvisada. Los proyectos
de la época sufrían retrasos constantes, sobrecostos y fallas graves, lo que demostró que construir software
complejo requería la misma disciplina que otras ingenierías (planificación, documentación, control de calidad)
y a partir de ese momento se empezó a hablar formalmente de "ingeniería de software" como disciplina,
sentando las bases para metodologías y procesos estructurados.

**Ejercicio de relación** (completá con la letra que corresponda a cada número):

| Evento / Período | Descripción |
|---|---|
| A. Programación artesanal (1950s–60s) | _3__ |
| B. Crisis del software (1968) | __1_ |
| C. Modelo en cascada (1970s–80s) | __5_ |
| D. Métodos iterativos (1990s) | __4_ |
| E. Metodologías ágiles (2001–hoy) | _2__ |

1. Se acuña el término "ingeniería de software" en una conferencia de la OTAN ante fallas y sobrecostos de proyectos.
2. Surge el Manifiesto Ágil; se popularizan Scrum, Kanban y XP.
3. El software se escribía de forma individual, sin procesos formales.
4. Ganan terreno la iteración, el prototipado y los modelos incrementales.
5. Se establecen los primeros procesos formales y estructurados de desarrollo.

---

## Tema 4 · El rol del ingeniero de software

**8. Menciona tres competencias que debe tener un ingeniero de software, además del conocimiento técnico.**

_Respuesta:_Resolución de problemas complejos
Comunicación y trabajo en equipo
Responsabilidad y ética profesional


**9. Describe brevemente qué hace cada uno de los siguientes roles dentro de un equipo de desarrollo:**

| Rol | Descripción |
|---|---|
| Analista |Se encarga de entender qué necesita el usuario y traducirlo en especificaciones claras. |
| Arquitecto | Define la estructura general del sistema|
| Desarrollador |Implementa el software, transformando el diseño y los requisitos en código funcional. |
| Tester / QA | Verifica la calidad del software y detecta defectos antes de que el producto llegue al

usuario final|

**10. Caso breve:** Un ingeniero de software descubre, cerca de la fecha de entrega, una falla de seguridad que podría exponer datos de usuarios, pero corregirla retrasaría el proyecto una semana. ¿Qué debería hacer y por qué, considerando la ética profesional?

_Respuesta:_ Considerando la ética profesional lo correcto sería informar de inmediato la falla al equipo y a los responsables del
proyecto, aunque esto implique retrasar la entrega una semana. Corregir la falla antes de lanzar es una obligación ética,
exponer datos de usuarios podría causar un daño real a las personas, además de consecuencias legales y de reputación
graves. Priorizar una fecha de entrega por sobre la seguridad de los usuarios sería anteponer un interés comercial a corto
plazo a la responsabilidad profesional, algo que contradice los principios básicos de la disciplina.


---

## Tema 5 · El ciclo del software

**11. Ordena y nombra las cinco fases genéricas del ciclo de vida del software vistas en clase.**

_Respuesta:_ 1. Análisis 2. Diseño 3. Implementación 4. Pruebas 5. Mantenimiento 


**12. ¿Por qué se afirma que el mantenimiento suele ser la fase más costosa del ciclo de vida del software? Da un ejemplo hipotético.**

_Respuesta:_ Se afirma que es la fase más costosa porque el software "vive y cambia mucho después de su primera entrega". Ejemplo hipotético: Imagina que un equipo desarrolla una aplicación de compras en 6 meses (fases 1 a 4). Sin embargo, durante los siguientes 10 años, la aplicación debe actualizarse constantemente para integrar nuevos métodos de pago, parches de ciberseguridad, cambios en las leyes de impuestos y mejoras solicitadas por los clientes. Todo el tiempo, esfuerzo y salario invertido en esos 10 años superará con creces el costo de los 6 meses de desarrollo inicial. 


---

## Tema 6 · Relación con otras áreas de la ciencia de la computación

**Completen el siguiente cuadro indicando cómo cada área apoya a la ingeniería de software.**

| Área | ¿Cómo apoya a la Ingeniería de Software? |
|---|---|
| Estructuras de datos y algoritmos |Son la base para diseñar soluciones eficientes. | 
| Bases de datos | Permiten el modelado y la gestión de la información del sistema.|
| Sistemas operativos |Entienden el entorno donde el software se ejecuta. |
| Redes | Soportan los sistemas distribuidos y su comunicación. |
---

## Tema 7 · Relación con otras disciplinas

**13. Elige dos de las siguientes disciplinas — Administración, Psicología, Economía, Derecho, Comunicación — y explica con un ejemplo concreto cómo se relacionan con el trabajo diario de un ingeniero de software.**

_Respuesta:_  Psicología: Se relaciona a través del diseño centrado en el usuario y la ergonomía. Ejemplo concreto: Un ingeniero de software que diseña una aplicación para adultos mayores debe aplicar principios de psicología y ergonomía para que los botones sean grandes, los colores generen confianza y la navegación no produzca frustración o estrés en el usuario final. ● Derecho: Aporta conocimientos sobre propiedad intelectual, contratos y normativa. Ejemplo concreto: Antes de lanzar una red social, el ingeniero debe colaborar con el equipo legal para asegurarse de que el código base no infrinja patentes (propiedad intelectual) y de que la forma en que se guardan los datos cumpla con las normativas de privacidad vigentes en el país. 


**14. Reflexión final:** de todo lo visto en clase (definición, historia, rol del ingeniero, ciclo del software, relación con otras áreas y disciplinas, e impacto de la IA), ¿qué idea te resultó más relevante y por qué?
La idea que me resultó más relevante es el impacto actual de la IA en la Ingeniería de Software. Me parece fascinante cómo ha cambiado el paradigma: ahora el ingeniero no solo escribe código, sino que asume un rol de validación, supervisión y corrección de las salidas generadas por la IA. Esto es crucial porque nos demuestra que la carrera no se trata solo de teclear rápido, sino de tener el criterio para resolver problemas complejos y manejar nuevos desafíos, como los sesgos, la seguridad y la dependencia de herramientas externas. 

_Respuesta:_

