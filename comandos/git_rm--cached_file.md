# git rm --cached <file>

## ¿Qué hace?
- "git rm --cached <file>" → elimina el archivo del índice de Git (staging area), pero no lo borra de la carpeta local.  
- El archivo deja de estar “trackeado” por Git, aunque sigue existiendo en el proyecto.

---

## ¿Para qué se usa?
Se usa cuando:
- Se agrega un archivo por error con "git add" y no se desea incluirlo en el commit.  
- Se quiere dejar de versionar un archivo (ejemplo: ".env", archivos temporales o configuraciones locales).  
- Se quiere limpiar el repositorio, haciendo que Git ignore ese archivo en el futuro (junto con ".gitignore").  

---

## Ejemplos
Dejar de trackear un archivo "config.json":
```bash
git rm --cached config.json
git commit -m "Dejar de trackear config.json"
```
---

## Detalles importantes: 
- El archivo no se borra de la carpeta local, se elimina solo del control de versiones. 
- Para borrarlo de la carpeta local usar "git rm <file>"
