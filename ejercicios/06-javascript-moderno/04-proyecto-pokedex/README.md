# jsm-04 · Mini proyecto: Pokédex 🔴⚪

- **Rama:** `jsm-04`

Una app para buscar Pokémon usando una API real y pública: [PokeAPI](https://pokeapi.co/).

## Probá la API primero

- https://pokeapi.co/api/v2/pokemon/pikachu
- https://pokeapi.co/api/v2/pokemon?limit=20

Es mucha información: buscá en el JSON dónde están el **nombre**, la **imagen** (`sprites`),
los **tipos** (`types`) y las **estadísticas** (`stats`). Leer JSON ajeno y encontrar lo que necesitás
es una habilidad que vas a usar siempre.

## Consigna

Organizá el código en **módulos** (como en jsm-02), por ejemplo:
`api.js` (los `fetch`), `ui.js` (lo que dibuja en la página), `main.js` (conecta todo).

### Nivel 1
- Un buscador: escribís un nombre, apretás "Buscar" y aparece una tarjeta con imagen, nombre, número y tipos.
- Si el Pokémon no existe (la API responde `404`), mostrá "No encontré ese Pokémon 😢".
- Mientras carga, mostrá un indicador.
- El nombre se busca en minúsculas aunque lo escribas con mayúsculas.

### Nivel 2
- Al abrir la página, mostrá una grilla con los primeros 20 Pokémon (nombre e imagen).
  Pista: `/pokemon?limit=20` te da nombres y URLs; para cada uno hay que pedir su detalle.
  Investigá `Promise.all` para hacer los 20 pedidos **a la vez** en lugar de uno por uno.
- Al hacer clic en uno de la grilla, se muestra su tarjeta con estadísticas.

### Nivel 3 (desafío ⭐)
- Botones "Anterior" / "Siguiente" para paginar de a 20.
- Filtrar la grilla por tipo.

## ✅ Checklist
- [ ] Código dividido en al menos 3 módulos
- [ ] Manejo de errores y de "cargando"
- [ ] Usaste `Promise.all`
- [ ] Usaste `map`/`filter` en vez de `for`
- [ ] Se ve bien en el celular
