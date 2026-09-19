# react-01 · Tu primera app: componentes y props ⚛️

- **Rama:** `react-01`
- 🧠 Leer antes: [React · Conceptos clave](../../../docs/react/conceptos-clave.md) (secciones 1 a 6)
- 📚 De apoyo: [react.dev — Tu primer componente](https://es.react.dev/learn/your-first-component) y [Pasar props a un componente](https://es.react.dev/learn/passing-props-to-a-component)

## Crear el proyecto

Parada en la carpeta **de este ejercicio** (`ejercicios/08-react/01-componentes-y-props/`):

```bash
npm create vite@latest solucion -- --template react
cd solucion
npm install
npm run dev
```

Abrí http://localhost:5173. Después, **borrá** el contenido de ejemplo de `App.jsx` y `App.css` para empezar de cero.

> 💡 Instalá la extensión **React Developer Tools** en tu navegador.

## Consigna

Hacé una **página de tarjetas de tus series o películas favoritas** (como en css-02, pero en React):

1. Un componente `Encabezado` con el título de la página y un subtítulo.
2. Un componente `Tarjeta` que reciba por props: `titulo`, `anio`, `genero`, `imagen` y `favorita` (booleano).
   - Si `favorita` es `true`, muestra una ⭐ y tiene una clase CSS distinta (pista: ternario en `className`).
3. En `App.jsx`, un array con al menos 6 series (objetos con `id` y los datos) que se muestra con
   `map` → una `Tarjeta` por serie, con su `key`.
4. Un componente `Pie` que reciba `autora` por props y muestre `"Hecho por [autora] con React ⚛️"`.
5. Cada componente en su propio archivo dentro de `src/components/`, con `export default`.
6. Estilos con CSS (en `App.css` o un `.css` por componente, importado con `import "./Tarjeta.css"`).

## Para investigar 🔍
- Abrí **F12 → Components** (React DevTools). Hacé clic en una `Tarjeta`: ¿ves sus props?
- Sacale la `key` al `map`. ¿Qué aviso aparece en la consola?

## ✅ Checklist
- [ ] Al menos 4 componentes, cada uno en su archivo
- [ ] Usaste props con desestructuración
- [ ] La lista se genera con `map` y cada elemento tiene `key`
- [ ] Usaste `className` (no `class`)
- [ ] `node_modules` no está en el commit
