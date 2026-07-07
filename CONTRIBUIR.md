# Cómo añadir o actualizar un proyecto

Guía paso a paso pensada para trabajar entre dos personas sin pisaros el trabajo.

## Para añadir un proyecto nuevo

1. **Clona o actualiza tu copia local** del repositorio (`git pull` si ya lo tienes clonado).
2. **Crea una rama nueva** con un nombre descriptivo, por ejemplo:
   ```
   git checkout -b nuevo-proyecto-migracion-fronteriza
   ```
3. **Copia la plantilla**: duplica `proyectos/ejemplo-proyecto.md`, renómbrala con el `id` del proyecto (ej. `2026-migracion-fronteriza.md`) y rellena todos los campos.
4. **Añade una fila en `proyectos.csv`** con los mismos datos, respetando el `ESQUEMA.md` (vocabulario controlado, formato de fechas, etc.).
5. **Sube los cambios**:
   ```
   git add .
   git commit -m "Añade proyecto: migración fronteriza"
   git push origin nuevo-proyecto-migracion-fronteriza
   ```
6. **Abre un Pull Request** en GitHub. Esto permite que la otra persona revise antes de que se incorpore al repositorio principal — útil sobre todo al principio, mientras cogéis ritmo.
7. Una vez revisado, **haced merge** a la rama principal.

## Para actualizar un proyecto existente (ej. cambia de estado a "completado")

1. Edita directamente el archivo en `/proyectos/` y la fila correspondiente en `proyectos.csv`.
2. Mismo flujo de rama → commit → push → Pull Request.
3. **Nunca cambiéis el `id`** del proyecto al actualizarlo, aunque cambie el título o el estado.

## Evitar conflictos entre las dos personas

- Trabajad siempre en una rama distinta por cada proyecto o cambio, nunca directamente sobre la rama principal.
- Si vais a tocar el `proyectos.csv` a la vez, avisaos: es el archivo con más probabilidad de generar conflictos porque todo el mundo edita el mismo fichero.
- Una alternativa si esto se vuelve frecuente: dividir `proyectos.csv` en varios CSV (por año o por país) para reducir la probabilidad de que las dos edite la misma línea a la vez. No hace falta hacerlo ahora, pero tenedlo en mente si el repositorio crece mucho.

## Antes de hacer merge, revisar

- [ ] El `id` sigue el formato `AAAA-slug` y no se repite.
- [ ] Las fechas están en formato `AAAA-MM`.
- [ ] La `disciplina` usa exactamente uno de los términos del vocabulario controlado en `ESQUEMA.md`.
- [ ] El campo `contacto` solo incluye información que el investigador ha autorizado a hacer pública.
