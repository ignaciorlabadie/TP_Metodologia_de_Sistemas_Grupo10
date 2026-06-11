# Instalación de Git

## Para macOS:
Se puede instalar Git usando **Homebrew**:
```bash
brew install git
```

---

# Para Windows:
Se puede instalar usando **Winget**:
```bash 
winget install --id Git.Git -e --source winget
```


---

# Para Linux 
1. Para Ubuntu / Debian
```bash 
sudo apt update
sudo apt install git
```

2. Para Fedora
```bash 
sudo dnf install git
```

3. Para Arch Linux
```bash
sudo pacman -S git
```

---

# Datos importantes: 
- También se puede instalar desde la página oficial, tanto para Windows, macOS y Linux
    - https://git-scm.com/download/win

---

# git --version  

## ¿Qué hace?  
El comando "git --version" se usa para mostrar la versión de Git instalada en el sistema.  

---

## ¿Para qué se usa?  
Sirve para confirmar que Git está correctamente instalado y saber qué versión exacta se posee.   

---

## Ejemplos  
En la terminal:  
```bash
git --version
```

salida: 
```bash
git version 2.44.0
```
## Detalles importantes
- Si el comando no funciona, Git no está instalado o no está en el PATH.
- Solo verifica, no modifica nada en el repositorio.