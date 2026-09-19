# 📅 Plan de aprendizaje

El curso tiene **dos etapas**, dedicándole entre 1 y 2 horas por día, 5 días por semana:

| Etapa | Contenido | Duración |
|---|---|---|
| **1 · Fundamentos web** | Fundamentos, Git, HTML, CSS, JavaScript y un portfolio publicado | ~17 semanas |
| **2 · Full stack** | JavaScript moderno, Node.js, React y una app completa propia | ~16 semanas |

Es una guía, no una carrera: si un tema lleva más tiempo, se toma más tiempo.

> 🧭 **Cómo usar este plan:** cada semana tiene *qué leer/ver*, *qué ejercicios hacer*
> y *qué tenés que saber al terminar*. Si al final de la semana podés responder que sí
> a todo lo de "Al terminar...", pasás a la siguiente.

---

# 🌱 Etapa 1 · Fundamentos web

## Módulo 0 · Fundamentos y preparación (Semana 0)

**Objetivo:** entender las bases que "todo el mundo da por sabidas" y dejar la compu lista para programar.
No te saltees esta semana: lo que aprendas acá lo vas a usar todos los días.

Leer **en este orden** (cada guía te lleva a la siguiente):

| Día | Qué |
|---|---|
| 1 | [Fundamentos 01 · Archivos y carpetas](docs/fundamentos/01-archivos-y-carpetas.md) y [02 · El teclado y los atajos](docs/fundamentos/02-teclado-y-atajos.md) |
| 2 | [Fundamentos 03 · Cómo funciona la web](docs/fundamentos/03-como-funciona-la-web.md) y [04 · ¿Qué es programar?](docs/fundamentos/04-que-es-programar.md) |
| 3 | [Git 00 · Instalar las herramientas](docs/git/00-preparar-la-compu.md) y [Fundamentos 05 · Visual Studio Code](docs/fundamentos/05-vs-code.md) |
| 4 | [Git 01 · La terminal sin miedo](docs/git/01-la-terminal.md) |
| 5 | [Fundamentos 08 · Cómo aprender y pedir ayuda](docs/fundamentos/08-aprender-y-pedir-ayuda.md) |

📖 Tené a mano el [Glosario](docs/fundamentos/09-glosario.md) durante todo el curso.

**Al terminar sabés:**
- [ ] Qué es una extensión de archivo y tenés las extensiones visibles en Windows
- [ ] Escribir `` < > { } [ ] ; " ' ` `` en tu teclado
- [ ] Explicar qué es un servidor, un navegador y una URL
- [ ] Explicar para qué sirven HTML, CSS y JavaScript
- [ ] Qué es un algoritmo y escribir pseudocódigo simple
- [ ] Abrir una carpeta en VS Code y crear archivos
- [ ] Abrir la terminal, moverte entre carpetas y ver qué archivos hay

---

## Módulo 1 · Git y GitHub (Semanas 1 y 2)

Git es la herramienta que usan **todos** los programadores del mundo para guardar el
historial de su código y trabajar en equipo. Lo aprendés primero porque lo vas a usar
para entregar cada ejercicio del curso.

### Semana 1
- Leer y practicar [guía 02](docs/git/02-que-es-git.md), [guía 03](docs/git/03-clonar-el-repo.md), [guía 04](docs/git/04-guardar-cambios.md) y [guía 05](docs/git/05-subir-y-bajar.md)
- Extra (muy recomendado, es un juego): [Learn Git Branching](https://learngitbranching.js.org/?locale=es_AR) — hacer los primeros 4 niveles

### Semana 2
- Leer [guía 06](docs/git/06-ramas-y-pull-requests.md) — la más importante
- Leer [Fundamentos 07 · Markdown](docs/fundamentos/07-markdown.md) (lo vas a usar en los ejercicios de Git)
- Ejercicio: [git-01 · Presentate (tu primer Pull Request)](ejercicios/01-git/01-presentate/)
- Ejercicio: [git-02 · Tu diario de aprendizaje](ejercicios/01-git/02-diario/)
- Ejercicio: [git-03 · Responder una revisión](ejercicios/01-git/03-responder-una-revision/)

**Al terminar sabés:**
- [ ] Qué es un repositorio, un commit, una rama y un Pull Request
- [ ] Usar `git status`, `git add`, `git commit`, `git push`, `git pull`
- [ ] Crear una rama, subirla y abrir un Pull Request en GitHub

---

## Módulo 2 · HTML (Semanas 3 a 5)

HTML es el **esqueleto** de una página web: dice qué hay (un título, un párrafo, una imagen)
pero no cómo se ve.

- 🧠 **Empezá por acá:** [HTML · Conceptos clave](docs/html/conceptos-clave.md) (elementos, atributos, anidación, bloque vs en línea)
- 📚 Material de apoyo: [MDN — Introducción a HTML](https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML)

| Semana | Temas | Ejercicios |
|---|---|---|
| 3 | Qué es HTML, etiquetas, estructura de un documento, títulos y párrafos | [html-01](ejercicios/02-html/01-mi-primera-pagina/), [html-02](ejercicios/02-html/02-textos/) |
| 4 | [Rutas de archivos](docs/fundamentos/06-rutas-de-archivos.md), listas, enlaces, imágenes, tablas | [html-03](ejercicios/02-html/03-listas-enlaces-imagenes/), [html-04](ejercicios/02-html/04-tablas/) |
| 5 | Formularios, HTML semántico | [html-05](ejercicios/02-html/05-formularios/), [html-06 · Mini proyecto](ejercicios/02-html/06-proyecto-pagina-personal/) |

**Al terminar sabés:**
- [ ] Explicar qué es un elemento, una etiqueta y un atributo
- [ ] Dibujar el árbol (padres, hijos, hermanos) de una página simple
- [ ] La diferencia entre elementos de bloque y en línea
- [ ] Escribir rutas relativas, incluidas las que usan `../`
- [ ] Armar una página con la estructura `<!DOCTYPE html>`, `<head>` y `<body>`
- [ ] Usar títulos, párrafos, listas, enlaces, imágenes y tablas
- [ ] Hacer un formulario simple
- [ ] Usar etiquetas semánticas: `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`

---

## Módulo 3 · CSS (Semanas 6 a 9)

CSS es la **ropa** de la página: colores, tipografías, tamaños y dónde va cada cosa.

- 🧠 **Empezá por acá:** [CSS · Conceptos clave](docs/css/conceptos-clave.md) (cascada, herencia, especificidad, unidades, colores, display)
- 📚 Material de apoyo: [MDN — Aprende a dar estilo con CSS](https://developer.mozilla.org/es/docs/Learn/CSS)

| Semana | Temas | Ejercicios |
|---|---|---|
| 6 | Cómo conectar CSS, selectores, colores, textos | [css-01](ejercicios/03-css/01-primeros-estilos/), [css-02](ejercicios/03-css/02-selectores/) |
| 7 | El modelo de caja (margin, border, padding) | [css-03](ejercicios/03-css/03-modelo-de-caja/) |
| 8 | Flexbox y Grid para ubicar elementos | [css-04](ejercicios/03-css/04-flexbox/), [css-05](ejercicios/03-css/05-grid/) |
| 9 | Diseño responsive (que se vea bien en el celular) + mini proyecto | [css-06 · Mini proyecto](ejercicios/03-css/06-proyecto-estilos-pagina-personal/) |

🎮 Juegos para practicar:
- [Flexbox Froggy](https://flexboxfroggy.com/#es) (semana 8)
- [Grid Garden](https://cssgridgarden.com/#es) (semana 8)

**Al terminar sabés:**
- [ ] Conectar un archivo `.css` a un `.html`
- [ ] Usar selectores por etiqueta, clase e id
- [ ] Explicar qué regla gana cuando dos se contradicen (especificidad y orden)
- [ ] Usar `px`, `%` y `rem` sabiendo cuándo conviene cada una
- [ ] Encontrar por qué un estilo no se aplica usando F12
- [ ] Explicar qué es margin, border y padding
- [ ] Ubicar elementos con Flexbox y con Grid
- [ ] Usar una media query para adaptar la página al celular

---

## Módulo 4 · JavaScript (Semanas 10 a 15)

JavaScript es el **cerebro** de la página: hace que las cosas pasen cuando tocás un botón,
calcula, decide y cambia la página en vivo. Acá empieza la programación "de verdad":
variables, condiciones, repeticiones y funciones.

- 🧠 **Empezá por acá:** [JavaScript · Conceptos clave](docs/javascript/conceptos-clave.md) (orden de ejecución, tipos, variables, errores, debugging)
y releé [¿Qué es programar?](docs/fundamentos/04-que-es-programar.md)
- 📚 Material de apoyo: [MDN — Primeros pasos con JavaScript](https://developer.mozilla.org/es/docs/Learn/JavaScript/First_steps)
y [javascript.info en español](https://es.javascript.info/)

| Semana | Temas | Ejercicios |
|---|---|---|
| 10 | Qué es programar, la consola, variables y tipos de datos | [js-01](ejercicios/04-javascript/01-variables/) |
| 11 | Condicionales (`if`, `else`) y operadores | [js-02](ejercicios/04-javascript/02-condicionales/) |
| 12 | Bucles (`for`, `while`) | [js-03](ejercicios/04-javascript/03-bucles/) |
| 13 | Funciones | [js-04](ejercicios/04-javascript/04-funciones/) |
| 14 | Arrays y objetos | [js-05](ejercicios/04-javascript/05-arrays-y-objetos/) |
| 15 | El DOM y los eventos: JavaScript + HTML | [js-06](ejercicios/04-javascript/06-dom-y-eventos/), [js-07 · Mini proyecto](ejercicios/04-javascript/07-proyecto-lista-de-tareas/) |

**Al terminar sabés:**
- [ ] Escribir pseudocódigo antes de programar
- [ ] Leer un error de la consola y encontrar la línea que falla
- [ ] Usar `console.log` para investigar qué pasa en tu programa
- [ ] Declarar variables con `let` y `const`
- [ ] Tomar decisiones con `if` / `else`
- [ ] Repetir tareas con `for`
- [ ] Escribir y usar tus propias funciones
- [ ] Guardar listas de datos en arrays y recorrerlas
- [ ] Cambiar la página con JavaScript cuando alguien hace clic

---

## 🏁 Proyecto final de la Etapa 1 (Semana 16)

Juntás todo lo aprendido para hacer **tu portfolio personal** y publicarlo gratis en
internet con GitHub Pages. Vas a tener un link para mostrarle a cualquiera.

👉 [Proyecto final](ejercicios/05-proyecto-final/)

---
---

# 🚀 Etapa 2 · JavaScript moderno, Node.js y React

**Duración estimada: unas 16 semanas más.** Empezá **solo** cuando termines la Etapa 1 y te sientas
cómoda con JavaScript (funciones, arrays, objetos, DOM). Si en algún momento algo de la Etapa 2 no se entiende,
casi siempre la solución es **volver a repasar JavaScript**.

¿Por qué estas tecnologías?
- **Node.js** te deja usar el JavaScript que ya sabés **del lado del servidor**: vas a poder hacer tu propio backend.
- **React** es la herramienta más usada del mundo para hacer interfaces web. Es lo que más piden las ofertas de trabajo para frontend.
- Juntas, te permiten hacer una **aplicación completa (full stack)** con un solo lenguaje.

---

## Módulo 5 · JavaScript moderno y APIs (Semanas 17 a 20)

El "puente" hacia Node y React. Son herramientas de JavaScript que React y Node usan **en cada línea**.

- 🧠 **Empezá por acá:** [JavaScript moderno · Conceptos clave](docs/javascript-moderno/conceptos-clave.md)
- 📚 Material de apoyo: [javascript.info en español](https://es.javascript.info/) (partes de arrays, destructuring, módulos, promesas y async/await)

| Semana | Temas | Ejercicios |
|---|---|---|
| 17 | Funciones flecha, `map` / `filter` / `find` / `reduce`, desestructuración, spread | [jsm-01](ejercicios/06-javascript-moderno/01-arrays-y-desestructuracion/) |
| 18 | Módulos (`import` / `export`), JSON | [jsm-02](ejercicios/06-javascript-moderno/02-modulos/) |
| 19 | Asincronía, promesas, `async` / `await`, `fetch`, qué es una API | [jsm-03](ejercicios/06-javascript-moderno/03-async-y-fetch/) |
| 20 | Mini proyecto con una API real | [jsm-04 · Pokédex](ejercicios/06-javascript-moderno/04-proyecto-pokedex/) |

**Al terminar sabés:**
- [ ] Resolver problemas con `map`, `filter`, `find` y `reduce` en lugar de `for`
- [ ] Copiar y modificar arrays y objetos **sin** cambiar el original (spread)
- [ ] Dividir el código en módulos con `import` / `export`
- [ ] Explicar qué es una promesa y usar `async` / `await` con `try` / `catch`
- [ ] Pedir datos a una API con `fetch` y mostrarlos en la página
- [ ] Explicar qué es un endpoint, los métodos HTTP y los códigos de estado

---

## Módulo 6 · Node.js y Express (Semanas 21 a 24)

JavaScript fuera del navegador: tu primer **backend**.

- 🧠 **Empezá por acá:** [Node.js · Conceptos clave](docs/node/conceptos-clave.md)
- 📚 Material de apoyo: [Aprende Node.js (sitio oficial, en inglés)](https://nodejs.org/en/learn) y [Guía de Express en español](https://expressjs.com/es/)

| Semana | Temas | Ejercicios |
|---|---|---|
| 21 | Qué es Node, instalarlo, npm, `package.json`, leer y escribir archivos | [node-01](ejercicios/07-node/01-primeros-pasos/) |
| 22 | Servidor web con Express, rutas, parámetros, archivos estáticos | [node-02](ejercicios/07-node/02-servidor-express/) |
| 23 | API REST: CRUD, métodos HTTP, códigos de estado, probar con Thunder Client | [node-03](ejercicios/07-node/03-api-rest/) |
| 24 | Mini proyecto: API con datos que persisten | [node-04 · API de tareas](ejercicios/07-node/04-proyecto-api-tareas/) |

**Al terminar sabés:**
- [ ] Explicar la diferencia entre JavaScript en el navegador y en Node
- [ ] Usar npm: `init`, `install`, scripts, y saber por qué `node_modules` no se sube
- [ ] Crear un servidor con Express y rutas que respondan JSON
- [ ] Hacer un CRUD completo con validaciones y códigos de estado correctos
- [ ] Guardar datos en un archivo para que no se pierdan
- [ ] Explicar qué es CORS y activarlo

---

## Módulo 7 · React (Semanas 25 a 30)

Interfaces modernas con componentes.

- 🧠 **Empezá por acá:** [React · Conceptos clave](docs/react/conceptos-clave.md)
- 📚 Material de apoyo: [react.dev en español](https://es.react.dev/learn) ⭐ (la documentación oficial es excelente: hacé el tutorial "Tres en línea")

| Semana | Temas | Ejercicios |
|---|---|---|
| 25 | Qué es React, Vite, componentes, JSX, props, listas con `key` | [react-01](ejercicios/08-react/01-componentes-y-props/) |
| 26 | Estado con `useState`, eventos, pasar funciones por props | [react-02](ejercicios/08-react/02-estado-y-eventos/) |
| 27 | Formularios controlados, actualizar arrays en el estado, "Pensar en React" | [react-03](ejercicios/08-react/03-listas-y-formularios/) |
| 28 | `useEffect`, pedir datos a una API, cargando y errores | [react-04](ejercicios/08-react/04-efectos-y-fetch/) |
| 29–30 | Mini proyecto full stack: React + tu API de Node | [react-05 · Tareas full stack](ejercicios/08-react/05-proyecto-tareas-fullstack/) |

**Al terminar sabés:**
- [ ] Crear un proyecto con Vite y dividir la interfaz en componentes
- [ ] Pasar datos con props y explicar la diferencia con el estado
- [ ] Actualizar el estado correctamente (sin modificarlo directo)
- [ ] Hacer formularios controlados
- [ ] Usar `useEffect` para pedir datos, sabiendo cuándo **no** hace falta
- [ ] Conectar un frontend de React con tu propia API

---

## 🏆 Proyecto final de la Etapa 2 (Semanas 31 y 32)

Tu propia aplicación **full stack**, de una idea tuya, trabajando con ramas chicas y Pull Requests como en un equipo real.

👉 [Proyecto final · Etapa 2](ejercicios/09-proyecto-final-etapa-2/)

---

## ¿Y después?

Con las dos etapas terminadas tenés la base de una desarrolladora **junior**. Algunos caminos para seguir:
- **Bases de datos:** SQL (PostgreSQL, SQLite) o MongoDB, para reemplazar el archivo JSON
- **TypeScript:** JavaScript con tipos; muy pedido en el mercado
- **Testing:** escribir pruebas automáticas para tu código
- **Next.js:** un framework sobre React para apps más grandes
- **Autenticación:** usuarios, login y contraseñas de forma segura
- Seguir practicando con [freeCodeCamp en español](https://www.freecodecamp.org/espanol/) y construyendo **tus propios proyectos**
