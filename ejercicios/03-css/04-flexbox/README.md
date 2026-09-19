# css-04 · Flexbox ↔️

**Rama:** `css-04`
📚 Leer antes: [MDN — Flexbox](https://developer.mozilla.org/es/docs/Learn/CSS/CSS_layout/Flexbox)
🎮 Jugar antes: [Flexbox Froggy](https://flexboxfroggy.com/#es) (¡terminá los 24 niveles!)

## Un poquito de teoría

Flexbox sirve para **acomodar elementos en una fila o en una columna**.
Se aplica al **contenedor** (el padre), y afecta a sus hijos:

```html
<div class="contenedor">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>
```

```css
.contenedor {
  display: flex;
  flex-direction: row;            /* row (fila) o column (columna) */
  justify-content: space-between; /* cómo se reparten en la dirección principal */
  align-items: center;            /* cómo se alinean en la otra dirección */
  gap: 16px;                      /* espacio entre los hijos */
  flex-wrap: wrap;                /* si no entran, pasan a la línea de abajo */
}
```

Valores de `justify-content`: `flex-start`, `center`, `flex-end`, `space-between`, `space-around`.

## Consigna

Creá `solucion/index.html` y `solucion/estilos.css`:

1. **Una barra de navegación**: el logo (o tu nombre) a la izquierda y 4 enlaces a la derecha, todo alineado verticalmente.
2. **Una galería de 6 tarjetas** (pueden ser tus series de css-02, o lo que quieras) que se acomoden en fila
   y, cuando la ventana se achica, pasen abajo (`flex-wrap`).
3. **Un footer** con 3 columnas de igual ancho (pista: `flex: 1` en cada hijo).
4. **Centrá** un elemento vertical y horizontalmente en una caja de 300px de alto
   (¡lo más buscado en internet por programadores! 😄).

## ✅ Checklist
- [ ] Terminaste Flexbox Froggy (sacale una captura al final y ponela en el PR)
- [ ] La galería se reacomoda al achicar la ventana
- [ ] Lograste centrar algo en ambos ejes
