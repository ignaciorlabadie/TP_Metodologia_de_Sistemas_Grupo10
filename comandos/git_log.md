# Git log 

## ¿Qué hacen? 
- Git log nos permite ver la historia del proyecto.
- Te permite ver quién hizo cada cambio, la fecha, el autor y un mensaje explicativo, ordenados de forma descendente del mas viejo al ultimo de todos los commits.


---

## ¿Para qué se usa?

- Para visualisar la historia del proyecto


---

## Ejemplos 

- Git log --oneline
- Muestra un resumen de cada commit en una sola línea, ideal para ver de un vistazo qué ha pasado
- Git log --oneline --graph --decorate
- Muestra un diagrama visual de las ramas y fusiones (merging) a la izquierda, junto con el historial
- Git log --oneline ruta/al/archivo.ext
- Si necesitas rastrear cuándo y cómo se modificó un archivo en particular
- Git log --author="TuNombre"
- Git log --since="2 weeks ago"
- Puedes encontrar cambios específicos de forma rápida combinando filtros.

---

## Detalles importantes:

- Git log no modifica archivos solamente nos permite ver el historial del proyecto.
- Sirve como un mapa historico que nos ayuda si nesecitamos volver atras o eliminar algun commit

---
# Git reflog

## ¿Qué hace?
- **"git reflog"** → muestra el historial de movimientos y acciones realizadas en el repositorio local.  
- Incluye:
     - Commits
     - Merges
     - Resets
     - Checkouts
     - Cualquier cambio en las referencias (HEAD).  
- Permite ver incluso commits que ya no aparecen en "git log" porque fueron descartados o reescritos.

---

## ¿Para qué se usa?
- Recuperar commits perdidos después de un **"reset"** o un **"rebase"**.  
- Ver qué acciones fueron realizadas en el repo (ejemplo: cambios de rama, merges, resets).  
- Tener un registro más detallado que **"git log"**, porque guarda la historia de los movimientos de HEAD.  

---

## Ejemplos
Ver el historial de acciones:
```bash
git reflog
```
Ejemplo de salida:
```bash 
2394272 (HEAD -> alumno4_foricher_castellon, origin/alumno4_foricher_castellon) HEAD@{0}: checkout: moving from dev to alumno4_foricher_castellon
fa93bfc (origin/dev, dev) HEAD@{1}: checkout: moving from alumno4_foricher_castellon to dev
2394272 (HEAD -> alumno4_foricher_castellon, origin/alumno4_foricher_castellon) HEAD@{2}: commit: docs: Agrego info restante
```

---

## Detalles importantes:
- "git reflog" es local, por ende no muestra el historial remoto, solo lo que paso en la máquina donde se ejecuta el comando.
- Sirve para recuperar commits borrados o sobreescritos.
- Cada entrada tiene un índice (HEAD@{n}) que se puede usar para volver a ese estado. (Donde n es un entero, comenzando de **0** siendo el estado actual del repo, **1** la acción anterior a la actual, **2** dos pasos atrás, y así sucesivamente). 
- A diferencia del **"git log"**, el **"reflog"** guarda los movimientos internos de HEAD, no solo los commits visibles (git log).
