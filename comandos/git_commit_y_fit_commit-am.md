# git commit / git commit -am 

## ¿Qué hace?

El comando "git commit" guarda los cambios previamente preparados en el historial del repositorio.

Cada commit representa un punto en el tiempo del proyecto.

---

## ¿Para qué se usa?

Se usa para registrar cambios de forma permanente, permitiendo:

- Llevar un historial del proyecto
- Volver a versiones anteriores
- Trabajar en equipo de forma organizada

---

## Ejemplos:

Crear un commit con mensaje:

En la terminal:
git commit -m "feat: agregar login"

---

## Detalles importantes

- Solo guarda los cambios que fueron agregados con "git add".
- Cada commit debe tener un mensaje descriptivo.
- Es una buena práctica hacer commits pequeños y claros.
- Permite identificar fácilmente qué cambios se hicieron.

---

## Ejemplo práctico

En la terminal:
git commit -m "docs: agregar explicaciones de git init, add y commit"

---

## Un commit incluye:

- Cambios realizados
- Autor del cambio
- Fecha
- Mensaje escrito en el commit.

Esto ayuda a tener un historial claro del proyecto.

# git commit -am "<mensaje>"

## ¿Qué hace?

- "git commit -am "<mensaje>"" → crea un commit con mensaje y automáticamente incluye todos los archivos modificados, solamente los que ya estaban trackeados.  
- Es una combinación de "git add" + "git commit -m" en un solo comando.  

---

## ¿Para qué se usa?
Se usa para ahorrar tiempo cuando:
- Ya tenés archivos que Git conoce (trackeados).   

---

## Ejemplos
Crear un commit rápido con todos los archivos modificados:
```bash
git commit -am "fix: corregir bug en login"
``` 