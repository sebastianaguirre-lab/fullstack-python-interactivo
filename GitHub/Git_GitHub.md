# Git y GitHub

## Conceptos rapidos

Git:
- Control de versiones local.

GitHub:
- Repositorio remoto.

Stage:
- Zona intermedia antes del commit.

Commit:
- Version guardada.

Branch:
- Rama de trabajo.

Pull Request:
- Solicitud para fusionar cambios.

Fork:
- Copia de un repositorio ajeno (se copia en GitHub).

---

## Flujo basico

Working Directory  
->  
`git add`  
->  
Stage  
->  
`git commit`  
->  
Repositorio local  
->  
`git push`  
->  
GitHub

---

## Comandos que usare siempre

```bash
git status (detectar cambios)
git add . (guardar cambios)
git commit -m "mensaje"
git push (y luego pull request en GitHub)
git pull (para descargar los cambios)
```

---

## Crear un repositorio local

```bash
git init
git status
git add .
git commit -m "primer commit"
```

---

## Conectar con GitHub

```bash
git remote add origin URL_DEL_REPOSITORIO
git branch -M main
git push -u origin main
```

Ver remotos:

```bash
git remote -v
```

---

## Clonar un repositorio

```bash
git clone URL_DEL_REPOSITORIO
cd nombre-del-repositorio
```

---

## Trabajar con ramas

Ver ramas:

```bash
git branch
```

Crear una rama:

```bash
git branch nombre-rama
```

Cambiar de rama:

```bash
git switch nombre-rama
```

Crear y cambiar al mismo tiempo:

```bash
git switch -c nombre-rama
```

Fusionar una rama:

```bash
git switch main
git merge nombre-rama
```

---

## Revisar cambios

```bash
git status
git diff
git log --oneline
```

---

## Deshacer cambios utiles

Sacar archivo del stage:

```bash
git restore --staged archivo
```

Descartar cambios de un archivo:

```bash
git restore archivo
```

Corregir el ultimo commit:

```bash
git commit --amend -m "nuevo mensaje"
```

---

## Comandos de emergencia

Guardar cambios temporalmente:

```bash
git stash
git stash pop
```

Traer cambios antes de trabajar:

```bash
git pull
```

Ver historial corto:

```bash
git log --oneline
```
