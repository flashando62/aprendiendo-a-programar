# css-05 · Grid ▦

**Rama:** `css-05`
📚 Leer antes: [MDN — Grids](https://developer.mozilla.org/es/docs/Learn/CSS/CSS_layout/Grids)
🎮 Jugar antes: [Grid Garden](https://cssgridgarden.com/#es)

## Flexbox vs Grid

- **Flexbox** → una dimensión: una fila **o** una columna.
- **Grid** → dos dimensiones: filas **y** columnas a la vez, como una grilla.

```css
.contenedor {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;   /* 3 columnas iguales (fr = "fracción") */
  gap: 20px;
}

.destacado {
  grid-column: span 2;   /* ocupa 2 columnas */
}
```

Truco útil: `grid-template-columns: repeat(3, 1fr);` es lo mismo que `1fr 1fr 1fr`.

### Diseño de página con áreas con nombre

```css
.pagina {
  display: grid;
  grid-template-columns: 200px 1fr;
  grid-template-areas:
    "cabecera cabecera"
    "lateral  contenido"
    "pie      pie";
}
header { grid-area: cabecera; }
aside  { grid-area: lateral; }
main   { grid-area: contenido; }
footer { grid-area: pie; }
```

## Consigna

1. **Galería de fotos** (`solucion/galeria.html`): 9 imágenes en una grilla de 3 columnas.
   La primera imagen ocupa 2 columnas y 2 filas.
   (Podés usar imágenes de ejemplo de https://picsum.photos/ — ej. `https://picsum.photos/400/300?random=1`.)
2. **Diseño de página** (`solucion/index.html`): usando `grid-template-areas`, armá una página con
   cabecera, menú lateral, contenido principal y pie. Pintá cada área de un color distinto para verlas bien.

## ✅ Checklist
- [ ] Terminaste Grid Garden
- [ ] Usaste `fr`, `gap` y `grid-template-areas`
- [ ] Podés explicar cuándo usarías Flexbox y cuándo Grid (escribilo en el PR)
