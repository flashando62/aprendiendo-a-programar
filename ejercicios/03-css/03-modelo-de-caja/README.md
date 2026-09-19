# css-03 · El modelo de caja 📦

- **Rama:** `css-03`
- 📚 Leer antes: [MDN — El modelo de caja](https://developer.mozilla.org/es/docs/Learn/CSS/Building_blocks/The_box_model)

## Todo es una caja

En CSS, **cada elemento es una caja rectangular** con 4 capas:

```
┌──────────────── margin (espacio AFUERA, separa de otras cajas) ───────┐
│  ┌───────────── border (el borde) ───────────────────────────────┐    │
│  │  ┌────────── padding (espacio ADENTRO, entre borde y texto) ─┐ │    │
│  │  │                                                           │ │    │
│  │  │                 content (el contenido)                    │ │    │
│  │  │                                                           │ │    │
│  │  └───────────────────────────────────────────────────────────┘ │    │
│  └────────────────────────────────────────────────────────────────┘    │
└────────────────────────────────────────────────────────────────────────┘
```

```css
.tarjeta {
  width: 300px;
  padding: 20px;              /* los 4 lados */
  border: 2px solid gray;     /* grosor, estilo, color */
  border-radius: 10px;        /* esquinas redondeadas */
  margin: 16px auto;          /* 16px arriba y abajo, centrado a los costados */
}
```

> 💡 Poné esto al principio de todos tus CSS. Hace que el `width` incluya el padding y el borde
> (mucho más fácil de calcular):
> ```css
> * { box-sizing: border-box; }
> ```

### 🔍 Herramientas de desarrollo
En el navegador apretá **F12** → pestaña *Elementos*. Pasá el mouse por el código y vas a ver
las cajas pintadas: azul = contenido, verde = padding, naranja = margin. **Usalo siempre.**

## Consigna

Creá una **tarjeta de presentación** (como las de papel) en `solucion/`:

1. Una caja de 350px de ancho, centrada en la página.
2. Adentro: tu foto (redonda, pista: `border-radius: 50%`), tu nombre, lo que estudiás y 3 datos.
3. Con `padding` para que el texto no toque el borde.
4. Con borde de color y esquinas redondeadas.
5. Con una sombra (investigá `box-shadow`).
6. Separación entre los elementos internos usando `margin`.

## ✅ Checklist
- [ ] Usaste `margin`, `padding` y `border`
- [ ] Sabés explicar la diferencia entre `margin` y `padding` (¡escribilo en el PR!)
- [ ] Abriste las herramientas de desarrollo (F12) e inspeccionaste tu tarjeta
