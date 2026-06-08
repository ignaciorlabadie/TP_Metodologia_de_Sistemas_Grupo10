# git merge / git rebase

## ¿Qué hacen? 

- git merge nombre-rama combina los cambios de la rama indicada con la rama actual
- Si no hay conflictos, Git crea automáticamente un nuevo commit de merge
- Si existen conflictos, Git pide que se resuelvan antes de completar la operación

- git rebase nombre-rama toma los commits de la rama actual y los reaplica sobre la rama indicada.
- Reescribe el historial para que parezca que el trabajo comenzó desde la versión más reciente de la otra 
- rama
- A diferencia de merge, no crea un commit de unión

---

## ¿Para qué se usa?

- merge
- Se usa para integrar cambios realizados en distintas ramas del proyecto
- Unir funcionalidades desarrolladas 
- Mantener el historial completo de como evolucionaron las ramas
- Incorporar cambios de una rama a otra sin modificar el historial existente

- rebase 
- Actualizar una rama con los cambios más recientes de otra
- Evitar commits de merge innecesarios
- Facilitar la lectura del historial del proyecto

---

## ejemplos 

- merge
- Cambiar a la rama principal

- git switch main

- Fusionar la rama usuarios con main

- git merge usuarios

- rebase
- Situarse en la rama usuarios

- git switch usuarios

- Rebasar usuarios sobre main

- git rebase main


## detalles importantes

- El merge se realiza sobre la rama actual.
- Conserva el historial completo de ambas ramas.
- Puede generar conflictos si dos ramas modificaron las mismas líneas de código.
- Generalmente se utiliza para integrar ramas terminadas a main.

- El rebase reescribe el historial de commits.
- No genera un commit de merge.
- Puede producir conflictos que deben resolverse manualmente.
- No se recomienda hacer rebase sobre commits que ya fueron compartidos con otros desarrolladores.
- Se utiliza frecuentemente para actualizar una rama antes de hacer un merge a main.
