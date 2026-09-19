# jsm-01 · Métodos de arrays, desestructuración y spread 🧰

- **Rama:** `jsm-01`
- 🧠 Leer antes: [JavaScript moderno · Conceptos clave](../../../docs/javascript-moderno/conceptos-clave.md) (secciones 1 a 5)
- 📚 De apoyo: [javascript.info — Métodos de arrays](https://es.javascript.info/array-methods), [Desestructuración](https://es.javascript.info/destructuring-assignment)

## Consigna

Mismo formato que en la etapa 1 (`index.html` + `script.js`, resultados en la consola).
Copiá estos datos al principio de tu `script.js`:

```js
const alumnas = [
  { id: 1, nombre: "Ana",   edad: 19, notas: [8, 9, 7],  ciudad: "Rosario" },
  { id: 2, nombre: "Luz",   edad: 22, notas: [4, 5, 6],  ciudad: "Córdoba" },
  { id: 3, nombre: "Sol",   edad: 18, notas: [10, 9, 10], ciudad: "Rosario" },
  { id: 4, nombre: "Mora",  edad: 25, notas: [6, 3, 5],  ciudad: "Mendoza" },
  { id: 5, nombre: "Delfi", edad: 20, notas: [7, 7, 8],  ciudad: "Córdoba" },
];
```

**Sin usar ningún `for`**, resolvé con `map`, `filter`, `find`, `some`, `every` y `reduce`:

1. Un array solo con los **nombres**.
2. Las alumnas de **Rosario**.
3. La alumna con **id 4**.
4. ¿Hay **alguna** menor de 19? ¿Son **todas** mayores de 17?
5. La **suma de las edades** y el **promedio de edad**.
6. Escribí `promedio(numeros)` con `reduce` y usala para crear un array nuevo donde cada alumna
   tenga además una propiedad `promedio` (pista: `map` + spread `{ ...alumna, promedio: ... }`).
7. Con el array del punto 6: las **aprobadas** (promedio ≥ 6), **ordenadas** de mayor a menor promedio
   (investigá `toSorted` en MDN).
8. Usá **desestructuración** en los parámetros: `presentar({ nombre, ciudad })` → `"Ana, de Rosario"`.
   Mostrá la presentación de todas con `map`.
9. **Sin modificar** el array original, creá:
   - uno con una alumna nueva agregada al final
   - uno sin la alumna de id 2
   - uno donde la alumna de id 3 tenga `ciudad: "Santa Fe"`

   Al final, mostrá `alumnas` y comprobá que **sigue igual**.

## ✅ Checklist
- [ ] Ningún `for` ni `while` en todo el archivo
- [ ] Usaste los 6 métodos de arrays
- [ ] El array original no se modificó
- [ ] Usaste spread para copiar arrays y objetos
