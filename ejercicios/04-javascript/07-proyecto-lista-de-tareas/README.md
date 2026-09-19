# js-07 · Mini proyecto: lista de tareas ✅

**Rama:** `js-07`

El clásico proyecto con el que **todos** los programadores practicamos: una app para anotar tareas.

## Lo nuevo que vas a necesitar

### Crear elementos desde JavaScript

```js
const lista = document.querySelector("#lista");

const item = document.createElement("li");   // crea un <li> (todavía no está en la página)
item.textContent = "Comprar pan";
lista.appendChild(item);                     // ahora sí, lo agrega adentro de la lista
```

### Borrar un elemento
```js
item.remove();
```

### Que el formulario no recargue la página
```js
formulario.addEventListener("submit", (evento) => {
  evento.preventDefault();   // ¡importante! Sin esto, la página se recarga y perdés todo
  // ... tu código
});
```

### Guardar datos en el navegador (para el nivel 3)
```js
localStorage.setItem("tareas", JSON.stringify(tareas));       // guardar
const guardadas = JSON.parse(localStorage.getItem("tareas")); // leer
```

## Consigna

Hacelo **por niveles**. Hacé commit al terminar cada uno.

### Nivel 1 · Lo básico
- Un input y un botón "Agregar".
- Al agregar, la tarea aparece en una lista.
- No se pueden agregar tareas vacías.
- Después de agregar, el input se vacía.

### Nivel 2 · Interacción
- Al hacer clic en una tarea, se marca como **hecha** (tachada, con una clase CSS).
- Cada tarea tiene un botón 🗑️ para borrarla.
- Un contador arriba: `"3 tareas pendientes"`.

### Nivel 3 · Que no se pierda nada (desafío ⭐)
- Guardá las tareas en `localStorage` para que sigan ahí al recargar la página.
  (Pista: mantené un array de objetos `{ texto, hecha }` y cada vez que cambie, volvé a dibujar la lista y guardalo.)
- Botones para filtrar: Todas / Pendientes / Hechas.

### Diseño
Que se vea lindo 💅: usá todo lo que aprendiste de CSS. Y que funcione en el celular.

## ✅ Checklist
- [ ] Nivel 1 completo
- [ ] Nivel 2 completo
- [ ] (Opcional) Nivel 3
- [ ] Hay al menos un commit por nivel
- [ ] Sin errores en la consola
- [ ] Se ve bien en el celular

🎉 **¡Terminaste JavaScript!** Hiciste una aplicación real. Mostrásela a alguien. 😄
