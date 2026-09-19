# react-04 · Efectos y datos de una API: Pokédex en React 🔴⚪

- **Rama:** `react-04`
- 🧠 Leer antes: [React · Conceptos clave](../../../docs/react/conceptos-clave.md) (sección 9)
- 📚 De apoyo: [react.dev — Sincronizar con efectos](https://es.react.dev/learn/synchronizing-with-effects) y [Quizás no necesitas un efecto](https://es.react.dev/learn/you-might-not-need-an-effect)

## Consigna

Rehacé tu **Pokédex de jsm-04** en React (proyecto Vite en `solucion/`).
Podés reusar tu módulo `api.js` tal cual: ¡para eso sirven los módulos!

### Nivel 1
- Al abrir la app, se cargan los primeros 20 Pokémon en una grilla (`useEffect` con `[]`).
- Tres estados posibles, cada uno con su pantalla: **cargando**, **error** y **datos**.
- Un componente `TarjetaPokemon` que recibe el Pokémon por props.

### Nivel 2
- Un buscador por nombre. Al buscar, se muestra el detalle del Pokémon (imagen, tipos, estadísticas).
- Un filtro por tipo que filtra la grilla **ya cargada** (¿hace falta un `useEffect` para esto,
  o se puede calcular? Leé "Quizás no necesitas un efecto").

### Nivel 3 (desafío ⭐)
- Paginación con "Anterior" / "Siguiente": el efecto depende de la página actual (`[pagina]`).
- Extraé la lógica de cargar datos a un **hook propio**: `usePokemons(pagina)` que devuelva
  `{ pokemons, cargando, error }`. (Investigá "custom hooks" en react.dev.)

## ✅ Checklist
- [ ] Usaste `useEffect` con el array de dependencias correcto
- [ ] Hay pantallas de cargando y de error
- [ ] El filtrado se calcula, no usa un efecto
- [ ] Reutilizaste el módulo `api.js`
