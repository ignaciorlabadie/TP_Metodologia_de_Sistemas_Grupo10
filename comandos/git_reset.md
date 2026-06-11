# Git reset

## ¿Qué hace?
- **"git reset"** → mueve el puntero de HEAD y la rama actual a un commit anterior.  
- Permite “volver atrás” en el historial, con diferentes niveles de impacto según la opción usada (**"--soft"** o **"--hard"**).  

---

## ¿Para qué se usa?
- Deshacer commits recientes.  
- Volver a un estado anterior del proyecto.  
- Ajustar el historial cuando se hicieron commits por error.  

---

## Ejemplos

### Reset --soft (mantiene cambios en staging)
```bash
git reset --soft HEAD~2
```
Esto vuelve 2 commits atrás, pero los cambios de esos commits siguen en el área de staging (listos para commitear nuevamente).

### Reset --hard (borra cambios)
```bash
git reset --hard HEAD~2
```
Vuelve 2 commits atrás y elimina completamente los cambios posteriores (los que estarían "adelante")
- Totalmente destructivo

---

## Detalles importantes: 
- **HEAD~n** → significa "n commits atrás" desde el commit actual.
- **--soft** → conserva los cambios en staging y puede ser revertido con "git reset"
- **--hard** → destructivo, borra todo.
- Si se realiza **"git reset --hard"**, y se tienen archivos sin commitear, se borran y no se pueden recuperar con "git reset"
- Para recuperar un commit perdido, usar **"git reset HEAD@{n}"**. Viendo desde **git reflog** el hash del commit y la referencia

---

# Ejemplo

1. Volver tres commits atrás pero manteniendo cambios:
```bash
git reset --soft HEAD~3
```

2. Volver cinco commits atrás y borrar todo lo posterior:
```bash
git reset --hard HEAD~5
```

3. Se hizo un reset --hard y se borraron los cambios posteriores. Se quiere volver a un commir anterior que ya no aparece en **"git log"** :
Paso 1, ver el reflog:
```bash
git reflog
```
ej de salida: 
```bash
537fa2e (HEAD -> alumno4_foricher_castellon) HEAD@{0}: commit: docs y refactor: agrego git remote y modifico git log
2394272 (origin/alumno4_foricher_castellon) HEAD@{1}: checkout: moving from dev to alumno4_foricher_castellon
fa93bfc (origin/dev, dev) HEAD@{2}: checkout: moving from alumno4_foricher_castellon to dev
2394272 (origin/alumno4_foricher_castellon) HEAD@{3}: commit: docs: Agrego info restante
```

Paso 2, elegir el commit a recuperar:
- Se puede usar el HEAD@{n}: 
```bash 
git reset HEAD@{2}
```
Restaura el repo a dos commits atrás

- Usando el hash:
```bash 
git reset 2394272
```
 
Esto restaura el repo exactamente al commit con el hash 2394272


---

# Git revert

## ¿Qué hace?
- **"git revert <commit>"** → crea un **nuevo commit** que revierte los cambios introducidos por el commit indicado.  
- No borra el historial, sino que añade un commit inverso.  
- Se usa para “deshacer” cambios de forma segura en repositorios compartidos, (como en este).  

---

## ¿Para qué se usa?
- Se quiere deshacer un commit que ya fue **pusheado** al remoto (ej, GitHub).  
- Necesitás mantener el historial intacto (no modificar commits anteriores).  
- Se quiere revertir un merge sin romper el historial compartido.  

---

## Ejemplos
1. Revertir un commit específico:
```bash
git revert abc123
```
Crea un nuevo commit que revierte el commit con hash abc123

2. Revertir varios commits:
```bash 
git revert abc123 def456
```
Crea un commit para revertir los commits con el hash abc123 y def456, respectivamente.

3. Revertir un merge commit:
```bash
git revert -m 1 <hash_del_merge>
```
- **-m 1**, quiere decir que te quedas con el historial de la rama actual y revierte lo que vino de la rama mergeada. 

---

# Detalles importantes:
- A diferencia de **"git reset"**, **no** borra commits, el historial se mantiene.
- Es mejor usar **"git revert"**, en trabajos colaborativos, porque se mantiene el historial y sigue en el "presente", no vamos a commits anteriores para restaurarlos. 

---

# Git clean

## ¿Qué hace?
- **"git clean"** → elimina archivos que **no están siendo trackeados por Git** (archivos **sin git add**).  
- Sirve para limpiar el directorio de trabajo de archivos temporales, pruebas o basura que no forman parte del repositorio.  

---

## ¿Para qué se usa?
- Se quiere borrar archivos generados automáticamente (logs, compilados, temporales).  
- Dejar la carpeta de trabajo limpia, solo con los archivos versionados.   

---

## Ejemplos

1. Ver qué se borraría 
```bash
git clean -n
```
Muestra qué archivos serían eliminados

2. Eliminar archivos no trackeados
```bash 
git clean -f
```
Borra los archivos que no están en el control de versiones (untracked)

3. Eliminar directorios no trackeados
```bash
git clean -fd
```
Borra archivos y carpetas untracked

4. Eliminar archivos ignorados por **.gitignore**
```bash 
git clean -fx
```
Borra los archivos listados en .gitignore

---

# Detalles importantes:
- Una vez eliminados, estos archivos no pueden ser recuperados con Git.
- Junto con **"git reset"**, sirven para mantener el repo limpio y consistente
    - git reset, deshace commits y mueve HEAD
    - git clean, borra archivos untracked  