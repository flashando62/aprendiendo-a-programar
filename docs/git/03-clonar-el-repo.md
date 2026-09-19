# 03 · Descargar este repo a tu compu (clonar)

**Clonar** es descargar un repositorio de GitHub a tu compu, **con toda su historia**.
Se hace **una sola vez**. Después, para traer novedades, se usa `git pull`.

> ✋ Antes de seguir, asegurate de haber **aceptado la invitación** al repo que te mandó tu mentor.

---

## Paso 1 · Copiar la dirección del repo

1. Entrá al repo en GitHub.
2. Apretá el botón verde **`<> Code`**.
3. Asegurate de que esté elegida la pestaña **HTTPS**.
4. Copiá la dirección. Es algo así: `https://github.com/flashando62/aprendiendo-a-programar.git`

## Paso 2 · Ir a tu carpeta de programación

Abrí Git Bash:

```bash
cd ~/programacion
```

(Si no existe, creala primero con `mkdir ~/programacion`.)

## Paso 3 · Clonar

Escribí `git clone ` (con un espacio al final) y pegá la dirección.
En Git Bash se pega con **clic derecho → Paste** o `Shift + Insert`.

```bash
git clone https://github.com/flashando62/aprendiendo-a-programar.git
```

La primera vez, **se va a abrir una ventana para iniciar sesión en GitHub**.
Elegí *Sign in with your browser* y autorizá. Esto se hace una sola vez: después Git se acuerda.

Vas a ver algo así:

```
Cloning into 'aprendiendo-a-programar'...
remote: Enumerating objects: 45, done.
Receiving objects: 100% (45/45), done.
```

## Paso 4 · Entrar y abrir en VS Code

```bash
cd aprendiendo-a-programar
ls
code .
```

¡Deberías ver los mismos archivos que en GitHub! 🎉

## Paso 5 · Comprobar que Git está funcionando

```bash
git status
```

```
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

Traducción: *"Estás en la rama main, al día con GitHub, y no cambiaste nada."* Perfecto.

---

## 💡 VS Code también sabe Git

En la barra izquierda de VS Code hay un ícono con forma de ramita (🌿 *Control de código fuente*,
`Ctrl + Shift + G`). Ahí se ve lo mismo que con `git status`, pero con botones.

**Te recomiendo aprender primero con la terminal**, porque así entendés qué pasa realmente.
Cuando ya te sientas cómoda, usá lo que te resulte más práctico.

---

Siguiente: [04 · Guardar cambios (commit)](04-guardar-cambios.md)
