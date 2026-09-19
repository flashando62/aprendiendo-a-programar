# 06 · Ramas y Pull Requests: cómo entregar ejercicios ⭐

Esta es **la guía más importante**. Vas a repetir este proceso en cada ejercicio del curso,
y es exactamente como se trabaja en las empresas de software.

---

## ¿Qué es una rama?

Una **rama** es una copia paralela del proyecto donde podés trabajar tranquila
**sin tocar la versión oficial** (`main`).

```
main:        ●───●───●─────────────●  ← versión oficial
                      \           /
html-01:               ●───●───●     ← tu rama de trabajo
                     (tus commits)
```

Cuando terminás, pedís que tu rama se **junte** con `main`. Ese pedido se llama **Pull Request** (PR).
Tu mentor lo revisa, te comenta, y cuando está todo bien, se junta (*merge*).

---

## 🔁 El ciclo completo de un ejercicio

Vamos con un ejemplo: el ejercicio **html-01**.

### 1 · Arrancar desde `main` actualizado

```bash
git switch main
git pull
```

### 2 · Crear tu rama

```bash
git switch -c html-01
```

- `switch` = cambiarse de rama.
- `-c` = *create*, crearla nueva.
- Nombre: usá el código del ejercicio (`git-01`, `html-03`, `js-05`...). Sin espacios ni tildes.

Comprobalo:

```bash
git branch
```
```
* html-01
  main
```
El `*` marca en qué rama estás. También lo ves abajo a la izquierda en VS Code.

### 3 · Hacer el ejercicio

Leé el `README.md` del ejercicio y creá tus archivos en su carpeta `solucion/`.
Hacé commits cada vez que avances algo:

```bash
git add .
git commit -m "Creo la estructura de la página"
# ...seguís trabajando...
git add .
git commit -m "Agrego los párrafos sobre mí"
```

### 4 · Subir tu rama

```bash
git push -u origin html-01
```

### 5 · Abrir el Pull Request en GitHub

1. Entrá al repo en GitHub. Va a aparecer un cartel amarillo:
   **"html-01 had recent pushes"** → botón **Compare & pull request**.
   (Si no aparece: pestaña **Pull requests → New pull request** → en *compare* elegí tu rama.)
2. Verificá que diga **`base: main` ← `compare: html-01`**.
3. **Título:** `html-01 · Mi primera página`
4. **Descripción:** completá la plantilla que aparece (qué hiciste, qué te costó).
5. A la derecha, en **Reviewers**, elegí a tu mentor.
6. **Create pull request**. 🎉

### 6 · Esperar la revisión

Tu mentor puede:
- ✅ **Aprobar** → pasá al paso 7.
- 💬 **Pedir cambios** → no hay que abrir otro PR. Seguí en la misma rama, corregí, y:
  ```bash
  git add .
  git commit -m "Corrijo lo que me marcaron en la revisión"
  git push
  ```
  El PR se actualiza solo. ✨

> Que te pidan cambios **no es un reto**: es la parte donde más se aprende.
> Los programadores con 20 años de experiencia también reciben correcciones en sus PRs.

### 7 · Hacer merge

Cuando está aprobado, en el PR apretá **Merge pull request → Confirm merge**.
Después GitHub te ofrece **Delete branch**: apretalo (la rama ya cumplió su función).

### 8 · Volver a `main` y limpiar

```bash
git switch main
git pull                  # baja tu ejercicio ya juntado con main
git branch -d html-01     # borra la rama de tu compu
```

**¡Ejercicio entregado!** Marcalo en [PROGRESO.md](../../PROGRESO.md) y a por el siguiente. 🚀

---

## 📋 Resumen para tener a mano

```bash
git switch main
git pull
git switch -c NOMBRE-EJERCICIO

# ... trabajar, y cada tanto:
git add .
git commit -m "Qué hice"

git push -u origin NOMBRE-EJERCICIO
# → Abrir el Pull Request en GitHub
# → Esperar revisión, corregir si hace falta (add, commit, push)
# → Merge en GitHub

git switch main
git pull
git branch -d NOMBRE-EJERCICIO
```

---

## ❓ Preguntas frecuentes

**¿Puedo tener varias ramas a la vez?**
Sí. Si estás esperando la revisión de `html-01`, podés arrancar `html-02` (desde `main`).
Solo acordate de hacer commit antes de cambiarte de rama.

**¿Me cambié de rama y desaparecieron mis archivos!**
No desaparecieron: están en la otra rama. Hacé `git switch nombre-de-la-otra-rama` y vuelven. 😌

**¿Cómo sé en qué rama estoy?**
`git status` (primera línea) o abajo a la izquierda en VS Code.

---

Siguiente: [07 · ¡Socorro! Errores comunes](07-errores-comunes.md)
