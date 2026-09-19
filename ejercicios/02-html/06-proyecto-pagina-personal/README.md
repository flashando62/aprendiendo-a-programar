# html-06 · Mini proyecto: tu página personal 🏠

- **Rama:** `html-06`
- 📚 Leer antes: [MDN — Estructura del documento y del sitio web](https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure)

## HTML semántico

En vez de usar etiquetas genéricas para todo, HTML tiene etiquetas que **dicen qué es cada parte**:

```html
<body>
  <header>   <!-- La cabecera: logo, nombre -->
    <nav>    <!-- El menú de navegación -->
    </nav>
  </header>

  <main>     <!-- El contenido principal (uno solo por página) -->
    <section>  <!-- Una sección temática -->
    </section>
    <article>  <!-- Un contenido independiente (ej. un post) -->
    </article>
  </main>

  <footer>   <!-- El pie: contacto, derechos -->
  </footer>
</body>
```

Se ve igual, pero ayuda a los buscadores (Google) y a los lectores de pantalla de personas ciegas.

## Consigna

Juntá todo lo aprendido en **una página personal** (que en el módulo de CSS vamos a poner linda 💅).

Creá `solucion/index.html` con:

1. **`<header>`** con tu nombre en `<h1>` y un `<nav>` con enlaces a las secciones de la página
   (pista: `<a href="#sobre-mi">` lleva a la sección que tenga `id="sobre-mi"`).
2. **`<main>`** con estas `<section>`:
   - **Sobre mí**: una foto y un par de párrafos.
   - **Mis gustos**: una lista de cosas que te gustan (música, series, deportes...).
   - **Lo que estoy aprendiendo**: una tabla con las tecnologías del curso y tu estado (✅ aprendido / 📖 aprendiendo / ⏳ pendiente).
   - **Contacto**: un formulario simple (nombre, email, mensaje).
3. **`<footer>`** con tu nombre, el año y un enlace a tu perfil de GitHub.

## ✅ Checklist
- [ ] Usaste `<header>`, `<nav>`, `<main>`, `<section>` y `<footer>`
- [ ] Los enlaces del menú llevan a cada sección
- [ ] Todas las imágenes tienen `alt`
- [ ] Validaste tu HTML en https://validator.w3.org/#validate_by_input (pegá tu código) y no hay errores

🎉 **¡Terminaste HTML!** Escribí en tu diario qué fue lo que más te gustó de este módulo.
