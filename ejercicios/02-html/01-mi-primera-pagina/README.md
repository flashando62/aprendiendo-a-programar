# html-01 · Mi primera página 🌐

- **Rama:** `html-01`
- 🧠 Leer antes: [HTML · Conceptos clave](../../../docs/html/conceptos-clave.md) (¡importante!)
- 📚 De apoyo: [MDN — Primeros pasos con HTML](https://developer.mozilla.org/es/docs/Learn/HTML/Introduction_to_HTML/Getting_started)

## Un poquito de teoría

HTML funciona con **etiquetas**: palabras entre `< >` que envuelven el contenido y dicen qué es.

```html
<p>Esto es un párrafo</p>
```

- `<p>` abre la etiqueta
- `</p>` la cierra (fijate la barra `/`)
- Lo del medio es el contenido

Toda página HTML tiene este esqueleto:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8">
    <title>El título que aparece en la pestaña</title>
  </head>
  <body>
    Lo que se ve en la página va acá.
  </body>
</html>
```

| Parte | Para qué |
|---|---|
| `<!DOCTYPE html>` | Le dice al navegador "esto es HTML moderno" |
| `<html lang="es">` | Envuelve todo. `lang="es"` = está en español |
| `<head>` | Info *sobre* la página (no se ve) |
| `<meta charset="UTF-8">` | Para que se vean bien las tildes y la ñ |
| `<title>` | El texto de la pestaña del navegador |
| `<body>` | Todo lo que **sí** se ve |

## Consigna

1. Creá `solucion/index.html`.
2. **Escribí** (sin copiar y pegar) el esqueleto de arriba.
3. Poné tu nombre en el `<title>`.
4. Dentro del `<body>`:
   - Un título principal con `<h1>`: *"Hola, soy [tu nombre]"*
   - Dos párrafos con `<p>` contando algo sobre vos.
5. Abrilo con **Live Server** y mirá cómo queda.

> 💡 **Truco de VS Code:** en un archivo `.html` vacío escribí `!` y apretá `Tab`. ¡Aparece el esqueleto solo!
> Pero **esta primera vez escribilo a mano** para aprenderlo.

## Desafío extra ⭐
Hacé clic derecho en la página → **Ver código fuente**. ¿Reconocés lo que escribiste?
Después probá lo mismo en cualquier otra página web. 👀

## ✅ Checklist
- [ ] El archivo tiene `<!DOCTYPE html>`, `<html>`, `<head>` y `<body>`
- [ ] Se ve tu nombre en la pestaña del navegador
- [ ] Las tildes se ven bien
- [ ] Todas las etiquetas que abrís, las cerrás
