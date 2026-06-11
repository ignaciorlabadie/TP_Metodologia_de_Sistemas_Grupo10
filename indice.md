# Indice

## Introducción

El objetivo de este trabajo es documentar los principales comandos de Git trabajados en clase, explicados con palabras propias.

---

## Comandos de Git

A continuación se presentan los comandos documentados:

- [brew install git / winget install --id Git.Git -e --source winget / sudo apt install git / sudo dnf install git / sudo pacman -S git / git --version](comandos/instalacion_git.md) - Instala Git según SO, muestra la versión de Git instalada en el sistema.
- [git init](comandos/git_init.md) - inicializa un repositorio Git en una carpeta.
- [git add](comandos/git_add.md) - agrega archivos al área de preparación (staging area)
- [git commit / git commit -am](comandos/git_commit_git_commit-am.md) - guarda los cambios preparados en el historial del repositorio
- [git status](comandos/git_status.md) - muestra el estado actual del repositorio
- [git merge / rebase](comandos/git_merge_rebase.md) - combina cambios de distintas ramas
- [git config](comandos/git_config.md) - configura los datos del autor (nombre y email)
- [git branch/checkout/switch](comandos/git_branch_checkout_switch.md) - gestiona y navega entre ramas
- [git log / git reflog](comandos/git_log.md) - muestra el historial de commits del repositorio
- [git rm --cached](comandos/git_rm--cached_file.md) - elimina un archivo del staging area sin borrarlo localmente
- [git remote](comandos/git_remote.md) - lista, agrega o modifica repositorios remotos asociados al proyecto (ej, origin en GitHub)
- [git reset / git revert / git clean](comandos/git_reset.md) - deshace commits o cambios: reset,  mueve HEAD a un commit anterior, revert, crea un commit inverso para deshacer cambios sin alterar el historial, y clean, elimina archivos no rastreados del directorio de trabajo

---

## Conflictos

- [Conflicto 1](conflictos/conflicto1.md)

---

## Estadísticas del repositorio

- [Ver estadísticas](estadisticas.md)

---

## Uso de Inteligencia Artificial

- [IA.md](IA.md)

---

## Notas

- Todas las modificaciones fueron realizadas utilizando ramas independientes.
- Se aplicaron convenciones de commits (Conventional Commits).
- Se utilizaron Pull Requests para la integración de cambios.