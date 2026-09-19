# 📅 Plan de aprendizaje

Duración estimada: **unas 17 semanas** (una de fundamentos + 16 de contenido) dedicándole entre 1 y 2 horas por día, 5 días por semana.
Es una guía, no una carrera: si un tema lleva más tiempo, se toma más tiempo.

> 🧭 **Cómo usar este plan:** cada semana tiene *qué leer/ver*, *qué ejercicios hacer*
> y *qué tenés que saber al terminar*. Si al final de la semana podés responder que sí
> a todo lo de "Al terminar...", pasás a la siguiente.

---

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
