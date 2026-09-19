# 03 · Cómo funciona la web 🌍

Vas a aprender a hacer páginas web. Pero ¿qué pasa realmente cuando entrás a una?

---

## Internet y la web no son lo mismo

- **Internet** es la **red**: millones de computadoras conectadas por cables, antenas y satélites.
  Son las rutas. 🛣️
- **La web** es **uno** de los servicios que viajan por esa red: las páginas que ves en el navegador.
  (WhatsApp, el mail o los juegos online también usan internet, pero no son "la web".)

---

## Cliente y servidor

En la web hay dos protagonistas:

```
   💻 CLIENTE                                   🖥️ SERVIDOR
 (tu navegador)                        (una compu en algún lugar del mundo)

   "Quiero la página                   
    de wikipedia.org"   ───── pedido ─────►   Busca los archivos
                                                   │
   Recibe los archivos  ◄──── respuesta ────   Manda: index.html,
   y DIBUJA la página                           estilos.css, script.js,
                                                imágenes...
```

- El **servidor** es una compu (casi siempre sin pantalla) que **guarda** los archivos de un sitio y los
  **entrega** cuando alguien los pide.
- El **cliente** es tu **navegador** (Chrome, Firefox, Edge…). Pide los archivos y los convierte en
  la página que ves.

> 🍕 **Analogía:** el navegador es el cliente que pide una pizza; el servidor es la pizzería;
> la pizza son los archivos. El navegador además la "arma" en tu pantalla.

**Dato clave:** una página web **son archivos de texto** (`.html`, `.css`, `.js`) como los que vas a escribir vos.
El navegador los lee y los transforma en algo lindo. No hay magia. ✨

---

## La URL: la dirección de una página

```
https://www.ejemplo.com/blog/receta.html
└─┬──┘   └──────┬─────┘└───────┬───────┘
protocolo     dominio          ruta
```

| Parte | Qué es |
|---|---|
| `https://` | El **protocolo**: el "idioma" en que hablan cliente y servidor. La `s` = seguro (cifrado 🔒) |
| `www.ejemplo.com` | El **dominio**: el nombre del servidor (como el nombre de un negocio) |
| `/blog/receta.html` | La **ruta**: qué archivo querés, dentro del servidor (¡como las carpetas de tu compu!) |

---

## Los tres lenguajes de la web

Cada página web está hecha con tres lenguajes que trabajan juntos:

| Lenguaje | Rol | Analogía (una casa 🏠) | Analogía (una persona 🧍‍♀️) |
|---|---|---|---|
| **HTML** | **Contenido y estructura**: qué hay | Paredes, puertas, ventanas | El esqueleto |
| **CSS** | **Presentación**: cómo se ve | Pintura, muebles, decoración | La ropa y el peinado |
| **JavaScript** | **Comportamiento**: qué hace | La electricidad: timbre, luces | Los músculos y el cerebro |

```html
<button>Tocame</button>                           ← HTML: hay un botón
button { background: pink; }                      ← CSS: el botón es rosa
boton.addEventListener("click", saludar);         ← JS: al tocarlo, saluda
```

Vas a aprenderlos **en ese orden**, porque cada uno se apoya en el anterior.

> ⚠️ **JavaScript no es Java.** Son lenguajes completamente distintos que tienen nombres parecidos
> por una estrategia de marketing de los años 90. Como "auto" y "autobús". 🚗🚌

---

## Frontend y backend

- **Frontend** ("la parte de adelante"): lo que corre **en el navegador**, lo que el usuario ve y toca.
  HTML, CSS y JavaScript. **Esto es lo que vas a aprender.**
- **Backend** ("la parte de atrás"): lo que corre **en el servidor**. Guarda datos, maneja usuarios
  y contraseñas, procesa pagos. Usa otros lenguajes (y también JavaScript).

Cuando hacés un formulario en este curso, "no se envía a ningún lado": eso es porque todavía no tenemos backend.

---

## ¿Y cómo veo mis páginas si no tengo servidor?

Tenés dos opciones:

1. **Doble clic en el `.html`**: el navegador abre el archivo directamente desde tu disco.
   La dirección empieza con `file:///C:/Users/...`. Funciona para casi todo.
2. **Live Server** (extensión de VS Code): crea un **mini servidor en tu propia compu**.
   La dirección es algo como `http://127.0.0.1:5500/index.html`.
   - `127.0.0.1` (o `localhost`) significa **"esta misma compu"**.
   - Además, **recarga la página sola** cada vez que guardás. ⭐ Por eso la recomendamos.

Al final del curso vas a usar **GitHub Pages**: un servidor gratuito de GitHub que publica tus
archivos para que cualquiera en el mundo los vea con una URL. 🚀

---

## 🧪 Práctica

1. Entrá a cualquier página (por ejemplo, https://es.wikipedia.org).
2. Clic derecho → **Ver código fuente de la página** (o `Ctrl + U`).
   Eso es HTML. Así de "feo" es por dentro todo lo que ves en internet. 😄
3. Apretá **F12**. Se abren las **herramientas de desarrollo**. Tocá la flechita de arriba a la izquierda
   y después cualquier parte de la página: te muestra el HTML de esa parte.
4. En la pestaña *Elementos*, hacé doble clic en algún texto y cambialo. ¡Modificaste Wikipedia!
   (Tranqui: solo en tu pantalla. Si recargás, vuelve a la normalidad.)

---

Siguiente: [04 · ¿Qué es programar?](04-que-es-programar.md)
