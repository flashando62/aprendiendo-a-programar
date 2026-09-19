# 04 · ¿Qué es programar? 🤖

## Programar es dar instrucciones

**Programar** es escribir instrucciones para que una computadora haga algo.
Esas instrucciones se escriben en un **lenguaje de programación**, y el texto que escribís se llama **código**.

La compu es **rapidísima**, pero **no piensa**: hace **exactamente** lo que le decís, ni más ni menos.

### 🥪 El experimento del sándwich

Imaginá que le explicás a un robot cómo hacer un sándwich:

> *"Poné el jamón sobre el pan."*

El robot apoya el paquete de jamón cerrado encima de la bolsa de pan. 🤦‍♀️ Hiciste lo que dijiste,
no lo que quisiste decir. La versión para robot sería:

```
1. Abrir la bolsa de pan
2. Sacar 2 rodajas de pan
3. Apoyar las 2 rodajas sobre el plato
4. Abrir el paquete de jamón
5. Sacar 1 feta de jamón
6. Poner la feta sobre UNA de las rodajas
7. Poner la otra rodaja encima de la feta
```

Eso es programar: **dividir un problema en pasos muy chiquitos y precisos**.

---

## Algoritmo

Un **algoritmo** es una lista ordenada de pasos para resolver un problema.
La receta del sándwich es un algoritmo. Las instrucciones para armar un mueble también.

Un programa es un algoritmo **escrito en un lenguaje que la compu entiende**.

## Pseudocódigo: pensar antes de escribir

Antes de escribir código, los programadores escriben los pasos **en su propio idioma**. Eso se llama
**pseudocódigo** ("código falso"). Por ejemplo, para saber si alguien puede votar:

```
pedir la edad
si la edad es 16 o más
    mostrar "Puede votar"
si no
    mostrar "Todavía no puede votar"
```

Y recién después lo traducís a JavaScript:

```js
const edad = Number(prompt("¿Cuántos años tenés?"));
if (edad >= 16) {
  alert("Puede votar");
} else {
  alert("Todavía no puede votar");
}
```

> 💡 **Consejo de oro:** cuando un ejercicio no te sale, **alejate del código**. Escribí los pasos en
> un papel o con comentarios, en castellano. Si no sabés explicarlo en castellano, no vas a poder en JavaScript.

---

## Lenguajes: cada uno para una cosa

Hay cientos de lenguajes: JavaScript, Python, Java, C#, PHP… Como los idiomas, cada uno tiene
sus reglas, pero **las ideas son las mismas** en todos: variables, condiciones, repeticiones, funciones.
Cuando aprendés bien uno, el segundo es muchísimo más fácil.

Técnicamente, **HTML y CSS no son lenguajes de programación**: no pueden tomar decisiones ni repetir cosas.
HTML es un *lenguaje de marcado* y CSS un *lenguaje de estilos*. **JavaScript sí es un lenguaje de programación.**

---

## Sintaxis: la ortografía del código

La **sintaxis** son las reglas de escritura de un lenguaje. La compu es **mucho más estricta**
que tu profe de Lengua:

| Humano 🧍‍♀️ | Compu 🤖 |
|---|---|
| Entiende "ola ke ase" | Un solo carácter mal → **error** |
| `Hola` y `hola` son lo mismo | `Hola` y `hola` son **cosas distintas** |
| Sobreentiende lo que falta | Si falta un `}`, no funciona nada |

---

## Errores: son normales (de verdad)

Vas a tener errores **todo el tiempo**. Los programadores con 20 años de experiencia también.
Un error **no significa que seas mala programando**: es parte del trabajo.

Hay dos tipos de errores:

1. **Errores de sintaxis:** escribiste algo mal (falta una llave, una comilla…).
   La compu **te avisa** con un mensaje. Son los fáciles.
2. **Errores de lógica:** el código funciona, pero **hace otra cosa** de la que querías
   (el robot con el paquete de jamón). La compu **no te avisa**: tenés que darte cuenta vos. Son los difíciles.

A los errores se les dice **bugs** (bichos 🐛) y a buscarlos y arreglarlos, **debuggear** (depurar).

> 🐛 Dato curioso: en 1947 encontraron una **polilla real** atrapada dentro de una computadora,
> causando fallas. La pegaron en el cuaderno de registro con la nota *"first actual case of bug being found"*.

---

## ¿Cómo se aprende a programar?

- **Programando.** Leer y mirar videos ayuda, pero se aprende **escribiendo código**. Como andar en bici.
- **Escribí el código vos**, no lo copies y pegues. Los dedos también aprenden.
- **Rompé cosas a propósito.** ¿Qué pasa si saco esta línea? ¿Y si cambio este número? Así se entiende.
- **Frustrarse es parte.** Si llevás mucho rato trabada, levantate, tomá agua, y volvé. Muchas veces la
  solución aparece en la ducha. 🚿
- **Nadie se sabe todo de memoria.** Los programadores buscan cosas en Google **todo el día**.
  Lo importante no es memorizar, es **entender** y saber **dónde buscar**.

---

## 🧪 Práctica

En un papel (o en el Bloc de notas), escribí el **pseudocódigo** de:

1. Cómo cruzar la calle en una esquina con semáforo.
2. Cómo decidir qué ropa ponerte según la temperatura (más de 25°, entre 15° y 25°, menos de 15°).
3. Cómo encontrar el número más grande en una lista de 5 números, mirándolos de a uno.

Mostráselo a tu mentor. No hay una respuesta única: lo importante es que los pasos sean **claros y precisos**.

---

Siguiente: instalar las herramientas → [Git · 00 · Preparar la compu](../git/00-preparar-la-compu.md)
y después volvé a [05 · Visual Studio Code](05-vs-code.md).
