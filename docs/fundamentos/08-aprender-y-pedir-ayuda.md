# 08 · Cómo aprender, buscar y pedir ayuda 🆘

La habilidad más importante de una programadora no es saberse todo de memoria:
es **saber destrabarse sola** cuando algo no funciona. Esto se aprende.

---

## 1 · Leé el mensaje de error (en serio)

Cuando algo falla, la compu casi siempre **te dice qué pasó y dónde**. El primer instinto es
entrar en pánico; el segundo, que es el bueno, es **leer**.

```
Uncaught ReferenceError: nombre is not defined
    at script.js:12:15
```

| Parte | Qué te dice |
|---|---|
| `ReferenceError` | El **tipo** de error |
| `nombre is not defined` | **Qué** pasó: "`nombre` no está definido" (¿lo escribiste distinto arriba?) |
| `script.js:12:15` | **Dónde**: archivo `script.js`, línea **12**, columna 15. ¡Hacé clic y te lleva! |

Los errores están en inglés. No hace falta saber inglés: copialo en un traductor. Con el tiempo
vas a reconocer los más comunes de memoria (hay una tabla en [JavaScript · Conceptos clave](../javascript/conceptos-clave.md)).

---

## 2 · Cuando no funciona y **no hay** error

1. **¿Guardaste?** (¿Hay un ● en la pestaña de VS Code?) — Es la causa #1. En serio.
2. **¿Recargaste** el navegador? (`F5`)
3. **¿Estás editando el archivo que creés?** A veces tenés dos `index.html` en carpetas distintas.
4. **Abrí F12 → Consola.** ¿Hay algo en rojo?
5. **Volvé a la última versión que funcionaba** y agregá los cambios de a uno.
6. **Explicáselo a un patito de goma.** 🦆 Sí, en serio: explicar el código en voz alta,
   línea por línea, hace que encuentres el error. Se llama *rubber duck debugging* y lo usan profesionales.

---

## 3 · Buscá

Los programadores googlean **todo el día**. No es trampa: es el trabajo.

**Cómo buscar bien:**
- Poné **el lenguaje + lo que querés hacer**: `css centrar un div`, `javascript sumar elementos de un array`.
- Si es un error, **copiá el mensaje** (sin tus nombres de variables): `ReferenceError is not defined javascript`.
- **Buscar en inglés da muchos más resultados.** `css center div` encuentra 10 veces más que en español.

**Dónde confiar:**

| Sitio | Para qué |
|---|---|
| [MDN Web Docs](https://developer.mozilla.org/es/) | ⭐ **La** referencia de HTML, CSS y JS. Está en español. |
| [javascript.info](https://es.javascript.info/) | Tutorial de JavaScript muy claro, en español |
| [Stack Overflow](https://es.stackoverflow.com/) | Preguntas y respuestas de programadores. Mirá la respuesta con más votos ✅ |
| [W3Schools](https://www.w3schools.com/) | Ejemplos cortitos para probar rápido (en inglés) |

> ⚠️ Mirá la **fecha**. Una respuesta de 2012 puede estar desactualizada (por ejemplo, si usa `var` en JavaScript).

---

## 4 · Preguntá (bien)

**La regla de los 20 minutos:** si estás trabada, intentá sola **20 minutos** (leé el error, buscá, probá).
Si pasaron 20 minutos y no avanzás, **preguntá**. Menos de eso no aprendés a destrabarte;
mucho más de eso te frustrás y perdés tiempo.

**Una buena pregunta tiene 4 partes:**

1. **Qué quería hacer:** *"Quiero que el botón cambie el color del título."*
2. **Qué pasa en cambio:** *"No pasa nada cuando lo toco."*
3. **Qué probé:** *"Revisé que el id sea el mismo y agregué un console.log, pero no aparece en la consola."*
4. **El código y el error:** el link al archivo en GitHub, una captura o el texto del error.

❌ *"No me anda."* → 😵 Imposible ayudar.
✅ Las 4 partes → Muchas veces **encontrás la respuesta vos misma mientras escribís la pregunta**. 😄

> 💡 Si tu código ya está en GitHub (en tu rama), podés pasarle a tu mentor el link directo al archivo
> o, mejor aún, preguntar en un comentario del Pull Request.

---

## 5 · La inteligencia artificial (ChatGPT, Claude, Copilot…)

La IA es una herramienta muy poderosa **y** una trampa para quien está aprendiendo.

✅ **Usala para:**
- Que te **explique** un concepto que no entendiste, "como si tuvieras 10 años".
- Que te **explique un error**: *"¿Qué significa este error? No me des la solución, dame una pista."*
- Que te dé **ejercicios extra** para practicar.
- **Revisar** tu código *después* de que lo hiciste sola: *"¿Qué podría mejorar?"*

❌ **No la uses para:**
- **Que te haga el ejercicio.** Si la IA lo escribe, **la que aprende es la IA**. Vas a llegar
  al proyecto final sin saber hacer nada solo, y eso se nota enseguida.
- Copiar código que **no entendés**. La IA a veces se equivoca con total seguridad.

> 🧠 **Regla:** si no podrías explicar cada línea de tu código, todavía no está terminado.

---

## 6 · Hábitos que ayudan

- **Poquito todos los días** > mucho un solo día. El cerebro aprende programación durmiendo entre sesiones.
- **Escribí tu diario** (ejercicio git-02): qué aprendiste y qué te costó.
- **Tomá descansos.** Si estás frustrada, alejarte 10 minutos ayuda más que 1 hora más de pelea.
- **Compará tu progreso con tu versión de hace un mes**, no con otras personas.
- **Celebrá** cuando algo te sale. 🎉 Programar es difícil y lo estás logrando.

---

Siguiente: tenés un [Glosario](09-glosario.md) para consultar cada vez que aparezca una palabra rara.
