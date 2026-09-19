# node-04 · Mini proyecto: API de tareas 📋

- **Rama:** `node-04`

Vas a construir el **backend** de una lista de tareas. En el módulo de React le vas a hacer el frontend,
y las dos partes van a hablar entre sí. 🤝 **Guardá bien este proyecto: lo vas a reusar.**

## Consigna

### Estructura sugerida
```
solucion/
├── package.json
├── index.js          ← crea el servidor y conecta las rutas
├── rutas.js          ← las rutas de /api/tareas (investigá express.Router)
├── almacen.js        ← leer y guardar las tareas en el archivo
└── datos/
    └── tareas.json
```

### Nivel 1 · CRUD
Cada tarea: `{ id, texto, hecha, creada }` (`creada` = fecha en formato ISO: `new Date().toISOString()`).

| Método y ruta | Qué hace |
|---|---|
| `GET /api/tareas` | Todas las tareas |
| `POST /api/tareas` | Crea una (solo recibe `texto`; `hecha` arranca en `false`) |
| `PATCH /api/tareas/:id` | Modifica `texto` y/o `hecha` |
| `DELETE /api/tareas/:id` | Borra una |

Con validaciones: el texto no puede estar vacío ni tener más de 200 caracteres (→ 400).

### Nivel 2 · Que no se pierda nada
Las tareas se guardan en `datos/tareas.json` (con `readFile` / `writeFile` de `node:fs/promises`):
cada cambio se escribe en el archivo, y al arrancar el servidor se leen de ahí.
Reiniciá el servidor y comprobá que las tareas siguen.

### Nivel 3 · Listo para el frontend
- Instalá y activá `cors` (vas a necesitarlo para React).
- `GET /api/tareas?estado=pendientes` o `?estado=hechas` para filtrar.
- El puerto se lee de una variable de entorno `PUERTO` (con 3000 por defecto). Creá un `.env.example`
  **(este sí se sube)** que muestre qué variables hacen falta, sin valores secretos.
- Un `README.md` en `solucion/` que explique cómo instalar y ejecutar el proyecto y qué rutas tiene.
  (Así se documenta una API de verdad.)

## ✅ Checklist
- [ ] CRUD completo con validaciones y códigos de estado correctos
- [ ] Los datos sobreviven a un reinicio
- [ ] CORS activado
- [ ] Código dividido en módulos
- [ ] README con instrucciones y lista de endpoints
- [ ] `node_modules` y `.env` **no** están en el commit

🎉 **¡Hiciste un backend!** Ya sabés de los dos lados de la web.
