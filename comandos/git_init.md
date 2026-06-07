## git init

## ¿Qué hace?

El comando "git init" se utiliza para inicializar un repositorio Git en una carpeta.
Esto convierte una carpeta común en un repositorio con versiones, permitiendo empezar a registrar cambios.

---

## ¿Para qué se usa?

Se usa cuando querés comenzar un proyecto nuevo y empezar a controlarlo con Git desde cero.

También puede usarse en un proyecto ya existente para empezar a versionarlo.

Ejemplo en la terminal:
git init

Este comando crea una carpeta oculta llamada ".git" dentro de la carpeta actual, donde Git guarda toda la información del repositorio.

## Detalles importantes:

Solo se ejecuta una vez por proyecto.
No sube nada a GitHub automáticamente.
Después de usarlo, es necesario agregar archivos ("git add") y hacer commits ("git commit").
Si eliminás la carpeta ".git", el proyecto deja de ser un repositorio Git.

---

## Ejemplo:

mkdir tp_metodologia_de_sistemas
cd tp_metodologia_de_sistemas
git init

Se crea un nuevo proyecto e inicializa como repositorio de git.
