# js-01 · Variables y tipos de datos 📦

**Rama:** `js-01`
📚 Leer antes:
- [MDN — ¿Qué es JavaScript?](https://developer.mozilla.org/es/docs/Learn/JavaScript/First_steps/What_is_JavaScript)
- [javascript.info — Variables](https://es.javascript.info/variables) y [Tipos de datos](https://es.javascript.info/types)

## Programar es dar instrucciones

Un programa es una **lista de instrucciones** que la compu ejecuta **en orden, de arriba hacia abajo**.
La compu no piensa: hace exactamente lo que le decís. Si le decís algo mal, lo hace mal. 🤖

## Cómo ejecutar JavaScript (así lo vas a hacer en los ejercicios js-01 a js-05)

Creá dos archivos en `solucion/`:

**`index.html`**
```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8">
    <title>js-01</title>
  </head>
  <body>
    <h1>Abrí la consola con F12 👀</h1>
    <script src="script.js"></script>
  </body>
</html>
```

**`script.js`**
```js
console.log("¡Hola, mundo!");
```

Abrí `index.html` con Live Server → **F12** → pestaña **Consola**. ¡Ahí aparece tu mensaje! 🎉
`console.log()` es tu mejor amigo: muestra cosas en la consola.

## Variables

Una **variable** es una cajita con un nombre donde guardás un dato.

```js
let edad = 18;          // let: el valor puede cambiar
const nombre = "Ana";   // const: el valor NO puede cambiar

edad = 19;              // ✅ se puede
// nombre = "Eva";      // ❌ error: es const

console.log(nombre, "tiene", edad, "años");
```

> 💡 Usá `const` siempre que puedas, y `let` solo si el valor va a cambiar.
> (Vas a ver `var` en internet: es la forma vieja, no la uses.)

## Tipos de datos

```js
const texto = "Hola";          // string (texto, siempre entre comillas)
const numero = 42;             // number
const decimal = 3.14;          // number (con punto, no coma)
const verdadero = true;        // boolean (true o false)
let nada;                      // undefined (todavía no tiene valor)

console.log(typeof texto);     // "string"
```

Operaciones:
```js
console.log(10 + 5);           // 15
console.log(10 * 2);           // 20
console.log(10 / 4);           // 2.5
console.log(10 % 3);           // 1  (el resto de la división)
console.log("Hola " + "Ana");  // "Hola Ana"  (unir textos)
console.log(`Tengo ${edad} años`);  // template string: meter variables en un texto (con comillas invertidas ` `)
```

## Consigna

En `solucion/script.js`:

1. Creá variables con tu nombre, tu edad, tu ciudad y si te gusta el mate (`true`/`false`).
2. Mostrá una presentación en la consola usando un **template string**:
   `Hola, soy Ana, tengo 18 años y vivo en Córdoba.`
3. Calculá y mostrá **cuántos años vas a tener en 2035**.
4. Calculá cuántos **días** viviste aproximadamente (edad × 365).
5. **Calculadora de propina:** creá una variable `cuenta` (ej. 12500) y `porcentaje` (ej. 10).
   Calculá la propina y el total, y mostralos.
6. Mostrá con `typeof` el tipo de 3 de tus variables.
7. **Probá romper algo:** intentá cambiar una `const`. Leé el error en la consola y copialo en el PR.

## Para pensar 🤔
¿Qué da `"5" + 3`? ¿Y `"5" * 3`? Probalo y tratá de explicar por qué.

## ✅ Checklist
- [ ] Usaste `let` y `const` correctamente
- [ ] Usaste al menos un template string
- [ ] Todo se ve en la consola sin errores (salvo el que rompiste a propósito, que después comentás con `//`)
