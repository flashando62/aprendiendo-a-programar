# js-03 · Bucles 🔁

**Rama:** `js-03`
📚 Leer antes: [javascript.info — Bucles: while y for](https://es.javascript.info/while-for)

## Repetir sin copiar y pegar

Si quisieras mostrar los números del 1 al 100, no vas a escribir 100 `console.log`. Para eso están los **bucles**.

### `for` — cuando sabés cuántas veces repetir

```js
for (let i = 1; i <= 5; i++) {
  console.log("Vuelta número", i);
}
```

Se lee: *"empezá con `i` en 1; mientras `i` sea menor o igual a 5, repetí; y en cada vuelta sumale 1 a `i`"*.

### `while` — cuando no sabés cuántas veces

```js
let clave = "";
while (clave !== "1234") {
  clave = prompt("Ingresá la clave:");
}
console.log("¡Entraste!");
```

> ⚠️ **Bucle infinito:** si la condición nunca se vuelve falsa, el programa no termina y la página se cuelga.
> Si te pasa, cerrá la pestaña. No es grave, ¡a todos nos pasó!

## Consigna

1. Mostrá los números del **1 al 20**.
2. Mostrá solo los **números pares** del 1 al 50.
3. **Tabla de multiplicar:** pedí un número y mostrá su tabla del 1 al 10 (`7 x 3 = 21`).
4. **Cuenta regresiva** de 10 a 0 y al final `"¡Despegue! 🚀"`.
5. **Sumador:** sumá todos los números del 1 al 100 y mostrá el resultado (debería dar 5050).
6. **FizzBuzz** (un clásico de las entrevistas de trabajo 😎): del 1 al 30, mostrá:
   - `"Fizz"` si el número es múltiplo de 3
   - `"Buzz"` si es múltiplo de 5
   - `"FizzBuzz"` si es múltiplo de los dos
   - El número, si no es ninguno
7. **Adiviná el número:** la compu elige un número del 1 al 10
   (`Math.floor(Math.random() * 10) + 1`) y te pide que lo adivines hasta que aciertes,
   diciéndote "más alto" o "más bajo". Al final, decí en cuántos intentos lo lograste.

## ✅ Checklist
- [ ] Usaste `for` y `while`
- [ ] FizzBuzz funciona bien con el 15 y el 30
- [ ] Jugaste al "adiviná el número" al menos 3 veces 🎲
