# jsm-02 · Módulos: dividir el código en archivos 🧩

- **Rama:** `jsm-02`
- 🧠 Leer antes: [JavaScript moderno · Conceptos clave](../../../docs/javascript-moderno/conceptos-clave.md) (sección 6)
- 📚 De apoyo: [javascript.info — Módulos](https://es.javascript.info/modules-intro)

## Consigna

Vas a rehacer la **calculadora de propinas y la biblioteca** de la etapa 1, pero bien organizadas en módulos.

Estructura de `solucion/`:

```
solucion/
├── index.html
├── main.js
├── utils/
│   ├── numeros.js
│   └── textos.js
└── datos/
    └── libros.js
```

1. **`utils/numeros.js`** exporta (con nombre):
   - `sumar(a, b)`, `promedio(numeros)`, `redondear(numero, decimales)`
   - `formatearPesos(numero)` → `"$ 12.500,00"` (investigá `toLocaleString("es-AR", ...)` en MDN)
2. **`utils/textos.js`** exporta:
   - `capitalizar(texto)` → `"hola"` → `"Hola"`
   - `contarPalabras(texto)`
   - por defecto (`export default`): `saludar(nombre)`
3. **`datos/libros.js`** exporta por defecto un array de al menos 5 libros (`{ id, titulo, autor, anio, precio }`).
4. **`main.js`** importa todo lo necesario y muestra en la consola:
   - Todos los libros con su precio formateado en pesos
   - El precio promedio
   - Los títulos capitalizados
5. En `index.html` cargá **solo** `main.js` con `type="module"`.
6. Abrilo con **Live Server** (con doble clic no funciona: ¿por qué? Mirá la consola y contalo en el PR).

## ✅ Checklist
- [ ] Usaste exportaciones con nombre **y** por defecto
- [ ] Las rutas de los `import` empiezan con `./` o `../` y terminan en `.js`
- [ ] El HTML carga un solo script
