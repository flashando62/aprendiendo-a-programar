# html-03 · Listas, enlaces e imágenes 🔗🖼️

**Rama:** `html-03`
📚 Leer antes:
- [MDN — Listas](https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML/HTML_text_fundamentals#listas)
- [MDN — Crear hipervínculos](https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks)
- [MDN — Imágenes en HTML](https://developer.mozilla.org/es/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML)

## Etiquetas nuevas

```html
<!-- Lista sin orden (con viñetas) -->
<ul>
  <li>Manzana</li>
  <li>Banana</li>
</ul>

<!-- Lista ordenada (con números) -->
<ol>
  <li>Primero</li>
  <li>Segundo</li>
</ol>

<!-- Enlace: href es la dirección -->
<a href="https://www.wikipedia.org">Ir a Wikipedia</a>

<!-- Enlace que abre en otra pestaña -->
<a href="https://www.wikipedia.org" target="_blank">Wikipedia</a>

<!-- Enlace a otra página tuya -->
<a href="otra-pagina.html">Ver otra página</a>

<!-- Imagen: no se cierra. alt describe la imagen (para personas ciegas y por si no carga) -->
<img src="img/mi-foto.jpg" alt="Foto mía en la playa" width="300">
```

Las cosas como `href`, `src`, `alt` se llaman **atributos**: le dan información extra a la etiqueta.

## Consigna

Mejorá la receta del ejercicio anterior (copiá tu `index.html` de html-02 a `solucion/` de este ejercicio):

1. Los ingredientes ahora van en una **lista sin orden** `<ul>`.
2. Los pasos de preparación van en una **lista ordenada** `<ol>` (podés sacar los `<h3>`).
3. Agregá una **imagen** del plato:
   - Creá la carpeta `solucion/img/` y guardá ahí una imagen (`.jpg` o `.png`, que pese menos de 500 KB).
   - Mostrala con `<img>` y un buen `alt`.
4. Agregá un **enlace** a un video o página de la receta, que abra en otra pestaña.
5. Creá una segunda página `solucion/sobre-mi.html` con algo sobre vos y
   **enlazá las dos páginas entre sí** (una a la otra y viceversa).

## ✅ Checklist
- [ ] Usaste `<ul>` y `<ol>` correctamente
- [ ] La imagen se ve y tiene `alt`
- [ ] Los nombres de archivos e imágenes están en minúscula, sin espacios ni tildes
- [ ] Podés ir de una página a la otra y volver haciendo clic
