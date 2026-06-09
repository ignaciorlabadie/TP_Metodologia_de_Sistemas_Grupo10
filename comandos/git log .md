# git log 

## ¿Qué hacen? 
- git log nos permite ver la historia del proyecto.
- Te permite ver quién hizo cada cambio, la fecha, el autor y un mensaje explicativo, ordenados de forma descendente del mas viejo al ultimo de todos los commits.


---

## ¿Para qué se usa?

- para visualisar la historia del proyecto


---

## ejemplos 

- git log --oneline
- Muestra un resumen de cada commit en una sola línea, ideal para ver de un vistazo qué ha pasado
- git log --oneline --graph --decorate
- Muestra un diagrama visual de las ramas y fusiones (merging) a la izquierda, junto con el historial
- git log --oneline ruta/al/archivo.ext
- Si necesitas rastrear cuándo y cómo se modificó un archivo en particular
- git log --author="TuNombre"
- git log --since="2 weeks ago"
- Puedes encontrar cambios específicos de forma rápida combinando filtros   

## detalles importantes

- git log no modifica archivos solamente nos permite ver el historial del proyecto.
- sirve como un mapa historico que nos ayuda si nesecitamos volver atras o eliminar algun commit