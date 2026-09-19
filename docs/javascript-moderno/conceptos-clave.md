# ⚡ JavaScript moderno · Conceptos clave

> 📌 Primer módulo de la **Etapa 2**. Leé esto antes del ejercicio jsm-01.
> Node.js y React usan **todo el tiempo** lo que está en esta guía. Si algo de acá no queda claro,
> después React va a parecer magia negra. 🧙‍♀️

---

## 1 · Funciones flecha (repaso a fondo)

```js
// Función clásica
function doble(n) {
  return n * 2;
}

// Flecha con llaves: necesita return
const doble = (n) => {
  return n * 2;
};

// Flecha de una sola expresión: el return es implícito
const doble = (n) => n * 2;

// Un solo parámetro: los paréntesis son opcionales
const doble = n => n * 2;

// Sin parámetros: paréntesis vacíos
const saludar = () => console.log("Hola");
```

⚠️ Para devolver un **objeto** directo, envolvelo en paréntesis (si no, JS cree que las llaves son el bloque):
```js
const crearUsuario = (nombre) => ({ nombre, activo: true });
```

---

## 2 · Métodos de arrays: `map`, `filter`, `find`, `reduce`

Reemplazan a la mayoría de los `for`. **React los usa en cada pantalla.**

```js
const productos = [
  { nombre: "Remera", precio: 15000, stock: 3 },
  { nombre: "Gorra",  precio: 8000,  stock: 0 },
  { nombre: "Buzo",   precio: 30000, stock: 5 },
];
```

| Método | Qué hace | Devuelve |
|---|---|---|
| `map` | **Transforma** cada elemento | Un array nuevo, **del mismo largo** |
| `filter` | **Se queda** con los que cumplen | Un array nuevo, **igual o más corto** |
| `find` | **Busca** el primero que cumple | **Un elemento** (o `undefined`) |
| `some` / `every` | ¿**Alguno** / **todos** cumplen? | `true` / `false` |
| `reduce` | **Acumula** todo en un solo valor | Un valor (número, objeto…) |

```js
const nombres  = productos.map(p => p.nombre);             // ["Remera", "Gorra", "Buzo"]
const conStock = productos.filter(p => p.stock > 0);       // Remera y Buzo
const gorra    = productos.find(p => p.nombre === "Gorra"); // { nombre: "Gorra", ... }
const hayCaros = productos.some(p => p.precio > 20000);    // true
const total    = productos.reduce((suma, p) => suma + p.precio, 0);  // 53000
```

> 💡 Ninguno de estos **modifica** el array original: siempre crean uno nuevo. Esto se llama
> **inmutabilidad** y en React es **obligatorio**.

---

## 3 · Desestructuración: sacar cosas de objetos y arrays

```js
const usuario = { nombre: "Ana", edad: 18, ciudad: "Rosario" };

// ❌ Antes
const nombre = usuario.nombre;
const edad = usuario.edad;

// ✅ Ahora
const { nombre, edad } = usuario;
```

Con arrays, por **posición**:
```js
const colores = ["rojo", "verde", "azul"];
const [primero, segundo] = colores;   // "rojo", "verde"
```

Muy usado en los **parámetros** de una función (así se reciben las *props* en React):
```js
function presentar({ nombre, ciudad }) {
  return `${nombre} vive en ${ciudad}`;
}
presentar(usuario);
```

---

## 4 · Spread `...`: copiar y combinar

Los tres puntos **"desparraman"** el contenido de un array u objeto:

```js
const a = [1, 2];
const b = [...a, 3, 4];           // [1, 2, 3, 4]  (array nuevo)

const usuario = { nombre: "Ana", edad: 18 };
const mayor = { ...usuario, edad: 19 };   // copia y cambia edad → { nombre: "Ana", edad: 19 }
```

En React vas a hacer esto **todo el tiempo** para "modificar" datos sin tocar el original:
```js
const tareasNuevas = [...tareas, nuevaTarea];              // agregar
const sinLaTres    = tareas.filter(t => t.id !== 3);       // borrar
const actualizadas = tareas.map(t => t.id === 3 ? { ...t, hecha: true } : t);  // modificar
```

---

## 5 · Operador ternario y cortocircuito

```js
// Ternario: un if/else en una línea → condición ? siEsVerdad : siEsFalso
const mensaje = edad >= 18 ? "Mayor" : "Menor";

// && : si lo de la izquierda es verdadero, devuelve lo de la derecha
const aviso = hayErrores && "Revisá el formulario";

// ?? : valor por defecto si es null o undefined
const nombreFinal = nombre ?? "Anónima";

// ?. : acceder sin romper si algo no existe
const calle = usuario.direccion?.calle;   // undefined en vez de error
```

Los vas a ver muchísimo dentro del JSX de React.

---

## 6 · Módulos: `import` y `export`

Cuando un proyecto crece, el código se divide en **varios archivos** (módulos). Cada uno **exporta**
lo que quiere compartir, y los demás lo **importan**.

```js
// matematica.js
export function sumar(a, b) { return a + b; }
export const PI = 3.1416;

export default function restar(a, b) { return a - b; }   // la exportación "principal" (una por archivo)
```

```js
// app.js
import restar, { sumar, PI } from "./matematica.js";
//     └ default   └ con nombre (entre llaves, mismo nombre)
```

En el navegador, para usar módulos el script se carga con `type="module"`:
```html
<script type="module" src="app.js"></script>
```
⚠️ Los módulos **no funcionan con doble clic** en el HTML (`file://`): necesitás **Live Server**.

---

## 7 · JSON: el idioma en que se hablan las aplicaciones

**JSON** (*JavaScript Object Notation*) es un formato de **texto** para mandar datos.
Se parece a un objeto de JS, pero es **texto** y es más estricto (comillas dobles en todas las claves):

```json
{
  "nombre": "Ana",
  "edad": 18,
  "cursos": ["HTML", "CSS"]
}
```

```js
const texto = JSON.stringify({ nombre: "Ana" });  // objeto → texto: '{"nombre":"Ana"}'
const objeto = JSON.parse(texto);                 // texto → objeto
```

---

## 8 · Asincronía: esperar sin congelarse ⏳

Algunas cosas **tardan**: pedir datos a un servidor, leer un archivo, esperar un temporizador.
JavaScript **no se queda esperando**: sigue con lo siguiente y "vuelve" cuando llega la respuesta.

```js
console.log("1");
setTimeout(() => console.log("2"), 1000);   // dentro de 1 segundo
console.log("3");
// Muestra: 1, 3, 2
```

> 🍔 **Analogía:** en un local de comida rápida pedís, te dan un **número** y te corrés.
> No bloqueás la fila. Cuando está lista, te llaman. Ese número es una **promesa**.

### Promesas

Una **promesa** (*Promise*) es un valor que **todavía no está**, pero va a estar (o va a fallar).

### `async` / `await`: la forma cómoda

```js
async function cargarUsuario() {
  const respuesta = await fetch("https://jsonplaceholder.typicode.com/users/1");
  const usuario = await respuesta.json();
  console.log(usuario.name);
}

cargarUsuario();
```

- `await` = **"esperá acá hasta que la promesa se resuelva"**.
- Solo se puede usar `await` **dentro de una función `async`** (o en el nivel principal de un módulo).
- Una función `async` **siempre devuelve una promesa**.

### Manejar errores con `try` / `catch`

La red puede fallar. Siempre protegé los pedidos:

```js
async function cargarUsuario() {
  try {
    const respuesta = await fetch("https://jsonplaceholder.typicode.com/users/1");
    if (!respuesta.ok) {
      throw new Error(`Error del servidor: ${respuesta.status}`);
    }
    const usuario = await respuesta.json();
    console.log(usuario.name);
  } catch (error) {
    console.error("No se pudo cargar:", error.message);
  }
}
```

---

## 9 · APIs: pedirle datos a otro programa

Una **API** es una "ventanilla" que un programa ofrece para que otros le pidan cosas.
Una **API web** es un servidor que, en lugar de páginas HTML, responde **datos en JSON**.

```
Tu página ──── GET https://api.ejemplo.com/productos ────► Servidor
          ◄──── [ { "nombre": "Remera", ... }, ... ] ─────
```

Cada dirección de la API se llama **endpoint**. Y cada pedido tiene un **método** (qué querés hacer):

| Método | Para | Ejemplo |
|---|---|---|
| `GET` | **Leer** datos | Ver la lista de productos |
| `POST` | **Crear** algo nuevo | Agregar un producto |
| `PUT` / `PATCH` | **Modificar** algo | Cambiar el precio |
| `DELETE` | **Borrar** algo | Eliminar un producto |

Y cada respuesta trae un **código de estado**:

| Código | Significa |
|---|---|
| `200` | OK ✅ |
| `201` | Creado ✅ |
| `400` | Pedido mal hecho (faltan datos) |
| `404` | No existe |
| `500` | El servidor se rompió 💥 |

🔍 En **F12 → Red** (*Network*) podés ver cada pedido que hace una página, con su método, código y respuesta.

---

## ✅ Autoevaluación

1. ¿Qué diferencia hay entre `map` y `filter`? ¿Y entre `filter` y `find`?
2. ¿Qué hace `const { nombre } = usuario`?
3. ¿Cómo agregás un elemento a un array **sin modificar** el original?
4. ¿Por qué `console.log` de algo que viene de `fetch` a veces muestra `Promise {<pending>}`?
5. ¿Qué es un endpoint? ¿Qué método usarías para borrar algo?
6. ¿Qué diferencia hay entre un objeto de JS y un JSON?
