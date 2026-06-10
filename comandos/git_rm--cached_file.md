## git rm

## ¿Qué hace git rm?

El comando "git rm" se utiliza para **eliminar archivos del repositorio Git**.
Al usarlo, el archivo se elimina tanto del:

- Directorio de trabajo
- Área de staging (index)

y queda preparado para el próximo commit.

---

## Uso básico

En la terminal:
git rm archivo.txt
git commit -m "Elimino archivo.txt"

---

## Casos de uso

### 1. Eliminar un archivo normalmente

En la terminal:
git rm archivo.txt

Esto elimina el archivo y registra el cambio automáticamente.

---

### 2. Eliminar archivo solo del repositorio (mantenerlo local)

En la terminal:
git rm --cached archivo.txt

Resultado:

- El archivo permanece en tu computadora
- Git deja de rastrearlo

Uso típico con `.gitignore`:

En la terminal:
git rm --cached .env

---

### 3. Eliminar múltiples archivos

En la terminal:
git rm \*.log

---

### 4. Eliminar un directorio completo

En la terminal:
git rm -r carpeta/

---

### 5. Forzar eliminación

Si el archivo tiene cambios sin confirmar:

En la terminal:
git rm -f archivo.txt

---

## Diferencias importantes

| Comando              | Acción                                                    |
| -------------------- | --------------------------------------------------------- |
| "rm archivo.txt"     | Borra el archivo, pero Git no lo registra automáticamente |
| "git rm archivo.txt" | Borra el archivo y registra el cambio en Git              |

---

## Flujo típico

En la terminal:
git rm archivo.txt
git commit -m "Elimino archivo innecesario"
git push

---

## Cuándo usar "git rm"

- Eliminar archivos del repositorio
- Limpiar archivos innecesarios
- Dejar de trackear archivos ("--cached")
