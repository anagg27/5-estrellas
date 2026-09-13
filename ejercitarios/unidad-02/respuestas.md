# Respuestas — Ejercitario Unidad 02

> Completen cada pregunta debajo de su enunciado. Pueden borrar este bloque de instrucciones una vez que empiecen.

---

## Tema 1 · La naturaleza del software

**1. En tus propias palabras, explica por qué se dice que el software es un producto de "naturaleza particular" en comparación con un producto físico. Menciona al menos tres características distintivas.**

_Respuesta:_
Se dice que el software es de naturaleza particular porque no se comporta como los objetos fisicos que podemos tocar y fabricar. Estas serian las 3 caracteristicas
1. No se desgastan con el uso
2. Es complejo e invisible
3. Es maleable y se construye a medida 


**2. ¿Por qué se afirma que la calidad del software se degrada por mal mantenimiento y no por el paso del tiempo? Da un ejemplo.**

_Respuesta:_
Se afirma eso porque el software no es físico. Ejemplo un producto físico como una bici sí se oxida, se rompe o se gasta solo con el paso del tiempo, en cambio un código de software no envejece solo, mientras esté guardado en un disco, va a seguir siendo el mismo código dentro de 10 años.


---

## Tema 2 · Requisitos funcionales y no funcionales

**3. Explica con tus propias palabras la diferencia entre un requisito funcional y un requisito no funcional.**

_Respuesta:_
Un requisito funcional basicamente seria el que debe hacer el sistema, son las acciones del sistema. iniciar sesion, guardar datos, enviar mensajes.
Un requisito no funcional seria como debe hacerlo, la calidad del sistema. Que sea rapido, seguro y facil de usar.

**4. Para el siguiente caso, identifica un requisito funcional y tres requisitos no funcionales de categorías distintas: "Una aplicación de delivery de comida debe permitir a los usuarios rastrear su pedido en tiempo real."**

_Respuesta:_
Para el requisito funcional el sistema debe permitir a los usuarios rastrear su pedido en tiempo real en un mapa, es el QUE hace la app seria la acciones del sistema.
Y los 3 requisitos no funcionales serian,
1. El rendimiento que la ubicación del pedido debe actualizarse cada 5 segundos máximo.
2. La eficiencia de  la pantalla de rastreo debe ser fácil de entender para cualquier usuario sin manual.  
3. La seguridad que solo el usuario que hizo el pedido y el repartidor pueden ver la ubicación en tiempo real.  
4. La seguridad.

**5. Menciona dos razones por las cuales los requisitos no funcionales suelen entrar en conflicto entre sí. Da un ejemplo concreto de ese conflicto.**

_Respuesta:_
Las razones principales seria que compiten por los mismos recursos y buscan objetivos opuestos. Un ejemplo concreto seria La app de delivery.El primer requisito seria el rendimiento de la app, debe actualizar la ubicación del pedido cada 1 segundo para que sea bien en tiempo real. El siguiente requisito la eficiencia, la app debe gastar poca batería del celular para que al usuario no se le descargue si actualizas la ubicación cada 1 segundo, usas GPS y datos a cada rato. Eso hace que la batería se descargue rapidísimo.
Para ahorrar batería tendria que actualizar cada 30 segundos, pero ahí ya no es tiempo real por eso el equipo tiene que negociar si cada 5 segundos está bien para ambos.

---

## Tema 3 · Clasificación de las cualidades del software

**6. Completa el siguiente cuadro clasificando cada elemento como cualidad "de producto" o "de proceso", y justifica brevemente tu respuesta.**

| Elemento | ¿Producto o proceso? | Justificación |
| --- | --- | --- |
| Tiempo de respuesta de una aplicación móvil |Producto  | Porque es una característica que se percibe en el software ya terminado. El usuario final experimenta al usar la app.|
| Capacidad del equipo de estimar correctamente los plazos de entrega |Proceso | Porque se refiere a una actividad del equipo de desarrollo, es la parte de cómo se gestiona y ejecuta el proyecto, no del producto final. |
| Facilidad de uso de una interfaz |Producto |Porque es un atributo de calidad del software entregado, porque el usuario evalúa al interactuar con la interfaz |
| Documentación interna del código fuente |Proceso | Porque es un artefacto que se genera durante el desarrollo para apoyar el mantenimiento y trabajo del equipo. No ve el usuario final.|

**7. ¿Por qué se dice que una buena calidad interna favorece, pero no garantiza, una buena calidad externa? Da un ejemplo de un software con buena calidad interna pero mala calidad externa, o viceversa.**

_Respuesta:_
Favorece pero no garantiza porque tener buen código interno hace más probable que el producto sea bueno. Si el código es ordenado, es más fácil de corregir errores, agregar funciones y que no se caiga.
Pero... podes tener un código perfecto y aún así entregar un producto que al usuario no le sirve. Y al revés podes tener un producto que al usuario le encante aunque por dentro sea un desastre.
ejemplo, Buena calidad interna, mala calidad externa una app de banco con código perfecto y súper seguro, pero es lentísimo y nadie entiende cómo transferir plata.
Los programadores felices,pero los usuarios lo desinstalan.
---

## Tema 4 · Cualidades representativas

Relaciona cada cualidad con su definición correspondiente (completá con el número que corresponda a cada letra).

| Cualidad | N.º de definición |
| --- | --- |
| A. Corrección | _3__ |
| B. Fiabilidad | _6__ |
| C. Robustez | _4__ |
| D. Eficiencia | _2__ |
| E. Mantenibilidad | __5_ |
| F. Interoperabilidad | _1__ |


1. Capacidad de coexistir e intercambiar información con otros sistemas.
2. Uso adecuado de los recursos disponibles: tiempo de procesamiento, memoria, ancho de banda.
3. El software hace exactamente lo que su especificación indica, ni más ni menos.
4. Comportamiento razonable frente a situaciones no anticipadas por la especificación.
5. Facilidad para corregir errores y adaptar o mejorar el software.
6. Capacidad de funcionar sin fallar durante un período y bajo condiciones dadas.

**8. Elige dos cualidades representativas distintas a las de la actividad anterior (por ejemplo, usabilidad, portabilidad o reusabilidad) y da un ejemplo concreto —de una app, sistema o servicio real— donde esa cualidad sea especialmente crítica.**

_Respuesta:_
Usabilidad es la facilidad con la que un usuario común puede aprender y usar el software, un ejemplo concreto seria Google Maps
es crítica porque usan personas de 8 a 80 años, apurados, manejando, sin leer manuales.
Si el botón de "ir" estuviese escondido o las indicaciones fuesen confusas, la app no serviría.
Su éxito depende 100% de que cualquiera pueda abrir y llegar a destino en 3 clics. 

**9. Caso breve: un equipo de desarrollo debe elegir entre optimizar la eficiencia de un sistema (tiempos de respuesta más rápidos) o su mantenibilidad (código más simple y modular), dado que el tiempo de desarrollo es limitado. ¿Qué factores debería considerar el equipo para tomar esa decisión?**

_Respuesta:_
Ejemplo un sistema de cobro de peaje en autopista, la decisión seria priorizar la  eficiencia.
Porque si el lector de TAG tarda 3 segundos en abrir la barrera, se forma una fila de 2km en 10 minutos. Los autos se enojan, hay accidentes y la autopista pierde miles por día.

---

## Tema 5 · Calidad según el dominio de aplicación

**10. Completa el siguiente cuadro indicando qué cualidades consideras prioritarias para cada tipo de sistema, y por qué.**

| Tipo de sistema | Cualidades prioritarias | ¿Por qué? |
| --- | --- | --- |
| Sistema de control de una planta industrial |Fiabilidad, Seguridad, Eficiencia | Porque un fallo puede causar accidentes, daños millonarios o parar toda la producción. Debe responder en tiempo real y no fallar nunca.|
| Red social de uso masivo |Usabilidad y Disponibilidad | Porque usan millones de personas a la vez desde celulares distintos. Si es difícil de usar se van, y si se cae en horas pico pierde usuarios y publicidad.|
| Sistema de trading financiero de alta frecuencia |Eficiencia, Fiabilidad, Integridad | Porque opera en milisegundos. 1ms de retraso y millones perdidos. Además debe ejecutar las órdenes correctas y sin errores, porque maneja dinero real.|

**11. En tu opinión, ¿es válido que un sistema de consumo masivo tolere una tasa de fallos mayor que un sistema crítico, a cambio de salir antes al mercado? Justifica tu postura.**

_Respuesta:_
En m opinion un sistema de consumo masivo sí puedes tolerar más fallos para salir antes, porque el costo de un fallo es bajo.
En un sistema crítico no, porque el costo de un fallo es altísimo. Porque en un sistema de consumo masivo, si hay un bug la gente se queja pero no muere nadie. Lo arreglas con una actualización mañana.
Pero si salis tarde al mercado, ya te ganó la competencia y perdiste todos los usuarios.En cambio en un sistema crítico el fallo cuesta vidas o millones, por eso ahí no se puede apurar.

---

## Tema 6 · Medición de la calidad del software

**12. Explica con tus propias palabras por qué se dice que una métrica es "un indicador indirecto de la cualidad, y no la cualidad en sí misma".**

_Respuesta:_
Porque la métrica mide un número y la cualidad es una idea. Ejemplo la cualidad "Seguridad". No podes medir "seguridad" directo. en cambio la 
métrica de N° de accesos no autorizados al mes. Ese número solo te da una pista de qué tan segura es. Por eso la métrica es un indicador indirecto porque te acerca a la cualidad, pero no es la cualidad. Puedes tener buen número y aún así el sistema sentirse inseguro.

**13. Menciona un riesgo concreto de que un equipo se enfoque en mejorar una métrica de calidad (por ejemplo, bajar la complejidad ciclomática) sin revisar si la cualidad real mejoró.**

_Respuesta:_
 Un riesgo seria el equipo se obsesiona con bajar la complejidad ciclomática.Para lograr parten una función gigante de 200 líneas en 20 funciones chiquitas de 10 líneas, la métrica baja un montón y todos felices.Pero la cualidad real empeoró, la mantenibilidad para entender qué hace el código tenes que saltar entre 20 archivos distintos. Es más difícil de leer y de cambiar. Y ahi entendes que mejoraron la métrica, pero el código se volvió menos mantenible en la práctica.Por eso si solo miras el número, podes tener buenas métricas con un mal sistema.

**14. Reflexión final: de todo lo visto en la Unidad 2 (naturaleza del software, requisitos no funcionales, clasificación de cualidades, cualidades representativas, calidad según el dominio, medición), ¿qué idea te resultó más relevante y por qué?**

_Respuesta:_
La idea más relevante para mí fue La calidad depende del dominio. Porque te obliga a dejar de buscar el software perfecto y empezar a buscar el software correcto para este problema.
