# node-02 · Tu primer servidor con Express 🖥️

- **Rama:** `node-02`
- 🧠 Leer antes: [Node.js · Conceptos clave](../../../docs/node/conceptos-clave.md) (sección 6)
- 📚 De apoyo: [Express — Hola mundo](https://expressjs.com/es/starter/hello-world.html)

## Consigna

En `solucion/`: `npm init -y`, agregá `"type": "module"`, un script `"dev": "node --watch index.js"`
y corré `npm install express`.

Creá `index.js` con un servidor en el puerto **3000** que tenga estas rutas:

| Método y ruta | Responde |
|---|---|
| `GET /` | Un texto: `"¡Bienvenida a mi servidor!"` |
| `GET /api/hora` | JSON con la hora actual: `{ "hora": "14:32:05" }` |
| `GET /api/sumar?a=5&b=3` | JSON con el resultado: `{ "resultado": 8 }` (ojo: los query params llegan como **texto**) |
| `GET /api/saludo/:nombre` | JSON: `{ "mensaje": "Hola, Ana" }` |
| `GET /api/dado` | JSON con un número al azar del 1 al 6 |

Además:
1. Si en `/api/sumar` falta `a` o `b`, o no son números, respondé con **código 400** y un JSON de error:
   `res.status(400).json({ error: "..." })`.
2. **Servir tu página:** creá una carpeta `public/` con un `index.html` (podés copiar tu página personal de la etapa 1)
   y agregá `app.use(express.static("public"))`. Ahora `http://localhost:3000` muestra tu página. ¿Qué pasó con la ruta `GET /`?
3. Mostrá en la terminal cada pedido que llega (método y ruta). Pista: un *middleware*:
   ```js
   app.use((req, res, next) => {
     console.log(req.method, req.url);
     next();
   });
   ```

## Para pensar 🤔
¿Qué es exactamente lo que acabás de construir? ¿Qué parte es el **cliente** y cuál el **servidor**?
Releé [Cómo funciona la web](../../../docs/fundamentos/03-como-funciona-la-web.md) y contalo en el PR con tus palabras.

## ✅ Checklist
- [ ] Todas las rutas funcionan desde el navegador
- [ ] `/api/sumar` devuelve 400 si faltan datos
- [ ] Sirve archivos estáticos desde `public/`
- [ ] Cada pedido aparece en la terminal
