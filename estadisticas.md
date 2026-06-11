# Estadísticas del repositorio

## Integrante con mayor cantidad de commits

```bash
git shortlog -sn --all
```

```
11  JuanForicher
 8  EmmanuelF90
 7  Ignacio
 4  Ignacio Ramirez Labadie
 3  Ramiro
 2  ramiro_stallone
```

El integrante con más commits es **JuanForicher** con 11 commits.

---

## Cantidad total de merges

```bash
git log --oneline --merges | wc -l
```

**15 merges** en total.

---

## Cantidad de conflictos

Se produjo **1 conflicto** durante el desarrollo. Ocurrió cuando dos integrantes subieron archivos con el mismo nombre y distinto contenido desde ramas distintas. Se resolvió con un revert (commit `accbf34`) y está documentado con capturas en [`conflictos/conflicto1.md`](conflictos/conflicto1.md).

---

## Cantidad de ramas

```bash
git branch -a
```

```
* alumno3_stallone
  dev
  main
  remotes/origin/HEAD -> origin/main
  remotes/origin/alumno1_ramirez_labadie
  remotes/origin/alumno2_franco
  remotes/origin/alumno3_stallone
  remotes/origin/alumno4_foricher_castellon
  remotes/origin/dev
  remotes/origin/main
  remotes/origin/revert-9-alumno4_foricher_castellon
```

**11 ramas** en total (3 locales, 8 remotas).

---

## Commit con mayor cantidad de archivos modificados

```bash
git log --all --format="%H" | while read hash; do
  count=$(git diff-tree --no-commit-id -r --name-only $hash | wc -l)
  echo "$count $hash"
done | sort -rn | head -5
```

El commit con más archivos modificados es el `e2452f6` con **5 archivos**.

```
commit e2452f68da8f8e628b3ca932213d2bf7232b83de
Autor:  Ignacio
Mensaje: fix: modificar nombres de archivos

 comandos/{git branch-checkout-switch.md => git_branch_checkout_switch.md} | 0
 comandos/{git config --global user.name.md => git_config.md}              | 0
 comandos/{git merge-rebase.md => git_merge_rebase.md}                     | 0
 comandos/{git status.md => git_status.md}                                 | 0
 comandos/{git--version.md => git_version.md}                              | 0
 5 files changed, 0 insertions(+), 0 deletions(-)
```

Este commit renombró los archivos de la carpeta `comandos/` para unificar la convención de nombres.

---

## Captura del conflicto previo a su resolución

El conflicto ocurrió en el archivo `git_rm--cached_file.md`. El revert asociado tiene el hash `accbf34`.

```
commit accbf349c8bbcb286f7ddda082f231cd166675db
Autor:  ramiro_stallone
Mensaje: Revert "docs: agrego archivo que explica git rm --cached <file>"

 comandos/git_rm --cached_file.md | 22 ----------------------
 1 file changed, 22 deletions(-)
```

La captura del estado previo a la resolución está en [`conflictos/conflicto1.png`](conflictos/conflicto1.png).