# react-03 · Listas y formularios: la lista de compras 🛒

- **Rama:** `react-03`
- 🧠 Leer antes: [React · Conceptos clave](../../../docs/react/conceptos-clave.md) (secciones 7 y 8), y repasá el spread en [JavaScript moderno](../../../docs/javascript-moderno/conceptos-clave.md)
- 📚 De apoyo: [react.dev — Actualizar arrays en el estado](https://es.react.dev/learn/updating-arrays-in-state) y [Pensar en React](https://es.react.dev/learn/thinking-in-react) ⭐

## Consigna

Una **lista de compras** en React (proyecto Vite en `solucion/`).

Cada producto: `{ id, nombre, cantidad, comprado }`. Para el `id` podés usar `crypto.randomUUID()`.

### Nivel 1
- Un formulario controlado con **nombre** y **cantidad** (número, mínimo 1) y un botón "Agregar".
- No se puede agregar un producto sin nombre.
- La lista muestra cada producto con un checkbox para marcarlo como **comprado** (tachado).
- Cada producto tiene un botón 🗑️ para borrarlo.
- Arriba: `"Faltan comprar 3 de 5 productos"` (¡calculado, no en un estado aparte!).

### Nivel 2
- Botones `+` y `−` en cada producto para cambiar la cantidad (sin bajar de 1).
- Filtros: **Todos / Pendientes / Comprados**.
- Botón "Borrar comprados".

### Nivel 3 (desafío ⭐)
- Guardar la lista en `localStorage` para que no se pierda al recargar
  (acá vas a necesitar `useEffect` con `[productos]` como dependencia: leé la sección 9 de la guía).

### Componentes sugeridos
Antes de programar, **dibujá en un papel** la interfaz y marcá con recuadros qué componentes hay
(como explica "Pensar en React"). Sacale una foto y ponela en el PR. 📸

```
App  (acá vive el estado: la lista y el filtro)
├── FormularioProducto
├── Filtros
├── Resumen
└── ListaProductos
    └── ItemProducto
```

## ✅ Checklist
- [ ] Agregar, borrar y modificar usan `[...]`, `filter` y `map` (nunca `push` ni modificar directo)
- [ ] El estado vive en un solo lugar y baja por props
- [ ] Nada que se pueda calcular está guardado en el estado
- [ ] Hiciste el dibujo de los componentes antes de programar
