# 🏆 Proyecto final · Etapa 2: tu propia app full stack

- **Rama:** `proyecto-final-2` (y varias ramas más chicas: ver abajo)

Llegó el momento de hacer **tu propia aplicación**, de una idea tuya, de punta a punta.
Este es el proyecto que vas a mostrar en tu portfolio y en entrevistas. 💼

## 1 · Elegí una idea

Algo que **a vos** te sirva o te guste. Algunas ideas:

- 📚 **Mis lecturas:** libros que leí, que quiero leer, puntaje y reseña.
- 🍳 **Recetario:** recetas con ingredientes, pasos, filtro por categoría.
- 💸 **Gastos del mes:** anotar gastos por categoría y ver totales.
- 🎬 **Watchlist:** series y películas, con estado (viendo / vista / pendiente).
- 🏋️ **Registro de entrenamientos**, 🌱 **cuidado de plantas**, 🎮 **colección de juegos**…

## 2 · Requisitos

### Backend (Node + Express)
- [ ] API REST con CRUD completo de **al menos una entidad** (ej. libros)
- [ ] Validaciones y códigos de estado correctos
- [ ] Datos guardados en archivo JSON (o, si te animás, investigá una base de datos como SQLite)
- [ ] Código organizado en módulos (rutas, almacenamiento…)

### Frontend (React)
- [ ] Al menos 6 componentes, organizados en carpetas
- [ ] Listado, alta, edición y baja contra tu API
- [ ] Al menos un **filtro o búsqueda** y algún dato **calculado** (totales, promedios, contadores)
- [ ] Estados de cargando y error
- [ ] Diseño prolijo y **responsive**

### Git y documentación
- [ ] Trabajo en **ramas chicas por funcionalidad**, cada una con su Pull Request
      (ej. `api-crud-libros`, `listado-libros`, `formulario-alta`, `filtros`, `estilos`).
      Así trabaja un equipo de verdad.
- [ ] Un `README.md` con: qué es la app, capturas de pantalla, tecnologías usadas, cómo instalarla y ejecutarla,
      y la lista de endpoints de la API

## 3 · Cómo encararlo (paso a paso)

1. **Planificá (en papel):** qué datos vas a guardar, qué pantallas hay, qué componentes.
   Escribilo en un `PLAN.md` dentro de tu carpeta y mostráselo a tu mentor **antes** de programar.
2. **Backend primero:** hacé la API y probala con Thunder Client.
3. **Frontend de a poco:** primero el listado, después agregar, después borrar, después editar…
   Una funcionalidad por rama y por PR.
4. **Estilos al final**, cuando todo funcione.
5. **Pulí:** errores, mensajes vacíos ("Todavía no cargaste ningún libro"), responsive.

## 4 · Estructura sugerida

```
09-proyecto-final-etapa-2/
└── solucion/
    ├── README.md
    ├── PLAN.md
    ├── backend/      ← proyecto Node + Express
    └── frontend/     ← proyecto React (Vite)
```

## 5 · Extra: publicarlo en internet (desafío ⭐)

A diferencia de una página estática, un backend de Node **necesita un servidor que esté siempre prendido**.
GitHub Pages no alcanza. Hay servicios con planes gratuitos para proyectos personales (Render, Railway, Vercel, Netlify…);
investigá con tu mentor cuál conviene en ese momento. Vas a tener que aprender sobre variables de entorno y *builds*
(`npm run build` en Vite). ¡Es un gran aprendizaje!

---

🎓 **¡Felicitaciones!** Si llegaste hasta acá, sabés hacer una aplicación web completa: frontend, backend,
API, control de versiones con Git y trabajo con Pull Requests. Eso es exactamente lo que piden para un
puesto **junior**. Actualizá tu portfolio de la etapa 1 con este proyecto. 💜
