# node-03 · Una API REST completa (CRUD) 🔁

- **Rama:** `node-03`
- 🧠 Leer antes: [Node.js · Conceptos clave](../../../docs/node/conceptos-clave.md) (secciones 6 y 7) y
  la sección 9 de [JavaScript moderno](../../../docs/javascript-moderno/conceptos-clave.md) (métodos HTTP y códigos)

## ¿Qué es CRUD?

Casi todas las aplicaciones del mundo hacen 4 cosas con sus datos:

| Letra | Acción | Método HTTP |
|---|---|---|
| **C** | *Create* — Crear | `POST` |
| **R** | *Read* — Leer | `GET` |
| **U** | *Update* — Actualizar | `PUT` / `PATCH` |
| **D** | *Delete* — Borrar | `DELETE` |

Instagram, Mercado Libre, tu home banking: son CRUDs muy grandes. 😄

## Consigna

Hacé una API de **películas**, con los datos guardados en un array en memoria:

```js
let peliculas = [
  { id: 1, titulo: "Relatos salvajes", anio: 2014, vista: true },
  { id: 2, titulo: "El secreto de sus ojos", anio: 2009, vista: false },
];
let proximoId = 3;
```

| Método y ruta | Qué hace | Código de respuesta |
|---|---|---|
| `GET /api/peliculas` | Devuelve todas. Con `?vista=true` filtra | 200 |
| `GET /api/peliculas/:id` | Devuelve una | 200, o **404** si no existe |
| `POST /api/peliculas` | Crea una con el `titulo` y `anio` del cuerpo | **201**, o **400** si falta el título |
| `PATCH /api/peliculas/:id` | Modifica los campos que vengan en el cuerpo | 200 o 404 |
| `DELETE /api/peliculas/:id` | La borra | **204** (sin contenido) o 404 |

Recordá `app.use(express.json())` para poder leer `req.body`.

### Probar la API
Instalá la extensión **Thunder Client** en VS Code (o REST Client) y probá **cada** ruta,
incluidos los casos de error (id que no existe, POST sin título).
Sacá capturas y ponelas en el PR.

## Para pensar 🤔
Reiniciá el servidor. ¿Qué pasó con las películas que agregaste? ¿Por qué?
(Lo arreglamos en el próximo ejercicio.)

## ✅ Checklist
- [ ] Las 5 rutas funcionan
- [ ] Cada respuesta usa el código de estado correcto
- [ ] Los errores devuelven un JSON con un mensaje claro
- [ ] Probaste todo con Thunder Client (o similar)
