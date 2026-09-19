# node-01 · Primeros pasos con Node y npm 🟩

- **Rama:** `node-01`
- 🧠 Leer antes: [Node.js · Conceptos clave](../../../docs/node/conceptos-clave.md) (secciones 1 a 5)

## Consigna

### Parte 1 · Instalar y ejecutar
1. Instalá Node.js (LTS) siguiendo la guía y comprobá `node --version` y `npm --version`.
2. En la carpeta `solucion/` creá `hola.js` con un `console.log` y ejecutalo con `node hola.js`.
3. Escribí `console.log(document)`. ¿Qué error aparece? Explicá en el PR por qué.

### Parte 2 · Tu primer proyecto con npm
Parada en `solucion/`:

1. Corré `npm init -y` y abrí el `package.json` que se creó.
2. Agregale `"type": "module"`.
3. Creá `index.js` que **importe** la función `formatearPesos` de un módulo tuyo `utils.js`
   (podés reusar el de jsm-02) y muestre algunos precios.
4. Agregá un script `"start": "node index.js"` y otro `"dev": "node --watch index.js"`.
   Probá `npm start` y `npm run dev` (cambiá algo y guardá: ¿se reinicia solo?).

### Parte 3 · Leer y escribir archivos
Node puede usar tu disco. Creá `notas.js` que:

1. Tenga un array de objetos con 3 notas `{ id, texto, fecha }`.
2. Lo guarde en `notas.json` con `writeFile` (de `node:fs/promises`) usando `JSON.stringify(notas, null, 2)`.
3. Lo vuelva a leer con `readFile`, lo convierta con `JSON.parse` y muestre cuántas notas hay.

```js
import { readFile, writeFile } from "node:fs/promises";
```

Abrí `notas.json` en VS Code: ¡lo creó tu programa! 🎉
(El `null, 2` hace que el JSON quede prolijo, con sangría. Probá sacarlo y mirá la diferencia.)

### Parte 4 · Tu primer paquete de npm
1. Instalá un paquete, por ejemplo `npm install dayjs` (para manejar fechas).
2. Leé su documentación en https://www.npmjs.com/package/dayjs y usalo para mostrar la fecha de hoy en formato `DD/MM/YYYY`.
3. Fijate qué cambió en `package.json` y qué apareció en la carpeta.
4. Corré `git status`: ¿aparece `node_modules`? ¿Por qué no? (pista: `.gitignore`)

## ✅ Checklist
- [ ] El `package.json` tiene `"type": "module"` y los scripts `start` y `dev`
- [ ] Leíste y escribiste un archivo JSON
- [ ] Instalaste y usaste un paquete
- [ ] `node_modules` **no** está en tu commit (revisalo en el PR, pestaña *Files changed*)
