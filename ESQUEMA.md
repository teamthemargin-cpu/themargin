# Esquema de datos — proyectos.csv

Cada fila representa un proyecto de investigación. Estos son los campos y su significado.

| Columna | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `id` | texto | Sí | Identificador único y estable del proyecto, formato `AAAA-slug` (ej. `2026-migracion-fronteriza`). No cambia nunca aunque cambien otros datos. |
| `titulo` | texto | Sí | Título del proyecto tal como debe mostrarse públicamente. |
| `investigador` | texto | Sí | Nombre del investigador o investigadora principal. |
| `institucion` | texto | Sí | Institución de adscripción. |
| `pais` | texto | Sí | País donde se desarrolla la investigación (usar nombre completo, no código). |
| `disciplina` | texto | Sí | Área temática (usar el mismo vocabulario controlado en todos los proyectos — ver lista abajo). |
| `estado` | texto | Sí | Uno de: `en curso`, `completado`, `suspendido`. |
| `fecha_inicio` | fecha (AAAA-MM) | Sí | Fecha de inicio del proyecto. |
| `fecha_fin` | fecha (AAAA-MM) | No | Fecha de finalización (dejar vacío si sigue en curso). |
| `resumen_breve` | texto | Sí | 1-2 frases, lenguaje accesible (no el abstract técnico). |
| `archivo_detalle` | texto | Sí | Nombre del archivo Markdown correspondiente en `/proyectos/` (ej. `2026-migracion-fronteriza.md`). |
| `contacto` | texto | No | Email o enlace de contacto autorizado por el investigador para el público. |
| `enlace_uwazi` | texto | No | URL al perfil completo en Uwazi, una vez publicado ahí. |

## Vocabulario controlado sugerido para `disciplina`

Mantener esta lista fija evita que cada persona escriba la disciplina de forma distinta (ej. "Derecho" vs "derecho" vs "Legal"). Añadid aquí las que falten y usad siempre exactamente estos términos:

- Derecho
- Sociología
- Ciencia política
- Historia
- Antropología
- Economía
- Estudios de género
- Comunicación
- Otra (especificar en resumen_breve)

## Reglas de consistencia

- No dejar celdas con espacios en blanco donde el campo es obligatorio.
- Las fechas siempre en formato `AAAA-MM` (ej. `2026-03`), nunca `03/2026` ni `marzo 2026`.
- El `id` no se reutiliza ni se edita una vez creado, aunque el proyecto cambie de estado.
