# 02 · El teclado y los atajos ⌨️

Programando vas a usar símbolos que casi nunca escribiste: `` { } [ ] < > ; | ` ``.
Encontrarlos al principio cuesta. En dos semanas los vas a apretar sin mirar. 💪

---

## Las teclas modificadoras

| Tecla | Dónde está | Para qué |
|---|---|---|
| **Shift** (⇧) | Las dos flechas gordas hacia arriba, a los costados | El símbolo de **arriba** de la tecla |
| **AltGr** | A la **derecha** de la barra espaciadora | El símbolo de **abajo a la derecha** de la tecla |
| **Ctrl** | Las esquinas de abajo | Atajos (copiar, pegar…) |

Una tecla puede tener hasta 3 símbolos:

```
┌───────┐
│ ?     │  ← con Shift
│ '   \ │  ← solo / con AltGr
└───────┘
```

---

## Dónde están los símbolos (teclado **Latinoamericano**, el más común en Argentina)

| Símbolo | Nombre | Cómo | Se usa en |
|---|---|---|---|
| `<` `>` | menor, mayor | Tecla a la izquierda de la **Z** (con Shift: `>`) | HTML |
| `/` | barra | Shift + 7 | HTML, rutas |
| `\` | barra invertida | AltGr + tecla `'` (a la derecha del 0) | rutas de Windows |
| `=` | igual | Shift + 0 | todo |
| `"` | comillas dobles | Shift + 2 | HTML, JS |
| `'` | comilla simple | Tecla a la derecha del 0 | JS |
| `{` `}` | llaves | Las dos teclas a la derecha de la **Ñ** | CSS, JS |
| `[` `]` | corchetes | Shift + esas mismas teclas | JS |
| `( )` | paréntesis | Shift + 8 y Shift + 9 | JS |
| `;` | punto y coma | Shift + , | CSS, JS |
| `:` | dos puntos | Shift + . | CSS |
| `#` | numeral | Shift + 3 | CSS, Markdown |
| `_` | guion bajo | Shift + - | nombres |
| `@` | arroba | AltGr + Q | emails |
| `\|` | barra vertical | Tecla a la izquierda del **1** | terminal |
| `~` | virgulilla | AltGr + tecla `+`, y después Espacio | terminal |
| `` ` `` | acento grave (*backtick*) | AltGr + tecla `}`, y después Espacio | JavaScript |
| `*` | asterisco | Shift + tecla `+` | JS, Markdown |

> 🔍 **Si tu teclado no coincide** (puede ser de España o en inglés), usá el **Teclado en pantalla**
> de Windows: apretá `Windows + Ctrl + O`. Si apretás Shift o AltGr en ese teclado virtual,
> te muestra qué símbolo sale en cada tecla. ¡Es el mapa perfecto!

> 💡 `~` y `` ` `` son **teclas muertas**: al apretarlas no aparece nada hasta que apretás otra tecla.
> Por eso hay que apretar **Espacio** después.

---

## Atajos universales (funcionan en casi todos los programas)

| Atajo | Qué hace | |
|---|---|---|
| `Ctrl + C` | Copiar | |
| `Ctrl + V` | Pegar | |
| `Ctrl + X` | Cortar | |
| `Ctrl + Z` | **Deshacer** ⭐ | Tu mejor amigo |
| `Ctrl + Y` | Rehacer | |
| `Ctrl + S` | **Guardar** ⭐ | Apretalo todo el tiempo |
| `Ctrl + A` | Seleccionar todo | |
| `Ctrl + F` | Buscar | |
| `Alt + Tab` | Cambiar de ventana | Vas a saltar entre VS Code y el navegador mil veces |
| `F5` | Recargar la página (en el navegador) | |
| `F12` | Herramientas de desarrollo (en el navegador) | Lo vas a usar muchísimo |

## ⚠️ ¡En la terminal es distinto!

En la terminal (Git Bash), **`Ctrl + C` NO copia**: **cancela** lo que se está ejecutando.

| En Git Bash | Cómo |
|---|---|
| Copiar | Seleccioná el texto con el mouse (se copia solo) o `Ctrl + Insert` |
| Pegar | Clic derecho → *Paste*, o `Shift + Insert` |
| Cancelar | `Ctrl + C` |
| Repetir el comando anterior | Flecha `↑` |

---

## 🧪 Práctica

Abrí el Bloc de notas y escribí esto **sin copiar y pegar**, buscando cada símbolo:

```
<h1>Hola</h1>
body { color: red; }
const lista = [1, 2, 3];
console.log(`Hola ${nombre}`);
a || b
~/programacion
```

Si pudiste escribir todo: ¡ya tenés el teclado dominado! 🎉

---

Siguiente: [03 · Cómo funciona la web](03-como-funciona-la-web.md)
