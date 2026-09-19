# 📅 Plan de aprendizaje

Duración estimada: **unas 16 semanas** dedicándole entre 1 y 2 horas por día, 5 días por semana.
Es una guía, no una carrera: si un tema lleva más tiempo, se toma más tiempo.

> 🧭 **Cómo usar este plan:** cada semana tiene *qué leer/ver*, *qué ejercicios hacer*
> y *qué tenés que saber al terminar*. Si al final de la semana podés responder que sí
> a todo lo de "Al terminar...", pasás a la siguiente.

---

## Módulo 0 · Preparación (Semana 1, primeros días)

**Objetivo:** dejar la compu lista para programar.

- Instalar Git, Visual Studio Code y crear la cuenta de GitHub → [guía 00](docs/git/00-preparar-la-compu.md)
- Aprender lo básico de la terminal → [guía 01](docs/git/01-la-terminal.md)

**Al terminar sabés:** abrir la terminal, moverte entre carpetas y ver qué archivos hay.

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

📚 Material principal: [MDN — Introducción a HTML](https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML)

| Semana | Temas | Ejercicios |
|---|---|---|
| 3 | Qué es HTML, etiquetas, estructura de un documento, títulos y párrafos | [html-01](ejercicios/02-html/01-mi-primera-pagina/), [html-02](ejercicios/02-html/02-textos/) |
| 4 | Listas, enlaces, imágenes, tablas | [html-03](ejercicios/02-html/03-listas-enlaces-imagenes/), [html-04](ejercicios/02-html/04-tablas/) |
| 5 | Formularios, HTML semántico | [html-05](ejercicios/02-html/05-formularios/), [html-06 · Mini proyecto](ejercicios/02-html/06-proyecto-pagina-personal/) |

**Al terminar sabés:**
- [ ] Armar una página con la estructura `<!DOCTYPE html>`, `<head>` y `<body>`
- [ ] Usar títulos, párrafos, listas, enlaces, imágenes y tablas
- [ ] Hacer un formulario simple
- [ ] Usar etiquetas semánticas: `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`

---

## Módulo 3 · CSS (Semanas 6 a 9)

CSS es la **ropa** de la página: colores, tipografías, tamaños y dónde va cada cosa.

📚 Material principal: [MDN — Aprende a dar estilo con CSS](https://developer.mozilla.org/es/docs/Learn/CSS)

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
- [ ] Explicar qué es margin, border y padding
- [ ] Ubicar elementos con Flexbox y con Grid
- [ ] Usar una media query para adaptar la página al celular

---

## Módulo 4 · JavaScript (Semanas 10 a 15)

JavaScript es el **cerebro** de la página: hace que las cosas pasen cuando tocás un botón,
calcula, decide y cambia la página en vivo. Acá empieza la programación "de verdad":
variables, condiciones, repeticiones y funciones.

📚 Material principal: [MDN — Primeros pasos con JavaScript](https://developer.mozilla.org/es/docs/Learn/JavaScript/First_steps)
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
- [ ] Declarar variables con `let` y `const`
- [ ] Tomar decisiones con `if` / `else`
- [ ] Repetir tareas con `for`
- [ ] Escribir y usar tus propias funciones
- [ ] Guardar listas de datos en arrays y recorrerlas
- [ ] Cambiar la página con JavaScript cuando alguien hace clic

---

## 🏁 Proyecto final (Semana 16)

Juntás todo lo aprendido para hacer **tu portfolio personal** y publicarlo gratis en
internet con GitHub Pages. Vas a tener un link para mostrarle a cualquiera.

👉 [Proyecto final](ejercicios/05-proyecto-final/)

---

## ¿Y después?

Cuando termines este plan, algunos caminos posibles:
- Profundizar JavaScript (promesas, `fetch`, consumir APIs)
- Aprender un framework como React
- Aprender backend (Node.js, bases de datos)
- Seguir con [freeCodeCamp en español](https://www.freecodecamp.org/espanol/) para practicar más
