# js-04 · Funciones 🧩

**Rama:** `js-04`
📚 Leer antes: [javascript.info — Funciones](https://es.javascript.info/function-basics)

## Recetas reutilizables

Una **función** es un bloque de código con nombre que podés usar cuantas veces quieras.
Como una receta: la escribís una vez y la cocinás cuando quieras.

```js
// Definir la función
function saludar(nombre) {
  console.log(`¡Hola, ${nombre}!`);
}

// Usarla (llamarla)
saludar("Ana");    // ¡Hola, Ana!
saludar("Luz");    // ¡Hola, Luz!
```

- `nombre` es un **parámetro**: un dato que la función recibe.
- `"Ana"` es el **argumento**: el valor concreto que le pasás.

### Devolver un resultado con `return`

```js
function sumar(a, b) {
  return a + b;
}

const resultado = sumar(3, 4);
console.log(resultado);   // 7
```

`return` **devuelve** un valor y **termina** la función. Lo que está después del `return` no se ejecuta.

> 💡 Diferencia clave: `console.log` **muestra** algo. `return` **devuelve** algo para que lo uses después.

### Funciones flecha (otra forma de escribirlas)

```js
const multiplicar = (a, b) => a * b;
```

## Consigna

Escribí estas funciones y **probá cada una al menos 3 veces** con distintos valores:

1. `esPar(numero)` → devuelve `true` o `false`.
2. `celsiusAFahrenheit(grados)` → fórmula: `grados * 9 / 5 + 32`.
3. `calcularPromedio(nota1, nota2, nota3)` → devuelve el promedio.
4. `aprobo(nota1, nota2, nota3)` → **usa** `calcularPromedio` y devuelve `true` si el promedio es 6 o más.
5. `esMayorDeEdad(edad)` → devuelve `true` o `false`.
6. `precioConDescuento(precio, porcentaje)` → devuelve el precio final.
7. `mayor(a, b)` → devuelve el mayor de los dos números (sin usar `Math.max`).
8. `repetirTexto(texto, veces)` → devuelve el texto repetido (usá un bucle). `repetirTexto("ja", 3)` → `"jajaja"`.

## Para pensar 🤔
¿Por qué conviene escribir `aprobo` usando `calcularPromedio` en lugar de volver a calcular el promedio adentro?

## ✅ Checklist
- [ ] Todas las funciones usan `return`
- [ ] Los nombres de las funciones dicen qué hacen
- [ ] Al menos una función usa otra función
- [ ] Hiciste al menos una función flecha
