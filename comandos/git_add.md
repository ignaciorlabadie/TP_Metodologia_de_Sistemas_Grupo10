# git add

## ¿Qué hace?

El comando "git add" se usa para agregar archivos al área de preparación (staging area).
Esto indica qué cambios serán incluidos en el próximo commit.

---

## ¿Para qué se usa?

Se usa para seleccionar qué modificaciones querés guardar en el historial del repositorio.
Permite decidir exactamente qué cambios incluir antes de confirmar (la confirmación sería elcommit).

---

## Ejemplos

Agregar un archivo específico:

En la terminal:
git comandos/add git_add.md

Agregar todos los archivos modificados:
git add .

---

## Detalles importantes

- "git add" no guarda cambios definitivamente, solo los prepara. Es posible quitarlos del staging area.
- Es el paso previo que tenés que usar si queres hacer "git commit".
- Permite agregar archivos de forma selectiva o agregar todos (git add .).
- Si modificás un archivo después de hacer "git add", tenés que volver a agregarlo.

---

## Ejemplo:

terminal:
git add index.html
git add app.js

Se preparan ambos archivos para ser incluidos en el próximo commit.
