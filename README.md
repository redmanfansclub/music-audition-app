# Music Audition (Bilingual Master)

App web de audiciones musicales con huecos (fill-in-the-gaps) para el aula. Autor: Manuel Esteve (IES Infanta Elena).

## Qué hay en este repositorio
- `index.html`: la app completa (React + Tailwind + Babel desde CDN, todo en un archivo).
- `favicon-32.png`, `favicon-192.png`, `apple-touch-icon.png`, `icono_music_audition.svg`: iconos.
- `sql/music_audition_instalacion_completa.sql`: instala o actualiza todo lo que necesita Supabase. Se puede ejecutar varias veces sin borrar datos.
- `sql/cerrar_tablas_antiguas.sql` y `sql/limpieza_tablas_antiguas.sql`: opcionales (ver comentarios dentro).
- `docs/`: guía de instalación y de gestión de profesores (PDF y Word).

## Despliegue (GitHub Pages)
1. Ejecutar el SQL en Supabase → SQL Editor (si hay cambios en la base de datos).
2. Subir `index.html` (y los iconos si han cambiado) a la rama `main`.
3. Esperar a que termine "pages build and deployment" en la pestaña Actions y recargar a fondo (Cmd + Mayús + R).

## Datos y privacidad
- El proyecto de Supabase guarda tareas, entregas y la lista de alumnos de cada profesor. Las reglas (RLS) dejan a cada profesor ver solo lo suyo.
- **No subir a este repositorio (es público)** archivos de Plumier, copias de notas ni copias de la lista de alumnos. El `.gitignore` los bloquea.
- La copia de las tareas (JSON de History) no lleva datos personales y sí puede guardarse aquí.

## Restaurar
- Tareas: History → Import (carga el JSON de copia con los mismos enlaces).
- Lista de alumnos: Class list → Import JSON, o volver a subir los archivos de Plumier.
- Si Supabase pausa el proyecto por inactividad, reanudarlo desde su panel (botón Restore).

## Versión en castellano
Comparte tablas y funciones con esta (las tareas llevan el prefijo `aud-es-`). Cualquier cambio de SQL afecta a las dos.
