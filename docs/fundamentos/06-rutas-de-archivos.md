# 06 · Rutas de archivos: el GPS de tu código 🧭

> 📌 Leela antes del ejercicio **html-03** (imágenes y enlaces). Es la causa #1 de
> *"¡mi imagen no aparece!"* y *"¡no se aplica mi CSS!"*.

Cada vez que un archivo usa otro (un HTML que muestra una imagen, que carga un CSS o que enlaza
a otra página) tenés que escribir **la ruta** hacia ese archivo:

```html
<img src="RUTA">
<link rel="stylesheet" href="RUTA">
<a href="RUTA">
<script src="RUTA"></script>
```

---

## Dos tipos de rutas

### 1 · Absolutas: la dirección completa

```html
<img src="https://picsum.photos/300">
```

Empiezan con `https://`. Sirven para cosas que están **en internet**.

> ⚠️ **Nunca** uses rutas como `C:/Users/maria/Desktop/foto.jpg`. En tu compu anda,
> pero cuando lo subas a GitHub **se rompe**: la compu de otra persona (o el servidor) no tiene tu disco C.

### 2 · Relativas: "desde donde estoy"

Se escriben **partiendo de la carpeta donde está el archivo que estás editando**.
Como cuando le explicás a alguien cómo llegar *"desde acá"*.

---

## Las tres reglas de las rutas relativas

Imaginá este proyecto:

```
📁 mi-sitio
├── 📄 index.html
├── 📄 contacto.html
├── 📁 css
│   └── 📄 estilos.css
├── 📁 img
│   └── 📄 logo.png
└── 📁 blog
    └── 📄 post.html
```

### Regla 1 · Mismo lugar → solo el nombre
Desde `index.html`, para ir a `contacto.html` (están en la misma carpeta):
```html
<a href="contacto.html">Contacto</a>
```

### Regla 2 · Entrar a una carpeta → `carpeta/archivo`
Desde `index.html`, para usar el logo (está **dentro** de `img`):
```html
<img src="img/logo.png" alt="Logo">
<link rel="stylesheet" href="css/estilos.css">
```

### Regla 3 · Salir de una carpeta → `../`
`..` significa **"la carpeta de arriba"** (la madre). Desde `blog/post.html`, para usar el logo:
```html
<img src="../img/logo.png" alt="Logo">
```
Se lee: *"salí de `blog`, entrá a `img`, agarrá `logo.png`"*.

Podés subir varias veces: `../../` = subir dos carpetas.

> 💡 Es lo mismo que en la terminal: `cd ..` sube una carpeta. ¡Las rutas funcionan igual en todos lados!

### ⚠️ Ojo con el CSS
Las rutas **dentro de un `.css`** se cuentan **desde la carpeta del CSS**, no desde el HTML:

```css
/* en css/estilos.css */
body {
  background-image: url("../img/fondo.jpg");   /* salgo de css/, entro a img/ */
}
```

---

## 🪤 La trampa de las mayúsculas

Windows **no distingue** mayúsculas: `Logo.PNG` y `logo.png` le dan igual.
Los servidores de internet (como GitHub Pages) **sí distinguen**.

```html
<img src="img/logo.png">   <!-- pero el archivo se llama Logo.PNG -->
```
→ En tu compu **funciona**. Publicado **se rompe**. 😱

**Solución:** nombres **siempre en minúscula**, sin espacios ni tildes (ver [guía 01](01-archivos-y-carpetas.md)).

---

## 🔍 Checklist: "mi imagen / mi CSS no carga"

1. ¿El nombre está escrito **exactamente** igual? (mayúsculas, extensión `.jpg` vs `.jpeg` vs `.png`)
2. ¿Contaste la ruta **desde el archivo que la usa**?
3. ¿Necesitás `../` porque el archivo está en otra carpeta?
4. ¿Usaste `/` y no `\`?
5. Abrí **F12 → Consola**: vas a ver un error rojo `404 (Not Found)` con la ruta que buscó el navegador.
   Comparala con la ruta real del archivo.

> 💡 En VS Code, cuando escribís `src="` te va **sugiriendo** las carpetas y archivos que existen.
> Usá esas sugerencias y te ahorrás errores.

---

## 🧪 Práctica

Con la estructura de `mi-sitio` de arriba, escribí la ruta:

1. Desde `contacto.html` → a `css/estilos.css`
2. Desde `blog/post.html` → a `index.html`
3. Desde `blog/post.html` → a `css/estilos.css`
4. Desde `css/estilos.css` → a `img/logo.png`

<details>
<summary>👀 Ver respuestas (¡intentalo primero!)</summary>

1. `css/estilos.css`
2. `../index.html`
3. `../css/estilos.css`
4. `../img/logo.png`

</details>

---

Siguiente: [07 · Markdown](07-markdown.md)
