# html-05 · Formularios 📝

**Rama:** `html-05`
📚 Leer antes: [MDN — Tu primer formulario](https://developer.mozilla.org/es/docs/Learn/Forms/Your_first_form)

## Etiquetas nuevas

```html
<form>
  <label for="nombre">Nombre:</label>
  <input type="text" id="nombre" name="nombre" required>

  <label for="email">Email:</label>
  <input type="email" id="email" name="email">

  <label for="mensaje">Mensaje:</label>
  <textarea id="mensaje" name="mensaje"></textarea>

  <button type="submit">Enviar</button>
</form>
```

- El `for` del `<label>` tiene que ser **igual** al `id` del `<input>`. Así, al hacer clic en el texto, se activa el campo.
- `required` = el campo es obligatorio.

Tipos de `<input>` útiles: `text`, `email`, `password`, `number`, `date`, `checkbox`, `radio`, `color`.

Listas desplegables:
```html
<label for="pais">País:</label>
<select id="pais" name="pais">
  <option value="ar">Argentina</option>
  <option value="uy">Uruguay</option>
</select>
```

## Consigna

Creá `solucion/index.html` con un **formulario de inscripción a un taller** (del tema que quieras) que tenga:

1. Nombre y apellido (texto, obligatorio)
2. Email (obligatorio)
3. Fecha de nacimiento (`date`)
4. Un `<select>` para elegir el turno: mañana / tarde / noche
5. Tres `radio` para el nivel: principiante / intermedio / avanzado
   (pista: todos con el mismo `name`)
6. Un `checkbox`: *"Acepto recibir novedades por email"*
7. Un `textarea`: *"¿Por qué querés hacer el taller?"*
8. Un botón *"Inscribirme"*

> El formulario todavía **no envía los datos a ningún lado** (eso necesita un servidor).
> Pero probá dejar un campo obligatorio vacío y apretar el botón: ¿qué pasa?

## ✅ Checklist
- [ ] Todos los campos tienen su `<label>` conectado con `for` / `id`
- [ ] Los campos obligatorios no dejan enviar si están vacíos
- [ ] Solo se puede elegir **un** nivel a la vez
