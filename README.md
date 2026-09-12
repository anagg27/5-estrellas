# 5 Estrellas — Trabajo Práctico Integrador

> Plantilla base para el repositorio del grupo. Reemplacen todo el texto entre `[corchetes]` por la información real de su proyecto.

Este repositorio contiene el análisis y diseño del sistema **5 Estrellas**, desarrollado como Trabajo Práctico Integrador de la asignatura **Ingeniería de Software**.

El sitio publicado en GitHub Pages es la entrega oficial del trabajo. **No se envían archivos impresos ni copias por otros medios.**

🔗 **Sitio publicado:** `https://anagg27.github.io/5-estrellas/`

---

## Integrantes del grupo

| Nombre completo | Rol / Responsabilidad principal | Usuario de GitHub |
|---|---|---|
| Vivian Frutos | Arquitecta de Software / Diseñadora de Datos | @Vivi-an99 |
| Araceli Franco | Diseñadora UI/UX / Analista de Sistemas | @aracelifrancofl-eng |
| Ana Girett | Analista de Requisitos | @anagg27 |

## Usuario / cliente real

**Ariel** — dueño de la despensa "5 Estrellas". Necesita el sistema porque actualmente gestiona ventas, créditos y stock de forma completamente manual (suma a mano, anota los créditos en un cuaderno o en una libreta del cliente, y no lleva ningún registro de stock)..

## Metodología de diseño y desarrollo elegida

**Metodología elegida:** Iterativa e Incremental, con modelado UML como soporte en cada etapa.

**Justificación:**

El grupo optó por una metodología iterativa e incremental porque se ajusta mejor a las características de este proyecto:

- **El trabajo está organizado en entregas sucesivas** (Conceptualización → Análisis → Diseño), donde cada una profundiza y agrega detalle sobre la anterior, en lugar de intentar definir todo el sistema de una sola vez. Esto es exactamente el espíritu de un enfoque iterativo e incremental.
- **Ariel, el cliente real, tiene disponibilidad limitada** para validar el sistema. Trabajar en incrementos pequeños permite mostrarle avances concretos (por ejemplo, el prototipo navegable) en distintos momentos, recoger su feedback y ajustar el rumbo sin haber invertido todo el esfuerzo de diseño de una sola vez.
- **El alcance está acotado pero puede afinarse con el uso real**: módulos como Ventas, Inventario y Clientes/Fiados se pueden refinar iteración a iteración a medida que entendemos mejor cómo trabaja Ariel día a día, sin necesidad de rehacer todo el análisis.
- **El modelado UML acompaña cada iteración** (diagramas de casos de uso, de clases, de secuencia, etc.), permitiendo documentar y comunicar las decisiones de diseño de forma clara entre las tres integrantes del grupo, y sirviendo de base directa para la futura implementación en Python (Django/Flask) con SQLite.
- **Reduce el riesgo del proyecto**: al validar en cada incremento que el sistema resuelve el problema real de Ariel (dejar de usar cuaderno y memoria), se evita llegar al final del trabajo práctico con un desarrollo desalineado de las necesidades del cliente.

---

## Entregas

| Entrega | Estado | Enlace |
|---|---|---|
| 1. Conceptualización | ✅ Entregado | [Ver documento](docs/conceptualizacion.md) |
| 2. Análisis | 🔲 Pendiente | [Ver documento](docs/analisis.md) |
| 3. Diseño | 🔲 Pendiente | [Ver documento](docs/diseno.md) |

## Estructura del repositorio

```
/docs           → contenido publicado en GitHub Pages (este es el sitio oficial de entrega)
  ├─ index.md          → página principal del sitio
  ├─ conceptualizacion.md
  ├─ analisis.md
  └─ diseno.md
/diagramas      → imágenes o archivos fuente de los diagramas (UML, mockups, etc.)
/src            → código fuente, si el grupo decide avanzar con una implementación
```

## Cómo publicar este sitio en GitHub Pages

1. Suban este repositorio a GitHub (público, o privado con acceso otorgado a la cátedra).
2. Vayan a **Settings → Pages**.
3. En **Source**, seleccionen la rama `main` (o `master`) y la carpeta **/docs**.
4. Guarden. GitHub publicará el sitio en `https://[usuario].github.io/[repositorio]/` en unos minutos.
5. Verifiquen que `docs/index.md` se muestre correctamente como página principal.
6. Actualicen el enlace del sitio arriba en este README y entréguenlo a la cátedra antes de la fecha límite de cada entrega.

> 💡 Tip: cada vez que hagan `push` a la rama publicada, el sitio se actualiza automáticamente. No es necesario volver a configurar nada en las siguientes entregas.
