# react-02 · Estado y eventos 🧠

- **Rama:** `react-02`
- 🧠 Leer antes: [React · Conceptos clave](../../../docs/react/conceptos-clave.md) (sección 7)
- 📚 De apoyo: [react.dev — Responder a eventos](https://es.react.dev/learn/responding-to-events) y [El estado: la memoria de un componente](https://es.react.dev/learn/state-a-components-memory)

## Consigna

Creá el proyecto con Vite en `solucion/` (igual que en react-01).
¿Te acordás de las mini apps de **js-06**? Rehacelas en React, cada una como un componente:

1. **`Contador`**: botones `+`, `−` y `Reiniciar`. En rojo si es negativo.
   Recibe por props `inicial` y `paso` (cuánto suma cada clic). Usalo **dos veces** en `App` con distintas props:
   ¿cada contador tiene su propio estado?
2. **`Saludador`**: un input controlado y un botón. Al tocarlo, muestra `¡Hola, [nombre]!`.
   Si está vacío, muestra un error.
3. **`ModoOscuro`**: un botón que alterna el tema. El estado vive en `App` y se le pasa al botón
   una función por props (los eventos **suben** ⬆️). El tema cambia la clase del contenedor principal.
4. **`ContadorDeCaracteres`**: un `textarea` y debajo `"23 / 140"`, en rojo si pasa de 140.
   (¿Necesitás un estado para la cantidad de caracteres, o se puede **calcular**?)

## Para pensar 🤔
Compará tu código de js-06 con este. ¿Qué tuviste que hacer "a mano" en JavaScript puro que acá hace React solo?
Contalo en el PR.

## ✅ Checklist
- [ ] Usaste `useState` en varios componentes
- [ ] Nunca modificás el estado directamente (siempre con `set…`)
- [ ] Un hijo cambia el estado del padre a través de una función recibida por props
- [ ] No guardás en el estado cosas que se pueden calcular
