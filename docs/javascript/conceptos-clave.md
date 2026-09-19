# 🧠 JavaScript · Conceptos clave

> 📌 Leé esto **antes** del ejercicio js-01. Si todavía no leíste [¿Qué es programar?](../fundamentos/04-que-es-programar.md), empezá por ahí.

---

## 1 · ¿Qué es JavaScript y dónde corre?

JavaScript (JS) es un **lenguaje de programación**. A diferencia de HTML y CSS, puede
**tomar decisiones**, **repetir cosas**, **hacer cálculos** y **reaccionar** a lo que hace el usuario.

Viene **incluido en todos los navegadores**: no hay que instalar nada. El navegador lee tu archivo `.js`
y ejecuta las instrucciones.

La **consola** (F12 → Consola) es donde JavaScript muestra mensajes y errores. También podés escribir
JavaScript directo ahí para probar cosas rápidas: escribí `2 + 2` y Enter. 🧪

---

## 2 · Un programa se ejecuta de arriba hacia abajo

```js
console.log("Primero");
console.log("Segundo");
console.log("Tercero");
```

Cada línea es una **instrucción** (o *sentencia*). Se ejecutan **en orden, una por una**.
Si una línea tiene un error, **el programa se frena ahí** y lo de abajo no se ejecuta.

> 💡 Terminá cada instrucción con `;`. JavaScript a veces lo adivina si te lo olvidás,
> pero es mejor no depender de eso.

---

## 3 · Las mayúsculas importan

```js
const nombre = "Ana";
console.log(Nombre);   // ❌ ReferenceError: Nombre is not defined
```

`nombre`, `Nombre` y `NOMBRE` son **tres cosas distintas**. Lo mismo con las palabras del lenguaje:
`console.log` ✅ · `Console.Log` ❌.

---

## 4 · Comentarios

```js
// Comentario de una línea

/*
  Comentario
  de varias líneas
*/
```

Úsalos para explicar **por qué** hacés algo, no **qué** (el qué ya lo dice el código).
También sirven para "apagar" una línea mientras probás.

---

## 5 · Valores y tipos

Todo en un programa son **valores**, y cada valor tiene un **tipo**:

| Tipo | Ejemplos | Para qué |
|---|---|---|
| **string** (texto) | `"Hola"`, `'Ana'`, `` `Hola ${nombre}` `` | Palabras, frases. **Siempre entre comillas** |
| **number** (número) | `42`, `3.14`, `-7` | Cuentas. **Sin comillas**, decimales con **punto** |
| **boolean** (booleano) | `true`, `false` | Sí o no. Resultado de las comparaciones |
| **undefined** | `undefined` | "Todavía no tiene valor" |
| **null** | `null` | "Vacío, a propósito" |
| **array** | `[1, 2, 3]` | Listas |
| **object** | `{ nombre: "Ana" }` | Fichas con datos |

### ⚠️ `"5"` no es lo mismo que `5`

```js
5 + 5       // 10     (números: suma)
"5" + "5"   // "55"   (textos: los pega)
"5" + 5     // "55"   (si uno es texto, pega)
```

Todo lo que viene de un `prompt()` o de un `<input>` es **texto**, aunque la persona escriba un número.
Para convertirlo: `Number("5")` → `5`.

---

## 6 · Variables: cajitas con nombre

```js
let puntos = 0;           // creo la caja "puntos" y guardo 0
puntos = puntos + 10;     // saco lo que hay, le sumo 10, lo vuelvo a guardar → 10
```

⚠️ En programación, `=` **no significa "es igual"**: significa **"guardá lo de la derecha en la caja de la izquierda"**.
Por eso `puntos = puntos + 10` tiene sentido (en matemática no lo tendría).

| Palabra | Cuándo |
|---|---|
| `const` | El valor **no va a cambiar**. **Usalo por defecto.** |
| `let` | El valor **va a cambiar** (contadores, acumuladores…) |
| `var` | Forma antigua. **No la uses** (la vas a ver en tutoriales viejos). |

### Cómo nombrar variables

- **camelCase:** la primera palabra en minúscula y las siguientes con mayúscula: `precioTotal`, `cantidadDeAlumnos`.
- **Nombres que expliquen:** `edadUsuario` ✅ · `x` ❌ · `dato2` ❌.
- Sin espacios, sin tildes, sin empezar con número.
- Los booleanos suelen empezar con `es`, `tiene`, `puede`: `esMayor`, `tieneEntrada`.

---

## 7 · Bloques y llaves `{ }`

Las llaves agrupan instrucciones que van juntas: lo que se ejecuta **si** se cumple un `if`,
lo que se **repite** en un `for`, lo que hace una **función**.

```js
if (edad >= 18) {
  // todo lo que está acá adentro
  // pertenece al if
}
```

Cada `{` necesita su `}`. **Indentá** lo de adentro para ver dónde empieza y termina cada bloque.

Una variable creada con `let` o `const` **adentro** de unas llaves **solo existe adentro** de esas llaves.
Eso se llama **alcance** (*scope*):

```js
if (true) {
  const mensaje = "Hola";
}
console.log(mensaje);   // ❌ ReferenceError: mensaje no existe acá afuera
```

---

## 8 · Entrada → Proceso → Salida

Casi todos los programas hacen lo mismo:

```
 📥 ENTRADA              ⚙️ PROCESO               📤 SALIDA
 datos que llegan   →    cálculos y decisiones  →  un resultado
 (prompt, input,          (variables, if,          (console.log, alert,
  un clic)                 for, funciones)          cambiar la página)
```

Cuando arranques un ejercicio, preguntate: **¿qué entra?, ¿qué tengo que hacer?, ¿qué tiene que salir?**
Y escribilo en [pseudocódigo](../fundamentos/04-que-es-programar.md) antes de programar.

---

## 9 · Los errores más comunes (y qué significan)

| Error en la consola | Traducción | Causa típica |
|---|---|---|
| `SyntaxError: Unexpected token` | "Encontré algo que no esperaba" | Falta o sobra un `)`, `}`, `,` o una comilla |
| `SyntaxError: Unexpected end of input` | "Se terminó el archivo antes de tiempo" | Te falta cerrar una `}` |
| `ReferenceError: x is not defined` | "No existe nada llamado `x`" | Nombre mal escrito, mayúsculas, o la variable está en otro bloque |
| `TypeError: x is not a function` | "`x` no es una función" | Escribiste mal el nombre de una función (`console.lg`) |
| `TypeError: Cannot read properties of null` | "Intentaste usar algo que no existe" | `querySelector` no encontró el elemento (¿el id está bien? ¿el script está al final del body?) |
| `TypeError: Assignment to constant variable` | "Intentaste cambiar una `const`" | Usá `let` si el valor cambia |

**Siempre mirá la parte de la derecha**: `script.js:12` → archivo y **número de línea**. Hacé clic y te lleva.

> Más sobre leer errores: [Cómo aprender y pedir ayuda](../fundamentos/08-aprender-y-pedir-ayuda.md).

---

## 10 · Debuggear con `console.log`

Cuando algo no funciona y no sabés por qué, **espiá** qué está pasando adentro del programa:

```js
const precio = prompt("Precio:");
console.log("precio vale:", precio, typeof precio);   // 👀 precio vale: 100 string
const total = precio * 1.21;
console.log("total vale:", total);
```

Poné `console.log` en distintos lugares para ver:
- ¿**Llega** el programa hasta acá?
- ¿Qué **valor** tiene cada variable en este momento?
- ¿Es del **tipo** que yo creía?

Cuando encuentres el error, borrá esos `console.log`.

---

## 11 · Cómo encarar un ejercicio

1. **Leé la consigna dos veces.** ¿Qué entra, qué sale?
2. **Escribí el pseudocódigo** como comentarios en el archivo.
3. **Dividí** el problema en pasos chiquitos. Resolvé **uno** por vez.
4. **Probá después de cada paso** (con `console.log`). No escribas 30 líneas sin probar.
5. **Probá casos raros:** 0, números negativos, texto vacío, texto en vez de número.
6. Cuando funcione, **hacé commit**. Después mejorá.

---

## ✅ Autoevaluación

1. ¿En qué orden se ejecutan las instrucciones?
2. ¿Qué da `"3" + 4`? ¿Por qué?
3. ¿Qué significa `=` en JavaScript? ¿Y `===`?
4. ¿Cuándo uso `const` y cuándo `let`?
5. Si ves `ReferenceError: total is not defined at script.js:8`, ¿qué revisás primero?
6. ¿Para qué sirve `console.log` además de mostrar resultados?
