# git config --global user.name ""  
# git config --global user.email ""
 
## ¿Qué hacen?  
Estos comandos configuran los datos del autor en Git:  
- "user.name" → define el nombre que aparecerá en cada commit.  
- "user.email" → define el correo electrónico asociado a esos commits.  

---

## ¿Para qué se usan?  
Se utilizan para identificar quién realizó los cambios en el historial del repositorio.  
Además, permiten vincular tus commits con tu cuenta de GitHub.  
En proyectos colaborativos es fundamental, porque cada commit muestra el autor y su correo.  

---

## Ejemplos  
En la terminal:  
```bash
git config --global user.name "juan"
git config --global user.email "juan@gmail.com"
```

## Detalles importantes
- El parámetro --global aplica la configuración a todos los repositorios en la computadora, si se quiere utilizar para un solo repositorio, sacar --global y ejecutarlo dentro de la carpeta del repo.
- Se puede verificar con:
```bash
git config --global --list
```
