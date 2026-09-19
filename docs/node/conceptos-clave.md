# 🟩 Node.js · Conceptos clave

> 📌 Leé esto antes del ejercicio node-01.

---

## 1 · ¿Qué es Node.js?

Hasta ahora, JavaScript **solo corría dentro del navegador**. **Node.js** es un programa que permite
ejecutar JavaScript **directamente en tu compu**, fuera del navegador.

Eso cambia todo: con Node, JavaScript puede
- **Crear servidores** y APIs (¡el backend!).
- **Leer y escribir archivos** de tu disco.
- Hacer **herramientas** para programadores (como la que crea proyectos de React).

```
          JavaScript
          ┌────┴─────┐
    En el navegador    En Node.js
    (frontend)         (backend, herramientas)
    ✅ document        ❌ document  (no hay página)
    ✅ window, alert   ❌ alert
    ❌ leer archivos   ✅ leer archivos
    ❌ crear servidor  ✅ crear servidor
```

El **lenguaje es el mismo** (variables, funciones, `if`, `map`…). Lo que cambia es **qué herramientas
tenés a mano**: en Node no hay página, así que no hay `document` ni botones.

> Es como un chef 👩‍🍳: sabe cocinar igual en un restaurante que en su casa, pero los utensilios cambian.

---

## 2 · Instalar Node.js

1. Entrá a https://nodejs.org/ y descargá la versión **LTS** (*Long Term Support*: la estable y recomendada).
2. Instalá aceptando las opciones por defecto.
3. **Cerrá y volvé a abrir** Git Bash y VS Code (para que se enteren de que Node existe).
4. Comprobá:

```bash
node --version
npm --version
```

Tienen que aparecer dos números de versión. 🎉

> ⚠️ Usá **Git Bash** para los comandos de Node. Si usás PowerShell y te aparece
> *"la ejecución de scripts está deshabilitada"*, cambiá a Git Bash.

---

## 3 · Ejecutar un archivo

```js
// hola.js
console.log("¡Hola desde Node!");
```

```bash
node hola.js
```

El `console.log` ahora aparece **en la terminal**, no en F12. 

Para que se reinicie solo cada vez que guardás (como Live Server, pero para Node):

```bash
node --watch hola.js
```
(Para frenarlo: `Ctrl + C`.)

---

## 4 · npm y los paquetes 📦

Un **paquete** (o *librería*, *dependencia*) es código que escribió otra persona y que podés usar
en tu proyecto. Hay más de 2 millones, gratis. ¿Para qué reinventar la rueda?

**npm** (*Node Package Manager*) viene con Node y sirve para **instalar y administrar** paquetes.

### `package.json`: el DNI del proyecto

Todo proyecto de Node tiene un archivo `package.json` con su nombre, sus paquetes y sus comandos:

```bash
npm init -y      # crea un package.json con valores por defecto
```

```json
{
  "name": "mi-proyecto",
  "version": "1.0.0",
  "type": "module",
  "scripts": {
    "dev": "node --watch index.js"
  },
  "dependencies": {
    "express": "^5.1.0"
  }
}
```

| Campo | Para qué |
|---|---|
| `"type": "module"` | Para poder usar `import`/`export` (¡agregalo siempre!) |
| `"scripts"` | Atajos de comandos. `npm run dev` ejecuta `node --watch index.js` |
| `"dependencies"` | Los paquetes que usa el proyecto y su versión |

### Comandos de npm

| Comando | Qué hace |
|---|---|
| `npm install express` | Instala el paquete `express` y lo anota en `package.json` |
| `npm install` | Instala **todos** los paquetes que dice el `package.json` |
| `npm run dev` | Ejecuta el script llamado `dev` |
| `npm uninstall express` | Desinstala un paquete |

### `node_modules`: la carpeta que **nunca** se sube

Los paquetes se descargan en la carpeta `node_modules`. Puede pesar **cientos de megas**
(los paquetes usan otros paquetes, que usan otros…).

- ❌ **Nunca** la subas a Git. Ya está en el `.gitignore` del repo. 
- ✅ Se puede **regenerar** en cualquier momento con `npm install`, porque el `package.json` dice qué hay que bajar.
- Si clonás un proyecto (o hacés `git pull` y alguien agregó un paquete), corré `npm install`.
- Si algo anda muy raro: borrá `node_modules` y volvé a correr `npm install`. Arregla más cosas de las que parece. 😅

`package-lock.json` es un archivo que npm crea solo, con las versiones exactas instaladas. **Sí** se sube a Git, pero no lo edites a mano.

---

## 5 · Módulos en Node

Con `"type": "module"` en el `package.json`, usás `import`/`export` igual que en
[JavaScript moderno](../javascript-moderno/conceptos-clave.md):

```js
import express from "express";                 // un paquete de npm: solo el nombre
import { sumar } from "./matematica.js";       // un archivo tuyo: con ./ y con .js
import fs from "node:fs/promises";             // un módulo que viene con Node: node:
```

---

## 6 · Un servidor web con Express

**Express** es el paquete más popular para crear servidores y APIs con Node.

```js
// index.js
import express from "express";

const app = express();
const PUERTO = 3000;

app.use(express.json());   // para entender pedidos que mandan JSON

app.get("/", (req, res) => {
  res.send("¡Hola desde mi servidor!");
});

app.get("/api/saludo", (req, res) => {
  res.json({ mensaje: "Hola", hora: new Date().toLocaleTimeString() });
});

app.listen(PUERTO, () => {
  console.log(`Servidor escuchando en http://localhost:${PUERTO}`);
});
```

Abrí http://localhost:3000/api/saludo en el navegador: **¡tu propia API!** 🎉

| Cosa | Qué es |
|---|---|
| `app.get(ruta, función)` | "Cuando alguien pida **GET** a esta **ruta**, ejecutá esta función" |
| `req` (*request*) | El **pedido**: qué mandó el cliente (parámetros, cuerpo…) |
| `res` (*response*) | La **respuesta**: lo que le devolvés (`res.json(...)`, `res.status(404)`) |
| **Puerto** (`3000`) | Una "puerta" de tu compu. Cada servidor escucha en una distinta. Live Server usa la 5500 |

> El servidor **se queda corriendo** esperando pedidos (la terminal no te devuelve el `$`).
> Es normal. Para frenarlo: `Ctrl + C`.

### Datos que llegan en el pedido

```js
// Parámetro en la ruta: GET /api/productos/7
app.get("/api/productos/:id", (req, res) => {
  const id = Number(req.params.id);   // "7" → 7
  // ...
});

// Query string: GET /api/productos?categoria=remeras
app.get("/api/productos", (req, res) => {
  const categoria = req.query.categoria;   // "remeras"
});

// Cuerpo JSON: POST /api/productos  con { "nombre": "Gorra" }
app.post("/api/productos", (req, res) => {
  const { nombre } = req.body;
  // ...
  res.status(201).json(productoNuevo);
});
```

---

## 7 · Probar una API

El navegador solo hace pedidos **GET** desde la barra de direcciones. Para probar `POST`, `PUT` o `DELETE`:

- **Thunder Client** o **REST Client** (extensiones de VS Code) ⭐
- **`fetch`** desde la consola del navegador o desde tu frontend
- `curl` en la terminal:
  ```bash
  curl -X POST http://localhost:3000/api/tareas -H "Content-Type: application/json" -d '{"texto":"Estudiar"}'
  ```

---

## 8 · CORS: cuando el navegador bloquea tu propia API 🚧

Si tu página está en `http://localhost:5173` (React) y tu API en `http://localhost:3000`,
el navegador **bloquea** el pedido por seguridad, con un error rojo que menciona **CORS**.
Son "orígenes distintos" (distinto puerto = distinto origen).

La API tiene que **dar permiso** explícitamente. Con Express:

```bash
npm install cors
```
```js
import cors from "cors";
app.use(cors());
```

---

## 9 · Variables de entorno y secretos 🔒

Nunca escribas contraseñas o claves de APIs en el código: el repo es **público**.
Se guardan en un archivo `.env` (que **no se sube**; ya está en el `.gitignore`) y se leen con `process.env`:

```bash
# .env
PUERTO=3000
```
```bash
node --env-file=.env index.js
```
```js
const PUERTO = process.env.PUERTO ?? 3000;
```

---

## ✅ Autoevaluación

1. ¿Qué diferencia hay entre JavaScript en el navegador y en Node?
2. ¿Para qué sirve `package.json`? ¿Y `node_modules`? ¿Cuál se sube a Git?
3. ¿Qué hacés después de clonar un proyecto de Node?
4. En `app.get("/api/tareas/:id", (req, res) => {...})`, ¿dónde encontrás el id?
5. ¿Por qué tu API puede andar en el navegador pero fallar desde React con un error de CORS?
6. ¿Dónde guardás una contraseña que necesita tu servidor?
