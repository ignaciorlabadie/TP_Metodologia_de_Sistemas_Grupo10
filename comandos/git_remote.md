# git remote -v 

## ¿Qué hace?
- "git remote -v" → muestra las direcciones urls de los repositorios remotos, que están asociados al proyecto local.  
- Muestra la URL para **fetch** (descargar cambios) y también  **push** (subir cambios).  

---

## ¿Para qué se usa?
Se usa para:
- Verificar si tu proyecto está conectado a un repositorio remoto (por ejemplo, en GitHub).  
- Confirmar la URL del repositorio remoto.  

---

## Ejemplos
Ver los remotos configurados:
```bash
git remote -v
```
salida: 
```bash 
origin  https://github.com/usuario/proyecto.git (fetch)
origin  https://github.com/usuario/proyecto.git (push)
```

---

# git remote add
- Se usa para agregar un nuevo repo remoto,
ej,
```bash 
git remote add origin https://github.com/usuario/proyecto.git
```

# git remote set-url
- Se usa para cambiar la URL actual de un repo remoto ya existente,
ej,
```bash 
git remote set-url origin https://github.com/usuario/proyecto-nuevo.git
```
---

## Detalles importantes:
- El remoto por defecto, normalmente, es **origin**
- Se pueden usar más de un remoto (ej, origin para realizar un fork y upstream para el repo original).
- Si al ejecutar "git remote -v", no aparece nada → significa que el repo local no está asociado a ningún remoto.
- Es necesario tener configurado un remoto para poder publicar el proyecto en GitHub o para vincularlo con otros usuarios.