# js-05 · Arrays y objetos 🗂️

- **Rama:** `js-05`
- 📚 Leer antes: [javascript.info — Arrays](https://es.javascript.info/array), [Objetos](https://es.javascript.info/object)

## Arrays: listas de cosas

```js
const frutas = ["manzana", "banana", "naranja"];

console.log(frutas[0]);        // "manzana"  ⚠️ ¡se empieza a contar desde 0!
console.log(frutas.length);    // 3

frutas.push("kiwi");           // agrega al final
frutas.pop();                  // saca el último

// Recorrer
for (const fruta of frutas) {
  console.log(fruta);
}
```

Métodos muy útiles:
```js
const numeros = [5, 12, 8, 3];

numeros.includes(8);                 // true
numeros.filter(n => n > 6);          // [12, 8]      → los que cumplen
numeros.map(n => n * 2);             // [10, 24, 16, 6] → transforma cada uno
```

## Objetos: fichas con datos

```js
const alumna = {
  nombre: "Ana",
  edad: 18,
  cursos: ["HTML", "CSS"],
};

console.log(alumna.nombre);   // "Ana"
alumna.edad = 19;             // modificar
alumna.ciudad = "Rosario";    // agregar
```

### Juntos: una lista de objetos (lo más usado en la vida real)

```js
const productos = [
  { nombre: "Remera", precio: 15000 },
  { nombre: "Gorra",  precio: 8000 },
];

for (const producto of productos) {
  console.log(`${producto.nombre}: $${producto.precio}`);
}
```

## Consigna

1. **Lista de compras:** un array con 5 productos. Mostralos numerados (`1. Leche`), agregá uno, sacá el último y mostrá cuántos quedaron.
2. **Notas:** con `const notas = [7, 4, 9, 10, 6, 3, 8];` escribí funciones que devuelvan:
   - el promedio
   - la nota más alta (recorriendo el array, sin `Math.max`)
   - cuántas notas son aprobadas (≥ 6)
3. **Tu perfil:** un objeto con tu nombre, edad, ciudad y un array de hobbies. Mostrá una presentación usando sus datos.
4. **Biblioteca:** un array de al menos 5 libros, cada uno un objeto con `titulo`, `autor`, `anio` y `leido` (true/false).
   - Mostrá todos los libros con el formato `"Rayuela" de Julio Cortázar (1963) ✅`
   - Usá `filter` para mostrar solo los que no leíste
   - Escribí `buscarPorAutor(libros, autor)` que devuelva los libros de ese autor

## ✅ Checklist
- [ ] Recorriste arrays con `for...of`
- [ ] Usaste `push`, `length` y `filter`
- [ ] Creaste un array de objetos y accediste a sus propiedades
