# js-06 · El DOM y los eventos 🖱️

- **Rama:** `js-06`
- 📚 Leer antes:
  - [MDN — Manipular documentos](https://developer.mozilla.org/es/docs/Learn/JavaScript/Client-side_web_APIs/Manipulating_documents)
  - [javascript.info — Introducción a los eventos](https://es.javascript.info/introduction-browser-events)

## Acá se junta todo: HTML + CSS + JavaScript ✨

El **DOM** es cómo JavaScript "ve" tu página HTML: como un árbol de elementos que puede **leer y modificar**.

### 1 · Buscar un elemento

```html
<h1 id="titulo">Hola</h1>
<button id="boton">Tocame</button>
```

```js
const titulo = document.querySelector("#titulo");   // igual que en CSS: # para id, . para clase
const boton = document.querySelector("#boton");
```

### 2 · Modificarlo

```js
titulo.textContent = "¡Chau!";           // cambiar el texto
titulo.style.color = "tomato";           // cambiar un estilo
titulo.classList.add("destacado");       // agregar una clase CSS (¡mejor que .style!)
titulo.classList.toggle("oculto");       // si la tiene la saca, si no la pone
```

### 3 · Reaccionar a lo que hace el usuario (eventos)

```js
boton.addEventListener("click", () => {
  titulo.textContent = "¡Me tocaste!";
});
```

Eventos comunes: `click`, `input` (cuando se escribe en un campo), `submit` (enviar formulario), `mouseover`.

### Leer lo que escriben en un input

```js
const campo = document.querySelector("#nombre");
console.log(campo.value);
```

## Consigna

Creá `solucion/index.html`, `solucion/estilos.css` y `solucion/script.js` con estas mini apps, una debajo de la otra:

1. **Contador:** un número en pantalla y botones `+`, `−` y `Reiniciar`. Si el número es negativo, que se vea en rojo.
2. **Saludador:** un input para escribir tu nombre y un botón. Al tocarlo, aparece `¡Hola, [nombre]!` en la página.
   Si el input está vacío, mostrá un mensaje de error.
3. **Modo oscuro:** un botón que cambie la página entre claro y oscuro (pista: `document.body.classList.toggle("oscuro")` y una clase `.oscuro` en el CSS).
4. **Contador de caracteres:** un `textarea` y debajo `"23 / 140 caracteres"` que se actualice mientras escribís (evento `input`).
   Si pasa de 140, que se ponga en rojo.

> 💡 Poné el `<script>` al final del `<body>`, así cuando se ejecuta, el HTML ya existe.

## ✅ Checklist
- [ ] Usaste `querySelector`, `textContent` y `addEventListener`
- [ ] Cambiaste estilos usando `classList` (no solo `.style`)
- [ ] Leíste el `value` de un input
- [ ] No hay errores en la consola (F12)
