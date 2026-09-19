# react-05 · Mini proyecto: lista de tareas full stack 🔗

- **Rama:** `react-05`

¡El momento de juntar las dos mitades! Vas a hacer el **frontend en React** para la **API de tareas**
que construiste en [node-04](../../07-node/04-proyecto-api-tareas/).

```
  🌐 React (Vite)                         🟩 Node + Express
  http://localhost:5173    ── fetch ──►   http://localhost:3000/api/tareas
  (lo que se ve)           ◄── JSON ───   (guarda los datos en tareas.json)
```

Una aplicación así, con frontend y backend propios, se llama **full stack**. 💪

## Cómo trabajar con los dos a la vez

Necesitás **dos terminales** abiertas (en VS Code: botón `+` del panel de la terminal):

```bash
# Terminal 1: el backend
cd ejercicios/07-node/04-proyecto-api-tareas/solucion
npm run dev
```

```bash
# Terminal 2: el frontend
cd ejercicios/08-react/05-proyecto-tareas-fullstack/solucion
npm run dev
```

## Consigna

Proyecto Vite en `solucion/`. Guardá la dirección de la API en un solo lugar:

```js
// src/api.js
const URL_API = "http://localhost:3000/api/tareas";

export async function obtenerTareas() { /* GET */ }
export async function crearTarea(texto) { /* POST */ }
export async function actualizarTarea(id, cambios) { /* PATCH */ }
export async function borrarTarea(id) { /* DELETE */ }
```

Para mandar datos con `fetch`:
```js
const res = await fetch(URL_API, {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({ texto }),
});
```

### Nivel 1
- Al abrir, muestra las tareas que vienen de la API (con cargando y error).
- Agregar una tarea → `POST` → cuando responde, se agrega al estado.
- Marcar como hecha → `PATCH`. Borrar → `DELETE`.
- **Recargá la página:** las tareas tienen que seguir ahí (¡están guardadas en el servidor!).

### Nivel 2
- Filtros Todas / Pendientes / Hechas y contador de pendientes.
- Editar el texto de una tarea (doble clic → se convierte en input → Enter guarda).
- Si el servidor está apagado, un mensaje claro: "No me puedo conectar con el servidor 🔌".
  (Probalo: frená el backend con `Ctrl + C`.)

### Nivel 3 (desafío ⭐)
- Mientras se guarda un cambio, deshabilitá los botones de esa tarea.
- Si el servidor rechaza una tarea (400), mostrá el mensaje de error que devuelve la API.

## Para investigar 🔍
Con la app abierta, mirá **F12 → Red**: ¿ves cada `GET`, `POST`, `PATCH` y `DELETE` con sus códigos?
Sacale una captura para el PR.

## ✅ Checklist
- [ ] Todo el CRUD funciona contra la API real
- [ ] Todos los `fetch` están en `src/api.js`
- [ ] Hay manejo de cargando y de errores (incluido servidor apagado)
- [ ] Los datos sobreviven a recargar la página
- [ ] Un `README.md` en `solucion/` explica cómo levantar backend y frontend

🎉 **¡Hiciste una aplicación full stack!** Esto ya es lo que se hace en un trabajo real.
