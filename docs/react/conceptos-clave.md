# ⚛️ React · Conceptos clave

> 📌 Leé esto antes del ejercicio react-01. Antes, asegurate de dominar
> [JavaScript moderno](../javascript-moderno/conceptos-clave.md): `map`, desestructuración, spread,
> `import`/`export` y ternarios. React los usa en **cada línea**.

---

## 1 · ¿Qué es React y por qué existe?

¿Te acordás de la [lista de tareas](../../ejercicios/04-javascript/07-proyecto-lista-de-tareas/) con JavaScript puro?
Tenías que acordarte de **actualizar la pantalla a mano** cada vez que cambiaban los datos:
crear el `<li>`, borrarlo, actualizar el contador, tachar… Con 3 cosas se puede. Con 300 es un caos.

**React** es una **librería** de JavaScript (creada por Meta/Facebook) para construir interfaces
que cambia esa forma de pensar:

| JavaScript puro (imperativo) | React (declarativo) |
|---|---|
| **Cómo** cambiar la pantalla paso a paso | **Cómo tiene que verse** según los datos |
| "Creá un `li`, agregalo, actualizá el contador…" | "Hay 3 tareas → mostrá 3 `li` y el número 3" |
| Vos sincronizás datos y pantalla | **React sincroniza solo** cuando cambian los datos |

> 🎨 Es la diferencia entre darle a alguien instrucciones para **pintar** cada pincelada, o darle
> una **foto** y decirle "que quede así". React se encarga de las pinceladas.

La idea central: **la interfaz es una función de los datos**.

```
datos (estado)  ──►  React  ──►  lo que se ve
```

---

## 2 · Crear un proyecto con Vite

**Vite** es una herramienta que crea y ejecuta proyectos de React (usa Node por dentro).

```bash
npm create vite@latest mi-app -- --template react
cd mi-app
npm install
npm run dev
```

Abrí la dirección que aparece (casi siempre http://localhost:5173). ¡Tu primera app de React! 🎉
(Si Vite te hace alguna pregunta extra, elegí la opción por defecto.)

### Qué hay adentro

```
mi-app/
├── index.html        ← la ÚNICA página HTML. Tiene un <div id="root"></div> vacío
├── package.json
└── src/
    ├── main.jsx      ← arranca React y lo "monta" dentro de #root
    ├── App.jsx       ← el componente principal ⭐ acá empezás a trabajar
    └── App.css
```

`.jsx` = JavaScript con JSX adentro (ahora vemos qué es).

---

## 3 · Componentes: piezas de Lego 🧱

Un **componente** es una **función que devuelve lo que se ve**. La interfaz se arma combinando componentes,
como piezas de Lego.

```jsx
function Saludo() {
  return <h1>¡Hola!</h1>;
}

export default function App() {
  return (
    <main>
      <Saludo />
      <Saludo />
    </main>
  );
}
```

Reglas:
- El nombre **empieza con mayúscula**: `Saludo`, no `saludo` (en minúscula React cree que es una etiqueta HTML).
- Se usan como etiquetas: `<Saludo />`.
- Un componente por archivo, en general: `src/components/Tarjeta.jsx`.

```
App
├── Encabezado
├── ListaDeTareas
│   ├── Tarea
│   ├── Tarea
│   └── Tarea
└── Pie
```
¡Otra vez **el árbol**! Como las carpetas y como el HTML. 🌳

---

## 4 · JSX: HTML adentro de JavaScript

**JSX** parece HTML, pero está dentro de JavaScript. Tiene algunas diferencias:

| HTML | JSX | Por qué |
|---|---|---|
| `class="..."` | `className="..."` | `class` es palabra reservada de JS |
| `for="..."` | `htmlFor="..."` | ídem |
| `<img>` | `<img />` | En JSX **todo** se cierra |
| `onclick="..."` | `onClick={funcion}` | Eventos en camelCase, con una **función** |
| `style="color: red"` | `style={{ color: "red" }}` | El estilo es un **objeto** |

### Llaves `{ }`: "acá va JavaScript"

```jsx
const nombre = "Ana";
const tareas = 3;

return (
  <p>
    Hola {nombre}, tenés {tareas} tareas. {tareas > 5 ? "¡Uf!" : "Tranqui"}
  </p>
);
```

Adentro de las llaves va **una expresión** (algo que da un valor): variables, cuentas, ternarios, `map`…
**No** va un `if` ni un `for` (para eso usás ternarios y `map`).

### Devolver un solo elemento padre

```jsx
// ❌ Dos elementos sueltos
return (
  <h1>Hola</h1>
  <p>Chau</p>
);

// ✅ Envueltos. <> </> es un "fragmento": envuelve sin agregar nada al HTML
return (
  <>
    <h1>Hola</h1>
    <p>Chau</p>
  </>
);
```

---

## 5 · Props: pasarle datos a un componente

Las **props** (propiedades) son los datos que un componente **recibe de su padre**.
Son como los **parámetros** de una función (¡porque un componente **es** una función!).

```jsx
function Tarjeta({ titulo, precio }) {     // desestructuración de las props
  return (
    <article className="tarjeta">
      <h2>{titulo}</h2>
      <p>${precio}</p>
    </article>
  );
}

export default function App() {
  return (
    <>
      <Tarjeta titulo="Remera" precio={15000} />
      <Tarjeta titulo="Gorra" precio={8000} />
    </>
  );
}
```

- Texto: entre comillas `titulo="Remera"`. Cualquier otra cosa: entre llaves `precio={15000}`.
- Las props son de **solo lectura**: el hijo **no las puede cambiar**.
- Los datos **bajan** del padre al hijo. ⬇️

---

## 6 · Listas: `map` + `key`

```jsx
const productos = [
  { id: 1, nombre: "Remera" },
  { id: 2, nombre: "Gorra" },
];

return (
  <ul>
    {productos.map((producto) => (
      <li key={producto.id}>{producto.nombre}</li>
    ))}
  </ul>
);
```

Cada elemento de una lista necesita una prop **`key` única** (normalmente el `id`), para que React
sepa cuál es cuál cuando la lista cambia. Si te olvidás, aparece un aviso en la consola.

---

## 7 · Estado (`useState`): la memoria del componente 🧠

Las variables normales **se reinician** cada vez que React vuelve a dibujar el componente, y cambiarlas
**no actualiza la pantalla**. Para datos que **cambian** y se tienen que **ver**, se usa **estado**:

```jsx
import { useState } from "react";

function Contador() {
  const [cuenta, setCuenta] = useState(0);
  //     └ valor  └ función para cambiarlo   └ valor inicial

  return (
    <div>
      <p>Clics: {cuenta}</p>
      <button onClick={() => setCuenta(cuenta + 1)}>Sumar</button>
    </div>
  );
}
```

Qué pasa al hacer clic:
1. Llamás a `setCuenta(1)`.
2. React guarda el nuevo valor y **vuelve a ejecutar** la función `Contador`.
3. Ahora `cuenta` vale 1, el JSX muestra 1, y React actualiza **solo lo que cambió** en la pantalla. ✨

### ⚠️ Las 3 reglas del estado

1. **Nunca lo modifiques directo.** Siempre con la función `set…`:
   ```jsx
   cuenta = cuenta + 1;          // ❌ no pasa nada
   setCuenta(cuenta + 1);        // ✅
   ```
2. **Con arrays y objetos, creá uno nuevo** (¡acá sirve el spread!):
   ```jsx
   tareas.push(nueva);                    // ❌ React no se entera
   setTareas([...tareas, nueva]);         // ✅ agregar
   setTareas(tareas.filter(t => t.id !== id));   // ✅ borrar
   setTareas(tareas.map(t => t.id === id ? { ...t, hecha: !t.hecha } : t));  // ✅ modificar
   ```
3. **Los hooks** (`useState`, `useEffect`…) van **al principio del componente**, nunca dentro de un `if` o un bucle.

### Props vs estado

| Props | Estado |
|---|---|
| Vienen **de afuera** (del padre) | Vive **adentro** del componente |
| **No** se pueden cambiar | **Se cambia** con `set…` |
| Como los parámetros de una función | Como la memoria del componente |

### ¿Y si un hijo necesita cambiar el estado del padre?

El padre le pasa una **función** por props. Los datos bajan ⬇️ y los eventos suben ⬆️:

```jsx
function Tarea({ tarea, onBorrar }) {
  return (
    <li>
      {tarea.texto}
      <button onClick={() => onBorrar(tarea.id)}>🗑️</button>
    </li>
  );
}

function Lista() {
  const [tareas, setTareas] = useState([]);
  const borrar = (id) => setTareas(tareas.filter(t => t.id !== id));

  return tareas.map(t => <Tarea key={t.id} tarea={t} onBorrar={borrar} />);
}
```

---

## 8 · Formularios controlados

El valor de un input vive en el **estado**, y el input siempre muestra ese estado:

```jsx
function Formulario() {
  const [texto, setTexto] = useState("");

  const enviar = (evento) => {
    evento.preventDefault();       // ¡como en JS puro!
    console.log("Enviado:", texto);
    setTexto("");                  // vaciar el input
  };

  return (
    <form onSubmit={enviar}>
      <input value={texto} onChange={(e) => setTexto(e.target.value)} />
      <button>Agregar</button>
    </form>
  );
}
```

---

## 9 · Efectos (`useEffect`): hacer algo "además" de dibujar

Algunas cosas no son "dibujar": **pedir datos a una API**, guardar en `localStorage`, poner un temporizador.
Eso son **efectos** y van en `useEffect`:

```jsx
import { useState, useEffect } from "react";

function Usuarios() {
  const [usuarios, setUsuarios] = useState([]);
  const [cargando, setCargando] = useState(true);
  const [error, setError] = useState(null);

  useEffect(() => {
    async function cargar() {
      try {
        const res = await fetch("https://jsonplaceholder.typicode.com/users");
        if (!res.ok) throw new Error(`Error ${res.status}`);
        setUsuarios(await res.json());
      } catch (e) {
        setError(e.message);
      } finally {
        setCargando(false);
      }
    }
    cargar();
  }, []);   // ← [] = "ejecutá esto UNA sola vez, cuando el componente aparece"

  if (cargando) return <p>Cargando…</p>;
  if (error) return <p>Hubo un error: {error}</p>;

  return (
    <ul>
      {usuarios.map(u => <li key={u.id}>{u.name}</li>)}
    </ul>
  );
}
```

El segundo argumento (el array de **dependencias**) dice **cuándo** se vuelve a ejecutar:

| Dependencias | Se ejecuta… |
|---|---|
| `[]` | Una vez, al aparecer el componente |
| `[tareas]` | Al aparecer y cada vez que cambia `tareas` (ej. guardar en `localStorage`) |
| (sin array) | Después de **cada** dibujo. Casi nunca es lo que querés ⚠️ |

> ⚠️ **Bucle infinito clásico:** un `useEffect` sin dependencias que hace `setAlgo` → redibuja →
> se ejecuta el efecto → `setAlgo` → redibuja… Si la página se cuelga, revisá tus efectos.

**Regla de oro:** si podés calcular algo a partir del estado o las props, **calculalo directamente**
en el componente. `useEffect` es solo para sincronizarse con cosas **de afuera** de React.

```jsx
const pendientes = tareas.filter(t => !t.hecha).length;   // ✅ calculado, sin efecto ni estado extra
```

---

## 10 · Herramientas

- **React Developer Tools**: extensión del navegador que agrega a F12 las pestañas *Components* y *Profiler*.
  Muestra el árbol de componentes con sus props y su estado. ⭐ Instalala.
- **Documentación oficial en español**: https://es.react.dev/ — tiene un tutorial excelente
  ("Tutorial: Tres en línea") y la sección "Pensar en React", que es de lectura obligatoria.

---

## ✅ Autoevaluación

1. ¿Qué significa que React sea "declarativo"?
2. ¿Qué es un componente? ¿Por qué su nombre empieza con mayúscula?
3. Nombrá 3 diferencias entre HTML y JSX.
4. ¿Qué diferencia hay entre props y estado?
5. ¿Por qué `tareas.push(nueva)` no actualiza la pantalla? ¿Cómo se hace bien?
6. ¿Para qué sirve la `key` en una lista?
7. ¿Qué pasa si un `useEffect` tiene `[]` como dependencias? ¿Y si no tiene array?
8. Si un hijo quiere borrar un elemento del estado del padre, ¿cómo lo hace?
