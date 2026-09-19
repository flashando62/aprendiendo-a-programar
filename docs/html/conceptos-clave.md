# 🦴 HTML · Conceptos clave

> 📌 Leé esto **antes** del ejercicio html-01 y volvé cada vez que lo necesites.

**HTML** significa *HyperText Markup Language* (lenguaje de marcado de hipertexto).

- **Lenguaje de marcado:** no da órdenes; **marca** qué es cada parte de un texto.
  Como cuando en un apunte subrayás los títulos con rojo y las definiciones con verde.
- **Hipertexto:** texto con **enlaces** que te llevan a otros textos. Es la idea que inventó la web.

---

## 1 · Anatomía de un elemento

```
   etiqueta de apertura          etiqueta de cierre
   ┌────────┴────────┐           ┌─┴─┐
   <a href="info.html">Más info</a>
      └─┬┘ └────┬───┘ └───┬──┘
   atributo   valor    contenido
   
   └──────────────── elemento ─────────────────┘
```

| Parte | Qué es |
|---|---|
| **Etiqueta** (*tag*) | El nombre entre `< >`. Dice **qué es**: `a` = enlace, `p` = párrafo |
| **Cierre** | Igual que la apertura pero con `/`. Dice dónde termina |
| **Contenido** | Lo que está entre las dos etiquetas |
| **Atributo** | Información extra, **siempre en la etiqueta de apertura**: `nombre="valor"` |
| **Elemento** | Todo junto |

Un elemento puede tener varios atributos, separados por espacios:
```html
<img src="gato.jpg" alt="Un gato naranja durmiendo" width="300">
```

### Elementos vacíos (no se cierran)

Algunos elementos no tienen contenido, así que **no llevan etiqueta de cierre**:
`<img>`, `<br>`, `<hr>`, `<input>`, `<meta>`, `<link>`.

```html
<img src="foto.jpg" alt="...">     ✅
<img src="foto.jpg" alt="..."></img>   ❌
```

---

## 2 · Anidación: elementos adentro de elementos

Los elementos se pueden meter **adentro** de otros. Como las cajas de mudanza, o las carpetas de tu compu:

```html
<ul>
  <li>Leer <strong>mucho</strong></li>
  <li>Practicar</li>
</ul>
```

### Regla de oro: se cierra en orden inverso

**Lo último que abriste es lo primero que cerrás.** Como las mamushkas 🪆.

```html
<p>Esto es <strong>muy importante</strong></p>     ✅
<p>Esto es <strong>muy importante</p></strong>     ❌  ¡se cruzan!
```

### El árbol de la página

Por la anidación, toda página HTML forma un **árbol** (¡como las carpetas!):

```html
<html>
  <head>
    <title>Mi página</title>
  </head>
  <body>
    <h1>Hola</h1>
    <ul>
      <li>Uno</li>
      <li>Dos</li>
    </ul>
  </body>
</html>
```

```
html
├── head
│   └── title
└── body
    ├── h1
    └── ul
        ├── li
        └── li
```

- `body` es **padre** (o madre) de `h1` y `ul`.
- `h1` y `ul` son **hermanos**.
- Los `li` son **hijos** de `ul` y **descendientes** de `body`.

Esta familia es **fundamental**: CSS la usa para elegir elementos (`nav a` = "los `a` dentro de `nav`")
y JavaScript la usa para recorrer y modificar la página (se llama **DOM**).

> 💡 **Por eso indentamos:** cada nivel del árbol, un `Tab` más a la derecha. Así el árbol se *ve*.

---

## 3 · Elementos de bloque y en línea

Hay dos grandes familias de elementos, según cómo se ubican en la página:

| **De bloque** (*block*) | **En línea** (*inline*) |
|---|---|
| Ocupan **todo el ancho** disponible | Ocupan **solo lo que necesitan** |
| Empiezan en una **línea nueva** | Se acomodan **dentro del texto**, uno al lado del otro |
| `<h1>`–`<h6>`, `<p>`, `<ul>`, `<li>`, `<div>`, `<section>`, `<header>`, `<form>` | `<a>`, `<strong>`, `<em>`, `<span>`, `<img>`, `<button>`, `<input>` |
| Son los "ladrillos" de la página | Son "palabras" dentro del ladrillo |

```
┌─────────────────────────────────────────┐
│ <h1> (bloque: toda la fila)             │
└─────────────────────────────────────────┘
┌─────────────────────────────────────────┐
│ <p> Un texto con [<a>enlace] y [<strong>]│
└─────────────────────────────────────────┘
```

Dos etiquetas "comodín", sin significado propio, muy usadas para agrupar y dar estilo:
- `<div>` → una caja genérica **de bloque**.
- `<span>` → un pedacito genérico **en línea**.

(Preferí siempre una etiqueta semántica si existe: `<nav>`, `<section>`… Usá `div` y `span` cuando no haya otra.)

---

## 4 · Los espacios y los Enter se ignoran

Para HTML, **muchos espacios o Enter seguidos valen como un solo espacio**:

```html
<p>Hola         mundo.


Chau.</p>
```
Se ve: `Hola mundo. Chau.`

Por eso podés indentar tranquila. Si querés **otro párrafo**, usá otro `<p>`.
(Y el espacio entre elementos se maneja con CSS, no con Enter.)

---

## 5 · Comentarios

```html
<!-- Esto es un comentario. No se ve en la página. -->
```

Sirven para dejar notas o "apagar" código sin borrarlo.
⚠️ Igual se ven en **Ver código fuente**: no pongas secretos.

---

## 6 · Caracteres especiales

`<` y `>` significan "etiqueta". Si querés **mostrar** esos símbolos, usá **entidades**:

| Escribís | Se ve |
|---|---|
| `&lt;` | < |
| `&gt;` | > |
| `&amp;` | & |
| `&copy;` | © |
| `&nbsp;` | un espacio que no se corta |

---

## 7 · El navegador perdona… y eso es un problema

Si te olvidás de cerrar una etiqueta, el navegador **no te avisa**: adivina qué quisiste hacer
y a veces adivina mal. La página se ve "rara" y no sabés por qué.

**Cómo detectar errores:**
- Fijate en los **colores** de VS Code: si algo cambia de color de golpe, falta cerrar algo.
- Usá el validador oficial: https://validator.w3.org/#validate_by_input (pegá tu código).
- Mirá el árbol en **F12 → Elementos**: muestra cómo lo **entendió** el navegador.

---

## 8 · ¿Por qué importa la semántica y el `alt`?

Usar la etiqueta correcta (`<nav>`, `<button>`, `<h1>`) no es un capricho:

- **Accesibilidad:** las personas ciegas usan **lectores de pantalla** que leen la página en voz alta.
  El lector usa las etiquetas para saber qué es cada cosa ("menú de navegación", "título", "botón")
  y lee el `alt` de las imágenes. Sin `alt`, dice "imagen" y nada más.
- **Buscadores:** Google entiende mejor tu página y la muestra mejor.
- **Vos del futuro:** `<nav>` se entiende mucho más rápido que `<div class="cosa-3">`.

> Los títulos (`h1`…`h6`) son para **jerarquía**, no para el tamaño de letra (el tamaño se cambia con CSS).
> Una página tiene **un solo `<h1>`**, y después `h2`, `h3`… en orden, sin saltearse.

---

## ✅ Autoevaluación

¿Podés responder sin mirar?

1. ¿Qué diferencia hay entre una etiqueta y un elemento?
2. ¿Dónde van los atributos?
3. ¿Qué tiene de raro `<img>`?
4. En `<p><a>Hola</p></a>`, ¿qué está mal?
5. ¿Qué diferencia hay entre `<div>` y `<span>`?
6. ¿Por qué no se ven los Enter que pongo en el HTML?
7. ¿Para qué sirve el `alt`?
