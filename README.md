[README.md](https://github.com/user-attachments/files/29748811/README.md)

# The Margin — Catálogo público de investigación

Este repositorio es la **fuente de datos y el sitio público** de The Margin. Se publica como página web a través de GitHub Pages (`index.html`) y esa misma web lee directamente `proyectos.csv`. Uwazi queda como archivo interno de respaldo, no como cara pública.

## Estructura

```
the-margin-data/
├── index.html               # El sitio público (GitHub Pages sirve esto)
├── proyectos.csv             # Índice maestro con todos los proyectos (un renglón por proyecto)
├── proyectos/                 # Un archivo Markdown por proyecto, con el detalle completo
│   └── ejemplo-proyecto.md
├── ESQUEMA.md                 # Descripción de cada columna/campo
└── CONTRIBUIR.md              # Cómo añadir o actualizar un proyecto
```

## Cómo activar el sitio público (GitHub Pages)

1. En GitHub, entra al repositorio → **Settings** → **Pages** (menú de la izquierda).
2. En "Build and deployment" → "Source", elige **"Deploy from a branch"**.
3. En "Branch", selecciona `main` (o la rama principal que uséis) y la carpeta `/ (root)`.
4. Haz clic en **Save**.
5. En unos minutos, GitHub te dará la URL del sitio, con el formato:
   ```
   https://tu-usuario-u-organizacion.github.io/nombre-del-repositorio/
   ```
   Esa es la dirección pública y oficial de The Margin.

## Cómo se actualiza el sitio

No hace falta tocar `index.html` para añadir proyectos. Basta con:
1. Añadir una fila nueva en `proyectos.csv` (siguiendo `ESQUEMA.md`).
2. Añadir el archivo Markdown correspondiente en `/proyectos/`.
3. Subir los cambios (ver `CONTRIBUIR.md`).

GitHub Pages se actualiza solo, normalmente en 1-2 minutos tras cada cambio.

## Qué papel juega Uwazi ahora

Uwazi pasa a ser el archivo interno de trabajo: gestión de envíos, validación, campos internos no públicos. Cuando un proyecto está validado, sus datos públicos pasan a `proyectos.csv` para aparecer en el sitio.

## Licencia de los datos

_Pendiente de decidir — recomendado: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) para que cualquiera pueda reutilizar los datos citando la fuente._
