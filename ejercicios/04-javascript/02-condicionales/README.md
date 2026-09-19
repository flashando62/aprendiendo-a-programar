# js-02 · Condicionales 🔀

- **Rama:** `js-02`
- 📚 Leer antes: [javascript.info — Operadores de comparación](https://es.javascript.info/comparison), [Condicionales](https://es.javascript.info/ifelse) y [Operadores lógicos](https://es.javascript.info/logical-operators)

## Tomar decisiones

```js
const edad = 17;

if (edad >= 18) {
  console.log("Podés votar");
} else if (edad >= 16) {
  console.log("Podés votar de forma optativa");
} else {
  console.log("Todavía no podés votar");
}
```

### Comparaciones

| Operador | Significa |
|---|---|
| `===` | igual a (usá siempre este, con **3** iguales) |
| `!==` | distinto de |
| `>` `<` | mayor, menor |
| `>=` `<=` | mayor o igual, menor o igual |

> ⚠️ `=` **guarda** un valor. `===` **compara**. Confundirlos es el error más común del mundo.

### Combinar condiciones

```js
if (edad >= 18 && tieneDni) { }   // && = Y  (las dos tienen que cumplirse)
if (esFeriado || esFinde) { }     // || = O  (alcanza con una)
if (!llueve) { }                  // !  = NO (lo contrario)
```

### Pedirle datos al usuario
```js
const nombre = prompt("¿Cómo te llamás?");         // devuelve texto
const edad = Number(prompt("¿Cuántos años tenés?")); // Number() lo convierte a número
alert(`Hola ${nombre}`);
```

## Consigna

Mismo formato que js-01 (`index.html` + `script.js`). Hacé estos programas, uno debajo del otro:

1. **Par o impar:** pedí un número y decí si es par o impar (pista: `%`).
2. **Semáforo:** una variable `color` ("verde", "amarillo", "rojo") y mostrá qué hacer en cada caso.
   Si es otro color, mostrá "Color inválido".
3. **Nota:** pedí una nota del 1 al 10 y mostrá:
   - 1 a 3 → "Desaprobado"
   - 4 a 6 → "Aprobado"
   - 7 a 9 → "Muy bien"
   - 10 → "¡Excelente!"
   - Otro número → "Nota inválida"
4. **Entrada al boliche:** pedí edad y si tiene entrada (`confirm()` devuelve `true`/`false`).
   Puede pasar solo si es mayor de 18 **y** tiene entrada.

## ✅ Checklist
- [ ] Usaste `if`, `else if` y `else`
- [ ] Usaste `===` (y no `==`)
- [ ] Usaste `&&` o `||`
- [ ] Probaste cada programa con varios valores, incluidos valores "raros" (0, negativos, texto)
