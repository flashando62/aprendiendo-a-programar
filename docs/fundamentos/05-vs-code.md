# 05 · Visual Studio Code: tu taller 🛠️

> Antes de leer esto tenés que haberlo instalado: [Git · 00 · Preparar la compu](../git/00-preparar-la-compu.md).

**Visual Studio Code** (VS Code) es el **editor de código** que vas a usar. Es gratis y es el más usado del mundo.

---

## Regla #1: abrí **carpetas**, no archivos sueltos

Siempre trabajá abriendo la **carpeta del proyecto** entera:

- Menú **Archivo → Abrir carpeta…** → elegí `aprendiendo-a-programar`
- O desde la terminal, parada en esa carpeta: `code .`

Si abrís un archivo suelto (doble clic en un `.html`), VS Code no "ve" el resto del proyecto
y Live Server, Git y el autocompletado no funcionan bien.

---

## Las partes de la pantalla

```
┌────┬─────────────────┬──────────────────────────────────────────┐
│ 📄 │ EXPLORADOR      │  index.html ×   estilos.css ×            │  ← pestañas
│ 🔍 │ ▾ ejercicios    │ ─────────────────────────────────────────│
│ 🌿 │   ▾ 02-html     │  1  <!DOCTYPE html>                      │
│ 🧩 │     ▸ 01-...    │  2  <html lang="es">                     │  ← editor
│    │                 │  3    <head>                             │
│    │                 │ ─────────────────────────────────────────│
│    │                 │ TERMINAL                                 │  ← terminal
│    │                 │ $ git status                             │
├────┴─────────────────┴──────────────────────────────────────────┤
│ 🌿 main   ⓧ 0 ⚠ 0                              Ln 3, Col 5  HTML│  ← barra de estado
└─────────────────────────────────────────────────────────────────┘
```

| Parte | Para qué |
|---|---|
| 📄 **Explorador** | Ver, crear, renombrar y borrar archivos y carpetas |
| 🔍 **Buscar** | Buscar un texto en todos los archivos |
| 🌿 **Control de código fuente** | Git con botones |
| 🧩 **Extensiones** | Instalar agregados (como Live Server) |
| **Editor** | Donde escribís. Cada archivo abierto es una pestaña |
| **Terminal** | Una terminal adentro de VS Code: `` Ctrl + ` `` |
| **Barra de estado** | Abajo: en qué **rama** de Git estás, errores, línea y columna |

### Crear archivos y carpetas
En el Explorador, pasá el mouse sobre el nombre del proyecto y aparecen íconos para
**nuevo archivo** 📄+ y **nueva carpeta** 📁+. Escribí el nombre **con la extensión** (`index.html`).

---

## El punto blanco: ¿guardé o no guardé?

Si en la pestaña de un archivo aparece un **●** en vez de la **×**, ese archivo tiene **cambios sin guardar**.
El navegador y Git **no ven** los cambios hasta que guardes (`Ctrl + S`).

> 💡 **Recomendado:** activá **Archivo → Guardado automático**. VS Code guarda solo mientras escribís.

---

## Atajos que te van a salvar la vida

| Atajo | Qué hace |
|---|---|
| `Ctrl + S` | Guardar |
| `Ctrl + Z` | Deshacer |
| `Ctrl + P` | Abrir un archivo escribiendo su nombre |
| `` Ctrl + ` `` | Abrir / cerrar la terminal |
| `Shift + Alt + F` | **Formatear**: acomoda la indentación de todo el archivo solo ✨ |
| `Alt + ↑` / `Alt + ↓` | Mover la línea para arriba / abajo |
| `Shift + Alt + ↓` | Duplicar la línea |
| `Ctrl + D` | Seleccionar la siguiente aparición de la palabra (para editar varias a la vez) |
| `Ctrl + Shift + P` | La "paleta de comandos": buscá cualquier acción por nombre |

**Comentar/descomentar una línea:** el atajo cambia según el teclado.
Fijate cuál es el tuyo en **Editar → Alternar comentario de línea** (en teclados en español suele ser `Ctrl + }`).

---

## Ayudas que te da VS Code

- **Colores** (*resaltado de sintaxis*): cada parte del código tiene un color. Si de golpe
  todo queda de un color raro, probablemente te falta cerrar una comilla o una etiqueta.
- **Autocompletado:** mientras escribís, te sugiere cosas. Aceptás con `Tab` o `Enter`.
- **Emmet** (en HTML): escribí `!` + `Tab` y aparece el esqueleto de una página.
  Escribí `ul>li*3` + `Tab` y aparece una lista con 3 ítems. (Usalo cuando ya entiendas lo que genera.)
- **Garabatos rojos** (subrayado ondulado): hay un error en esa línea. Pasá el mouse para leerlo.
- **Pares de llaves:** si ponés el cursor junto a una `{`, se ilumina su `}` correspondiente.

---

## Indentación: el código prolijo se entiende

**Indentar** es correr hacia la derecha lo que está **adentro** de otra cosa. Se hace con `Tab`.

```html
<!-- ❌ Sin indentar: ¿qué está adentro de qué? -->
<ul>
<li>Uno</li>
<li>Dos</li>
</ul>

<!-- ✅ Indentado: se ve la estructura -->
<ul>
  <li>Uno</li>
  <li>Dos</li>
</ul>
```

Al navegador le da igual. **A vos y a quien revise tu código, no.** Si te desordenás, `Shift + Alt + F`.

---

## 🧪 Práctica

1. Abrí la carpeta del curso con **Archivo → Abrir carpeta**.
2. Activá el **Guardado automático**.
3. Creá una carpeta `pruebas` y adentro un archivo `hola.html`.
4. Escribí `!` y `Tab`. Dentro del `<body>` escribí `<h1>Hola</h1>`.
5. Clic derecho en el archivo → **Open with Live Server**. Cambiá el texto y mirá cómo el navegador se actualiza solo.
6. Borrá la carpeta `pruebas` (clic derecho → Eliminar).

---

Siguiente: [Git · 01 · La terminal sin miedo](../git/01-la-terminal.md)
