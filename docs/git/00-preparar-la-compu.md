# 00 · Preparar la compu

Antes de programar necesitamos 3 cosas:

| Herramienta | ¿Qué es? | Analogía |
|---|---|---|
| **Git** | Un programa que guarda el historial de tus archivos | Una máquina de sacar fotos de tu trabajo |
| **GitHub** | Una página web donde se guardan esos historiales en internet | Un álbum de fotos en la nube |
| **Visual Studio Code** | El editor donde vas a escribir código | Un Word, pero para programar |

---

## Paso 1 · Instalar Git

### En Windows
1. Entrá a https://git-scm.com/downloads y descargá la versión para Windows.
2. Ejecutá el instalador. **Aceptá todas las opciones que vienen por defecto** (Next, Next, Next...).
   - Hay una sola pantalla que conviene mirar: *"Choosing the default editor used by Git"*.
     Elegí **"Use Visual Studio Code as Git's default editor"** (si todavía no instalaste VS Code,
     no pasa nada, dejalo como está).
3. Al terminar vas a tener un programa nuevo llamado **Git Bash**. Esa es tu terminal.

### En Mac
Abrí la app **Terminal** y escribí `git --version`. Si no lo tenés, el Mac te ofrece instalarlo solo.

### ✅ Comprobar
Abrí **Git Bash** (en Windows) o **Terminal** (en Mac) y escribí:

```bash
git --version
```

Tiene que aparecer algo como `git version 2.xx.x`. ¡Listo!

---

## Paso 2 · Instalar Visual Studio Code

1. Entrá a https://code.visualstudio.com/ y descargalo.
2. Instalalo. En Windows, marcá estas casillas cuando aparezcan:
   - ✅ *Agregar la acción "Abrir con Code" al menú contextual de archivos*
   - ✅ *Agregar la acción "Abrir con Code" al menú contextual de directorios*
   - ✅ *Agregar a PATH*
3. Abrilo. Si está en inglés: `Ctrl + Shift + X` → buscá **Spanish Language Pack** → *Install*.
4. Instalá también la extensión **Live Server** (la vamos a usar para ver páginas web).

---

## Paso 3 · Crear tu cuenta de GitHub

1. Entrá a https://github.com/ → **Sign up**.
2. Elegí un **nombre de usuario** pensando que es tu identidad profesional
   (ej. `mariagomez`, `maria-dev`). Evitá nombres como `xXmariXx2007`. 😉
3. Confirmá tu email.
4. Pasale tu nombre de usuario a tu mentor para que te dé acceso al repo del curso.
5. Te va a llegar una invitación por mail: **aceptala**.

---

## Paso 4 · Presentarte ante Git

Git necesita saber quién sos para firmar cada cambio que guardes. Abrí Git Bash y escribí
(cambiando por tus datos, **con las comillas**):

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "el-mismo-email-de-github@ejemplo.com"
git config --global init.defaultBranch main
```

> 💡 Usá el **mismo email** que usaste en GitHub, así GitHub reconoce que los cambios son tuyos.

### ✅ Comprobar

```bash
git config --global --list
```

Tienen que aparecer tu nombre y tu email.

---

## 🎉 ¡Listo!

Ya tenés todo instalado. Siguiente paso: [01 · La terminal sin miedo](01-la-terminal.md)
