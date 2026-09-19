# jsm-03 · Asincronía y `fetch`: pedirle datos a internet 🌐

- **Rama:** `jsm-03`
- 🧠 Leer antes: [JavaScript moderno · Conceptos clave](../../../docs/javascript-moderno/conceptos-clave.md) (secciones 7 a 9)
- 📚 De apoyo: [javascript.info — Async/await](https://es.javascript.info/async-await), [MDN — Usando Fetch](https://developer.mozilla.org/es/docs/Web/API/Fetch_API/Using_Fetch)

## La API que vamos a usar

[JSONPlaceholder](https://jsonplaceholder.typicode.com/) es una API **de práctica**, gratis y sin registro.
Abrí estas direcciones en el navegador para ver qué devuelven:

- https://jsonplaceholder.typicode.com/users
- https://jsonplaceholder.typicode.com/users/1
- https://jsonplaceholder.typicode.com/posts?userId=1

> 💡 Instalá una extensión del navegador para ver JSON lindo (buscá "JSON Viewer"),
> o usá Firefox, que ya lo muestra formateado.

## Consigna

### Parte 1 · Entender el orden (consola)
1. Escribí este código y **antes de ejecutarlo**, anotá en qué orden creés que se muestran los mensajes:
   ```js
   console.log("A");
   setTimeout(() => console.log("B"), 0);
   console.log("C");
   ```
   ¿Acertaste? Explicá en el PR por qué sale en ese orden.
2. Escribí `esperar(ms)`, que devuelva una promesa que se resuelve después de `ms` milisegundos
   (pista: `new Promise(resolve => setTimeout(resolve, ms))`). Usala con `await` para mostrar
   una cuenta regresiva de 3 a 1, un número por segundo.

### Parte 2 · Pedir datos y mostrarlos en la página
Hacé una página que:
1. Al cargar, muestre `"Cargando…"`.
2. Pida la lista de usuarios con `fetch` + `async/await`.
3. Muestre una **tarjeta por usuario** con nombre, email y ciudad (`address.city`).
4. Al hacer clic en una tarjeta, pida los **posts** de ese usuario (`/posts?userId=ID`) y los muestre debajo.
5. Si algo falla, muestre un mensaje de error amigable (no solo en la consola).
   Probalo: cambiá la URL por una que no exista. ¿Qué pasa?

## Para investigar 🔍
Abrí **F12 → Red** (*Network*) y recargá. Buscá el pedido a `/users`:
¿qué **método** usó? ¿qué **código de estado** devolvió? ¿cuánto tardó?

## ✅ Checklist
- [ ] Usaste `async`/`await` y `try`/`catch`
- [ ] Revisás `respuesta.ok` antes de usar los datos
- [ ] Hay un estado de "cargando" y uno de "error"
- [ ] Miraste los pedidos en la pestaña Red
