# html-04 · Tablas 📊

**Rama:** `html-04`
📚 Leer antes: [MDN — Tablas en HTML](https://developer.mozilla.org/es/docs/Learn/HTML/Tables/Basics)

## Etiquetas nuevas

```html
<table>
  <thead>
    <tr>
      <th>Materia</th>
      <th>Nota</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Matemática</td>
      <td>8</td>
    </tr>
  </tbody>
</table>
```

| Etiqueta | Qué es |
|---|---|
| `<table>` | La tabla entera |
| `<thead>` / `<tbody>` | La cabecera / el cuerpo |
| `<tr>` | Una fila (*table row*) |
| `<th>` | Una celda de título (*table header*) |
| `<td>` | Una celda de datos (*table data*) |

> ⚠️ Las tablas son para **datos en filas y columnas**, no para acomodar el diseño de la página
> (para eso está CSS).

## Consigna

Creá `solucion/index.html` con **tu horario semanal ideal para estudiar programación**:

1. Un `<h1>` con el título.
2. Una tabla con:
   - Columnas: Día · Horario · Tema · ¿Cuánto tiempo?
   - Al menos 5 filas (una por día)
3. Agregá `border="1"` al `<table>` para que se vean las líneas (después lo haremos con CSS).

## Desafío extra ⭐
Investigá el atributo `colspan` y usalo para que una fila tenga una celda que ocupe todo el ancho
(por ejemplo, una fila *"Fin de semana: ¡descanso!"*).

## ✅ Checklist
- [ ] La tabla tiene `<thead>` y `<tbody>`
- [ ] Los títulos de columna usan `<th>`
- [ ] Cada fila tiene la misma cantidad de celdas (salvo si usás `colspan`)
