# 🎨 CSS · Conceptos clave

> 📌 Leé esto **antes** del ejercicio css-01 y volvé cada vez que lo necesites.

**CSS** significa *Cascading Style Sheets* (hojas de estilo en cascada).
HTML dice **qué es** cada cosa; CSS dice **cómo se ve**.

---

## 1 · Anatomía de una regla

```
  selector     llave de apertura
  ┌┴┐          │
  h1           {
    color:     purple;        ← declaración
    font-size: 40px;          ← declaración
  }            
  └──┬──┘     └──┬──┘
  propiedad    valor    ← y siempre termina con ;
```

| Parte | Qué es |
|---|---|
| **Selector** | **A quién** se aplica |
| **Propiedad** | **Qué** querés cambiar |
| **Valor** | **Cómo** lo querés |
| **Declaración** | `propiedad: valor;` (¡no te olvides los `:` y el `;`!) |
| **Regla** | Selector + todas sus declaraciones entre `{ }` |

Comentarios en CSS: `/* esto es un comentario */`

---

## 2 · Tres formas de poner CSS (y cuál usar)

```html
<!-- 1. En línea: en el atributo style -->
<p style="color: red;">Hola</p>

<!-- 2. En el <head>, dentro de <style> -->
<style>
  p { color: red; }
</style>

<!-- 3. En un archivo aparte ⭐ -->
<link rel="stylesheet" href="estilos.css">
```

**Usá siempre la 3.** Un solo archivo CSS puede darle estilo a **muchas** páginas: si cambiás un
color, cambia en todo el sitio. Además, el HTML queda limpio.

---

## 3 · La cascada: ¿quién gana?

Muchas veces **varias reglas** le dan valor a la **misma propiedad** del **mismo elemento**.
¿Cuál se aplica? CSS lo decide en este orden:

### a) Especificidad: la regla más específica gana

Cuanto más "puntería" tiene un selector, más peso tiene:

| Selector | Peso | Analogía |
|---|---|---|
| `p` (etiqueta) | 🥉 bajo | "A todas las personas" |
| `.destacado` (clase) | 🥈 medio | "A las personas con remera roja" |
| `#titulo` (id) | 🥇 alto | "A María" |
| `style="..."` (en línea) | 🏆 altísimo | Le hablás al oído |

```css
#aviso    { color: red; }     /* gana: es un id */
.alerta   { color: orange; }
p         { color: black; }
```
```html
<p id="aviso" class="alerta">¿De qué color soy?</p>   <!-- rojo -->
```

### b) Si empatan: gana la **última**

```css
h1 { color: blue; }
h1 { color: green; }   /* ← gana: está después */
```

Por eso el **orden** de tu CSS importa, y también el orden de los `<link>` en el HTML.

> 💡 **Consejo:** usá **clases** para casi todo. Los `id` pesan tanto que después cuesta "pisarlos".
> Y evitá `!important`: es como gritar, y cuando todos gritan nadie se entiende.

---

## 4 · Herencia: los hijos heredan de los padres

Algunas propiedades (sobre todo las de **texto**: `color`, `font-family`, `font-size`, `line-height`)
**se heredan** a todos los elementos de adentro:

```css
body {
  font-family: Arial, sans-serif;
  color: #333;
}
```
→ **Todo** el texto de la página queda en Arial y gris oscuro, sin tener que ponérselo a cada `p`, `li`, `h1`…

Las propiedades de **caja** (`margin`, `padding`, `border`, `background`, `width`) **no** se heredan.

---

## 5 · Los estilos por defecto del navegador

Aunque no pongas CSS, el `h1` se ve grande, los enlaces azules y subrayados y el `body` tiene un margen.
Son los **estilos por defecto** del navegador. Vos los vas pisando con tus reglas.

Casi todos los proyectos empiezan con este "mini reset":

```css
* {
  box-sizing: border-box;   /* se explica en css-03 */
  margin: 0;
  padding: 0;
}
```
(`*` = "todos los elementos".)

---

## 6 · Unidades de medida

| Unidad | Qué es | Cuándo usarla |
|---|---|---|
| `px` | Píxeles: puntitos de la pantalla. Fijo. | Bordes, sombras, detalles chicos |
| `%` | Porcentaje **del elemento padre** | Anchos: `width: 50%` = la mitad del padre |
| `rem` | Relativo al tamaño de letra de la página (por defecto 1rem = 16px) | ⭐ Tamaños de letra y espacios |
| `em` | Relativo al tamaño de letra **del propio elemento** | Espacios que acompañan al texto |
| `vw` / `vh` | 1% del ancho / alto de la **ventana** | Secciones de pantalla completa: `height: 100vh` |
| `fr` | Fracción del espacio libre (solo en Grid) | Columnas de Grid |

> ¿Por qué `rem` y no `px` para la letra? Porque si una persona con baja visión agranda la letra
> en su navegador, los `rem` se agrandan y los `px` no. **Accesibilidad.** 💜

⚠️ **Entre el número y la unidad no va espacio:** `16px` ✅ · `16 px` ❌ · `16` ❌ (excepto el `0`, que no necesita unidad).

---

## 7 · Colores

```css
color: tomato;                     /* por nombre (hay ~140) */
color: #ff6347;                    /* hexadecimal */
color: rgb(255, 99, 71);           /* rojo, verde, azul, de 0 a 255 */
color: rgb(255 99 71 / 0.5);       /* con transparencia al 50% */
```

**¿Cómo se lee el hexadecimal?** `#RRGGBB`: dos dígitos para el **R**ojo, dos para el **V**erde (*Green*)
y dos para el **A**zul (*Blue*). Van de `00` (nada) a `ff` (máximo).

| Hex | Color |
|---|---|
| `#000000` | negro (nada de luz) |
| `#ffffff` | blanco (toda la luz) |
| `#ff0000` | rojo puro |
| `#808080` | gris |

No hace falta calcularlos: **VS Code muestra un cuadradito de color** al lado; hacé clic y aparece un selector. 🎨

---

## 8 · `display`: cómo se comporta una caja

¿Te acordás de los elementos **de bloque** y **en línea** de HTML? Eso se controla con `display`:

| Valor | Comportamiento |
|---|---|
| `block` | Toda la fila, empieza en línea nueva. Acepta `width`, `height`, `margin` |
| `inline` | Dentro del texto. **Ignora** `width`, `height` y el margin de arriba/abajo |
| `inline-block` | Dentro del texto, pero **acepta** `width` y `height` (ideal para botones) |
| `none` | **Desaparece** (no ocupa lugar) |
| `flex` | Sus hijos se acomodan con Flexbox (css-04) |
| `grid` | Sus hijos se acomodan en una grilla (css-05) |

> Cuando un `width` "no hace nada", casi siempre es porque el elemento es `inline` (un `<a>` o un `<span>`).

---

## 9 · CSS no te avisa cuando te equivocás 🤫

HTML perdona, pero CSS es peor: **si una declaración está mal escrita, la ignora en silencio** y sigue.

```css
h1 {
  colr: red;          /* ❌ propiedad mal escrita → ignorada */
  font-size: 20;      /* ❌ falta la unidad → ignorada */
  color: blue         /* ❌ falta el ; → esta Y la siguiente se rompen */
  margin: 10px;
}
```

### 🔍 Checklist: "mi CSS no se aplica"

1. ¿Guardaste el archivo? ¿Recargaste?
2. ¿El `<link>` está en el `<head>` y la **ruta** al `.css` es correcta? ([Rutas](../fundamentos/06-rutas-de-archivos.md))
3. ¿El selector coincide? `.tarjeta` en CSS ↔ `class="tarjeta"` en HTML (sin punto en el HTML, con punto en el CSS).
4. ¿Faltan `:`, `;` o una `}`?
5. **F12 → Elementos**, elegí el elemento y mirá el panel **Estilos**:
   - Si tu regla **no aparece** → el selector no coincide o el CSS no cargó.
   - Si aparece **tachada** → otra regla más específica le gana.
   - Si tiene un ⚠️ amarillo → la propiedad o el valor están mal escritos.

> 💡 En ese mismo panel podés **cambiar valores en vivo** y ver qué pasa. Es la mejor forma de experimentar.
> Cuando te guste, copiá el valor a tu archivo (los cambios en F12 se pierden al recargar).

---

## ✅ Autoevaluación

1. ¿Cuáles son las partes de una regla CSS?
2. ¿Por qué conviene usar un archivo `.css` aparte?
3. Si una clase dice `color: red` y un id dice `color: blue`, ¿cuál gana?
4. Si pongo `font-family` en el `body`, ¿por qué cambian también los párrafos?
5. ¿Qué diferencia hay entre `%` y `px`?
6. ¿Por qué un `<a>` ignora mi `width`?
7. ¿Qué hacés si una regla aparece tachada en F12?
