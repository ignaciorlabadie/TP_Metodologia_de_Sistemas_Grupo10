# git branch / git checkout / git switch  

## ¿Qué hacen?  
- "git branch" → lista todas las ramas del repositorio. La rama actual aparece marcada con un "*".  
- "git branch nombre-rama" → crea una nueva rama llamada "nombre-rama".  
- "git checkout nombre-rama" / "git switch nombre-rama" → cambia a la rama indicada.  
- "git checkout -b nombre-rama" / "git switch -c nombre-rama" → crea una nueva rama y cambia directamente a ella.  
- "git branch -d nombre-rama" → elimina la rama indicada.  

---

## ¿Para qué se usan?  
Se usan para trabajar con diferentes versiones del proyecto sin afectar la rama principal.  
Permiten:  
- Organizar el trabajo en paralelo (cada rama puede tener una funcionalidad distinta).  
- Probar cambios sin riesgo de romper el código principal.  
- Eliminar ramas que ya no se necesitan.  

---

## Ejemplos  
Listar ramas existentes:  
```bash
git branch
```
Crear una rama llamada "usuarios":
```bash
git branch usuarios
```
Cambiar a la rama usuarios:
```bash 
git checkout usuarios
git switch usuarios
```
Crear y cambiar a la rama prueba:
```bash
git checkout -b prueba
git switch -c prueba
```
Eliminar la rama prueba:
```bash 
git branch -d prueba
```

---

### Detalles importantes:
- La rama actual aparece marcada con * en la lista (git branch)
- No se puede eliminar la rama en la que estás parado (git branch -d nombre-rama)
- Si se elimina una rama con commits que no fuerpn mergeados, esos commits se pierden