# css-06 · Mini proyecto: tu página personal con estilo 💅

**Rama:** `css-06`
📚 Leer antes: [MDN — Diseño responsivo](https://developer.mozilla.org/es/docs/Learn/CSS/CSS_layout/Responsive_Design)

## Responsive: que se vea bien en el celular 📱

Primero, esta línea en el `<head>` (sin ella, el celular muestra la página "de compu" chiquita):

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Después, las **media queries**: reglas que se aplican solo si la pantalla cumple una condición.

```css
.galeria {
  display: grid;
  grid-template-columns: repeat(3, 1fr);   /* compu: 3 columnas */
}

@media (max-width: 600px) {
  .galeria {
    grid-template-columns: 1fr;            /* celular: 1 columna */
  }
}
```

🔍 Para probar: **F12** → ícono de celular/tablet (arriba a la izquierda de las herramientas) → elegí un modelo de celular.

### Variables CSS
Para no repetir colores por todos lados:

```css
:root {
  --color-principal: #6c5ce7;
  --color-texto: #2d3436;
}

h1 { color: var(--color-principal); }
```

## Consigna

1. Copiá tu página personal de **html-06** a `solucion/`.
2. Creá `solucion/estilos.css` y dale **tu estilo**:
   - Definí una paleta de 3–4 colores con variables CSS (buscá inspiración en https://coolors.co/).
   - Tipografía de Google Fonts.
   - El `<nav>` con Flexbox.
   - Alguna sección con Grid (por ejemplo, "Mis gustos" como tarjetas).
   - Tu foto redonda, con sombra.
   - El formulario de contacto prolijo (campos del mismo ancho, botón llamativo con `:hover`).
3. **Responsive**: en pantallas de menos de 600px todo debe ir en una columna y verse bien.

## ✅ Checklist
- [ ] Usaste variables CSS
- [ ] Usaste Flexbox y Grid
- [ ] Tiene al menos una media query
- [ ] La probaste en modo celular con F12 (sacale captura y ponela en el PR)
- [ ] No hay scroll horizontal en el celular

🎉 **¡Terminaste CSS!** Compará tu página con la de html-06. ¡Mirá todo lo que avanzaste!
