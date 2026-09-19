# 05 · Subir y bajar cambios (push y pull)

Hasta ahora tus commits están **solo en tu compu**. GitHub no se enteró de nada.

```
   Tu compu                          GitHub
 ┌──────────┐     git push ──►     ┌──────────┐
 │  commits │                      │  commits │
 └──────────┘     ◄── git pull     └──────────┘
```

- **`git push`** → subís tus commits a GitHub.
- **`git pull`** → bajás los commits nuevos que hay en GitHub.

---

## `git push` — subir

Seguimos en la rama `practica` de la guía anterior. Como es la **primera vez** que subís
esa rama, hay que decirle a Git a dónde subirla:

```bash
git push -u origin practica
```

- `origin` = el nombre corto del repo en GitHub.
- `-u` = "acordate de esto" (las próximas veces alcanza con `git push` a secas).

```
To https://github.com/usuario/aprendiendo-a-programar.git
 * [new branch]      practica -> practica
```

Entrá a GitHub, tocá el selector de ramas (dice `main`, arriba a la izquierda) y elegí `practica`:
¡tus commits están ahí! 🚀

> ⚠️ En este curso **nunca vas a hacer push directo a `main`**: siempre trabajás en una rama
> y pedís que se junte con un Pull Request (próxima guía). Puede que GitHub ni siquiera te deje
> subir a `main`, y está bien: es a propósito.

### Borrar la rama de práctica

Ya cumplió su función. Borrala de GitHub y de tu compu:

```bash
git push origin --delete practica
git switch main
git branch -D practica
```

(`-D` en mayúscula fuerza el borrado de una rama que nunca se juntó con `main`.)

---

## `git pull` — bajar

Cuando tu mentor agrega material nuevo, o cuando se aprueba un Pull Request tuyo,
GitHub tiene cosas que tu compu no. Para traerlas:

```bash
git pull
```

```
Updating a1b2c3d..9e8f7d6
Fast-forward
 ejercicios/03-css/01-primeros-estilos/README.md | 40 +++++++++
```

> 💡 **Hábito de oro:** antes de empezar a trabajar cada día, `git switch main` y `git pull`.
> Así siempre arrancás desde la última versión.

---

## `git status` te avisa si estás atrasada o adelantada

```
Your branch is ahead of 'origin/main' by 2 commits.
```
→ Tenés 2 commits que GitHub no tiene. Hacé `git push`.

```
Your branch is behind 'origin/main' by 3 commits.
```
→ GitHub tiene 3 commits que vos no. Hacé `git pull`.

(Para que Git sepa que estás atrasada primero tiene que consultar a GitHub: `git fetch` hace eso sin bajar nada.)

---

Siguiente: [06 · Ramas y Pull Requests](06-ramas-y-pull-requests.md) ⭐ (la más importante del curso)
