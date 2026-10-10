# Guía para trabajar en equipo

Reglas sencillas para que nadie pise el trabajo de los demás.

## 1. Cada rol, su carpeta

| Rol | Carpeta principal | Qué sube |
|-----|-------------------|----------|
| Backend | `codigo/backend/` | Código del servidor, API, base de datos |
| Frontend | `codigo/frontend/` | Código de la interfaz |
| Scrum Master | `docs/scrum/` | Backlog, sprints, dailies, retrospectivas |
| Project Manager | `docs/pm/` | Plan del proyecto, cronograma, riesgos, informes |

Regla simple: **trabaja solo dentro de tu carpeta**. Si necesitas cambiar algo de otra, avisa a esa persona o a todo el grupo.
Imágenes, diagramas y capturas van en `imagenes/` y los documentos comunes (enunciado, bibliografía, entrega final) en `docs/general/`.

## 2. Rama y revisión

**Nunca trabajen directamente en `main`.** Cada persona trabaja en una rama con el nombre de su rol:

- `backend/login-api`
- `frontend/pantalla-inicio`
- `scrum/sprint-1`
- `pm/plan-de-proyecto`

Después se abre un **Pull Request** hacia `main` y otra persona lo revisa antes de aprobarlo:

- Backend y Frontend se revisan entre sí.
- Scrum y PM se revisan entre sí.

## 3. Si usas Git en la terminal (normalmente backend y frontend)

```bash
# Primera vez
git clone https://github.com/EstebanBurgos2903/GRUPO-3---ADMINISTRACION-DE-PROYECTOS.git
cd GRUPO-3---ADMINISTRACION-DE-PROYECTOS

# Cada vez que empieces
git checkout main
git pull
git checkout -b backend/login-api

# Trabajar y guardar
git add .
git commit -m "Agrega endpoint de login"
git push -u origin backend/login-api
```

Luego abre el Pull Request en GitHub.

## 4. Si prefieres la página web de GitHub (útil para Scrum y PM)

No necesitas instalar nada:

1. Entra a la carpeta donde vas a subir (por ejemplo `docs/pm`).
2. Presiona **Add file → Upload files** y arrastra tus archivos.
3. Escribe un mensaje corto de lo que subes.
4. Marca **Create a new branch for this commit and start a pull request** y dale a *Commit changes*.
5. Abre el Pull Request y pide a un compañero que lo apruebe.

Límite de la web: **25 MB por archivo**. Para algo más pesado (videos), usen Google Drive y pongan el enlace en el README.

## 5. Mensajes de commit

Cortos y claros, en presente:

- ✅ `Agrega plan de proyecto v1`
- ✅ `Corrige validación del formulario`
- ❌ `cambios`, `arreglos`, `asdf`

## 6. Nombres de archivos

- Sin espacios ni tildes: usa guiones (`plan-proyecto.pdf`, no `Plan Proyecto.pdf`).
- Minúsculas.
- Si hay versiones, usa fecha: `avance-2026-10-15.pdf`.

## 7. Resolver conflictos

Si Git dice que hay un conflicto:

1. Abre el archivo y busca las marcas `<<<<<<<`, `=======`, `>>>>>>>`.
2. Decide con tu compañero qué versión se queda y borra las marcas.
3. `git add archivo` y `git commit`.

Trabajar cada quien en su carpeta reduce mucho esto.

## 8. Reparto de tareas

Usen la pestaña **Issues**: cada tarea es un issue asignado a una persona. Pueden organizarlos en **Projects** (tablero tipo Kanban), que además le sirve al Scrum Master y al PM para dar seguimiento.
