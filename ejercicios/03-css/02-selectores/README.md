# css-02 · Selectores 🎯

- **Rama:** `css-02`
- 📚 Leer antes: [MDN — Selectores CSS](https://developer.mozilla.org/es/docs/Learn/CSS/Building_blocks/Selectors)

## Los tres selectores básicos

```html
<p>Párrafo normal</p>
<p class="destacado">Párrafo destacado</p>
<p id="aviso">Párrafo de aviso</p>
```

```css
p            { color: black; }   /* por etiqueta: TODOS los <p>                     */
.destacado   { color: blue;  }   /* por clase (con punto): los que tengan esa clase */
#aviso       { color: red;   }   /* por id (con #): el único con ese id              */
```

- Una **clase** se puede usar en muchos elementos. Un **id** es único por página.
- Un elemento puede tener varias clases: `class="destacado grande"`.
- **Consejo:** para estilos, preferí siempre **clases**.

### Otros selectores útiles

```css
nav a        { }   /* los <a> que están DENTRO de un <nav> */
h1, h2, h3   { }   /* varios a la vez                      */
a:hover      { }   /* cuando pasás el mouse por encima     */
```

## Consigna

Creá `solucion/index.html` y `solucion/estilos.css` con una **lista de tus 6 series o películas favoritas**:

1. Cada una en un `<article>` con título (`<h2>`) y una breve descripción.
2. Creá la clase `.favorita` y aplicala a tus 2 preferidas: que se distingan (otro fondo, un borde, lo que quieras).
3. Creá la clase `.vista` y `.pendiente` para marcar si ya la viste o no (distinto color de texto).
4. Poné un `<nav>` arriba con 3 enlaces y hacé que **cambien de color cuando pasás el mouse** (`:hover`).
5. Usá un `id` para el título principal.

## Para pensar 🤔
Si un elemento tiene la clase `.favorita` (fondo amarillo) y además la etiqueta `article` tiene fondo blanco,
¿cuál gana? ¿Por qué? Investigá **especificidad** en MDN y contalo en el PR.

## ✅ Checklist
- [ ] Usaste selectores de etiqueta, clase e id
- [ ] Hay al menos un elemento con **dos** clases
- [ ] Los enlaces cambian con `:hover`
