# css-01 · Primeros estilos 🎨

- **Rama:** `css-01`
- 🧠 Leer antes: [CSS · Conceptos clave](../../../docs/css/conceptos-clave.md) (¡importante!)
- 📚 De apoyo: [MDN — ¿Qué es CSS?](https://developer.mozilla.org/es/docs/Learn/CSS/First_steps/What_is_CSS)

## Un poquito de teoría

CSS dice **cómo se ven** las cosas. Una regla CSS se escribe así:

```css
selector {
  propiedad: valor;
}
```

Ejemplo:

```css
h1 {
  color: purple;
  font-size: 40px;
}
```
→ *"A todos los `h1`, ponelos violeta y de 40 píxeles."*

### Conectar CSS con HTML
El CSS va en un archivo aparte (`estilos.css`) y se conecta desde el `<head>` del HTML:

```html
<head>
  <meta charset="UTF-8">
  <title>Mi página</title>
  <link rel="stylesheet" href="estilos.css">
</head>
```

### Propiedades para empezar

| Propiedad | Ejemplo | Qué hace |
|---|---|---|
| `color` | `color: #333333;` | Color del texto |
| `background-color` | `background-color: lightyellow;` | Color de fondo |
| `font-size` | `font-size: 18px;` | Tamaño de letra |
| `font-family` | `font-family: Arial, sans-serif;` | Tipografía |
| `font-weight` | `font-weight: bold;` | Grosor de letra |
| `text-align` | `text-align: center;` | Alineación del texto |

Los colores se pueden escribir por nombre (`tomato`), en hexadecimal (`#ff6347`) o en `rgb(255, 99, 71)`.
Herramienta para elegir colores: https://coolors.co/

## Consigna

1. Copiá la **receta** que hiciste en html-03 a `solucion/`.
2. Creá `solucion/estilos.css` y conectalo al HTML.
3. Dale estilo:
   - Un color de fondo suave para toda la página (`body`)
   - Una tipografía distinta para todo el texto
   - El `h1` centrado y de otro color
   - Los `h2` con otro color y otro tamaño
   - Los párrafos con un tamaño de letra cómodo para leer

## Desafío extra ⭐
Usá una tipografía de [Google Fonts](https://fonts.google.com/): elegí una, copiá el `<link>` que te da
y ponelo en el `<head>`.

## ✅ Checklist
- [ ] El CSS está en un archivo aparte, no mezclado en el HTML
- [ ] Usaste al menos 5 propiedades distintas
- [ ] El texto se lee bien (buen contraste entre texto y fondo)
