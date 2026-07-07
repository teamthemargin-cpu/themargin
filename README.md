# The Margin — Datos de investigación

Este repositorio es el **respaldo abierto y versionado** de los proyectos de investigación recogidos por The Margin. Es la fuente de datos en bruto; la interfaz pública de búsqueda y filtrado vive en Uwazi.

## Estructura

```
the-margin-data/
├── proyectos.csv          # Índice maestro con todos los proyectos (un renglón por proyecto)
├── proyectos/              # Un archivo Markdown por proyecto, con el detalle completo
│   └── ejemplo-proyecto.md
├── ESQUEMA.md               # Descripción de cada columna/campo
└── CONTRIBUIR.md            # Cómo añadir o actualizar un proyecto
```

## Cómo se relaciona con Uwazi

1. Los investigadores rellenan el formulario de captura.
2. Se valida la información y se añade una fila en `proyectos.csv` + un archivo en `/proyectos/`.
3. Desde ahí se sube (o exporta vía CSV) a Uwazi para que el público pueda buscar y filtrar.

Este repo no sustituye a Uwazi: es la copia de seguridad histórica, auditable y de acceso libre de los mismos datos.

## Licencia de los datos

_Pendiente de decidir — recomendado: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) para que cualquiera pueda reutilizar los datos citando la fuente._
