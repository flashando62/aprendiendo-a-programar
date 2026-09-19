# 08 · Machete de comandos 📋

Imprimilo o dejalo abierto en una pestaña.

## Terminal

| Comando | Qué hace |
|---|---|
| `pwd` | ¿Dónde estoy? |
| `ls` | ¿Qué hay acá? |
| `cd carpeta` | Entrar a una carpeta |
| `cd ..` | Subir una carpeta |
| `mkdir nombre` | Crear carpeta |
| `code .` | Abrir la carpeta actual en VS Code |
| `clear` | Limpiar la pantalla |
| **Tab** | Autocompletar |
| **Ctrl + C** | Cancelar lo que se está ejecutando |
| **↑** | Repetir el comando anterior |

## Git · Todos los días

| Comando | Qué hace |
|---|---|
| `git status` | ¿Qué cambió? ¿En qué rama estoy? **(usalo siempre)** |
| `git add .` | Preparar todos los cambios |
| `git add archivo` | Preparar un archivo |
| `git commit -m "mensaje"` | Guardar una foto con mensaje |
| `git push` | Subir commits a GitHub |
| `git pull` | Bajar commits de GitHub |
| `git log --oneline` | Ver el historial (salir con `q`) |
| `git diff` | Ver qué líneas cambiaron |

## Git · Ramas

| Comando | Qué hace |
|---|---|
| `git branch` | Ver ramas (la `*` es la actual) |
| `git switch -c nombre` | Crear rama nueva y pasarse a ella |
| `git switch nombre` | Pasarse a una rama que ya existe |
| `git push -u origin nombre` | Subir una rama nueva por primera vez |
| `git branch -d nombre` | Borrar una rama (ya juntada) |

## Git · Deshacer

| Comando | Qué hace |
|---|---|
| `git restore archivo` | Descartar cambios sin commitear ⚠️ |
| `git restore --staged archivo` | Sacar un archivo de la zona de preparación |
| `git commit --amend -m "nuevo"` | Cambiar el mensaje del último commit (antes del push) |

## Git · Una sola vez

| Comando | Qué hace |
|---|---|
| `git config --global user.name "Nombre"` | Decirle a Git tu nombre |
| `git config --global user.email "mail"` | Decirle a Git tu email |
| `git clone URL` | Descargar un repo |

---

## 🔁 El ciclo de cada ejercicio

```bash
git switch main
git pull
git switch -c EJERCICIO
# trabajar...
git add .
git commit -m "Qué hice"
git push -u origin EJERCICIO
# → Pull Request en GitHub → revisión → merge
git switch main
git pull
git branch -d EJERCICIO
```

---

📖 ¿Querés profundizar? El libro oficial de Git, gratis y en español: https://git-scm.com/book/es/v2
