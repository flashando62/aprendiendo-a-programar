# 07 · ¡Socorro! Errores comunes 🆘

Respirá. Con Git **casi nada se pierde para siempre** si ya hiciste commit.
Acá están los problemas más comunes y cómo salir.

> 🛟 **Regla número 1:** si no sabés qué pasa, escribí `git status`. Casi siempre te dice qué hacer.

---

## "Se me abrió una pantalla rara y no puedo salir"

Hiciste `git commit` **sin** `-m` y se abrió un editor.

- **Si es VS Code:** escribí el mensaje en la primera línea, guardá (`Ctrl + S`) y cerrá la pestaña.
- **Si es Vim** (pantalla negra con `~` a la izquierda): apretá `Esc`, escribí `:wq` y `Enter`.
  (Para salir sin guardar: `Esc`, `:q!` y `Enter`.)
- **Si dice `:` abajo** (por ejemplo tras `git log`): apretá `q`.

---

## "Escribí mal el mensaje del último commit"

Si **todavía no hiciste push**:

```bash
git commit --amend -m "El mensaje correcto"
```

---

## "Me olvidé de agregar un archivo al último commit"

Si **todavía no hiciste push**:

```bash
git add archivo-olvidado.html
git commit --amend --no-edit
```

---

## "Trabajé en `main` en vez de crear una rama"

Si **todavía no hiciste commit**: creá la rama ahora, tus cambios viajan con vos.

```bash
git switch -c html-01
```

Si **ya hiciste commit** (pero no push):

```bash
git switch -c html-01        # la rama nueva se lleva tus commits
git switch main
git reset --hard origin/main # main vuelve a como está en GitHub
git switch html-01           # y seguís trabajando acá
```

> ⚠️ `reset --hard` borra cambios sin commitear. Usalo solo siguiendo estos pasos exactos
> y con `git status` limpio. Si tenés dudas, **preguntá antes**.

---

## "Quiero descartar los cambios de un archivo y dejarlo como estaba"

```bash
git restore archivo.html
```

⚠️ Esto borra los cambios que no commiteaste en ese archivo. No se puede deshacer.

## "Hice `git add` de algo que no quería"

```bash
git restore --staged archivo.html
```

(El archivo no se borra; solo sale de la zona de preparación.)

---

## `error: failed to push some refs` / `Updates were rejected`

GitHub tiene commits que vos no tenés. Primero bajalos:

```bash
git pull
git push
```

## `Your local changes would be overwritten by checkout`

Querés cambiarte de rama pero tenés cambios sin guardar. Hacé commit primero:

```bash
git add .
git commit -m "Avance del ejercicio"
git switch otra-rama
```

## `fatal: not a git repository`

Estás en una carpeta que no es el repo. Hacé `pwd` para ver dónde estás y `cd` hasta la carpeta del curso.

## `Permission denied` / `403` al hacer push

- ¿Aceptaste la invitación al repo? Mirá https://github.com/notifications
- ¿Estás intentando hacer push a `main`? Tiene que ser a tu rama (ver [guía 06](06-ramas-y-pull-requests.md)).

---

## 💥 Conflictos (`CONFLICT (content): Merge conflict in ...`)

Pasa cuando **dos personas cambiaron la misma línea** y Git no sabe con cuál quedarse.
Git marca el archivo así:

```
<<<<<<< HEAD
<h1>Hola, soy María</h1>
=======
<h1>Bienvenidos a mi página</h1>
>>>>>>> main
```

- Arriba de `=======`: tu versión.
- Abajo: la otra versión.

**Cómo resolverlo:**
1. Abrí el archivo en VS Code. Te muestra botones: *Aceptar cambio actual / entrante / ambos*.
2. Dejá el archivo como querés que quede y **borrá las marcas** `<<<<<<<`, `=======`, `>>>>>>>`.
3. Guardá y:
   ```bash
   git add .
   git commit -m "Resuelvo conflicto"
   ```

La primera vez asusta. Es normal. Pedí ayuda y hacelo acompañada. 🤝

---

## 🚫 Cosas que NO hay que hacer (por ahora)

- `git push --force` → puede borrar trabajo de GitHub.
- Borrar la carpeta oculta `.git` → borrás todo el historial.
- Copiar y pegar comandos que encontraste en internet sin entender qué hacen.

Ante la duda: **preguntá**. 🙋‍♀️

---

Siguiente: [08 · Machete de comandos](08-machete.md)
