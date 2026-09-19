# 01 · La compu por dentro: archivos y carpetas 🗂️

Antes de programar hay que entender **dónde vive** lo que programamos. Todo lo que hagas
en este curso van a ser **archivos** guardados dentro de **carpetas**.

---

## ¿Qué es un archivo?

Un **archivo** es un paquete de información guardado en la compu, con un nombre.
Una foto, una canción, un documento de Word: todos son archivos.

## ¿Qué es una carpeta?

Una **carpeta** (en inglés *folder* o *directory*) es un contenedor de archivos… y de otras carpetas.
Las carpetas adentro de carpetas forman un **árbol**:

```
📁 C:
└── 📁 Users
    └── 📁 maria
        ├── 📁 Desktop          (el Escritorio)
        ├── 📁 Documents        (Documentos)
        │   └── 📄 cv.docx
        └── 📁 programacion
            └── 📁 aprendiendo-a-programar
                ├── 📄 README.md
                └── 📁 ejercicios
```

Se habla de carpetas como de una familia:
- `Users` es la carpeta **madre** (o *padre*) de `maria`.
- `Desktop` y `Documents` son **hijas** de `maria`, y **hermanas** entre sí.

Esta idea de árbol con madres e hijas **vuelve a aparecer en HTML**. Guardátela. 🌳

---

## Extensiones: el "apellido" del archivo

El nombre de un archivo tiene dos partes separadas por un punto:

```
  foto-de-perfil . jpg
  └─── nombre ──┘  └─ extensión
```

La **extensión** le dice a la compu **qué tipo de archivo es** y con qué programa abrirlo:

| Extensión | Tipo | En este curso |
|---|---|---|
| `.html` | Página web | ⭐ Lo vas a usar muchísimo |
| `.css` | Estilos de una página web | ⭐ |
| `.js` | Código JavaScript | ⭐ |
| `.md` | Texto con formato Markdown | ⭐ (documentación) |
| `.jpg` `.png` `.webp` `.svg` | Imágenes | ⭐ |
| `.txt` | Texto plano | |
| `.docx` | Documento de Word | ❌ **no sirve** para programar |

### ⚠️ Windows te esconde las extensiones: hacelas visibles

Por defecto Windows muestra `index` en vez de `index.html`. Eso trae muchos problemas
(por ejemplo, terminar con un archivo `index.html.txt` sin darte cuenta).

**Windows 11:** abrí el Explorador de archivos → **Ver** → **Mostrar** → activá
✅ **Extensiones de nombre de archivo** y ✅ **Elementos ocultos**.

**Windows 10:** Explorador → pestaña **Vista** → activá ✅ **Extensiones de nombre de archivo** y ✅ **Elementos ocultos**.

> "Elementos ocultos" te va a dejar ver la carpeta `.git` que crea Git. **Nunca la toques ni la borres**:
> ahí vive todo el historial del proyecto.

---

## Texto plano vs documentos con formato

El código se escribe en **texto plano**: solo letras, sin negritas, sin colores, sin tamaños.

- ❌ **Word / Google Docs** guardan mucha información escondida (fuentes, márgenes…). No sirven para programar.
- ✅ **VS Code** es un editor de texto plano. Los colores que ves en el código los pone
  VS Code para ayudarte a leer, pero **no se guardan en el archivo**.

---

## Cómo nombrar archivos y carpetas (reglas de programadora)

| ✅ Bien | ❌ Mal | Por qué |
|---|---|---|
| `mi-pagina.html` | `Mi Página.html` | Espacios y tildes traen problemas en la web y en la terminal |
| `foto-perfil.jpg` | `FOTO perfil (1).JPG` | Mayúsculas y paréntesis complican |
| `index.html` | `index.HTML` | Extensiones siempre en minúscula |

**Regla simple:** todo en **minúscula**, **sin espacios** (usá guion `-`), **sin tildes ni ñ**.

> 💡 `index.html` es un nombre especial: es la página que un navegador abre **por defecto**
> cuando entrás a una carpeta de un sitio web. Por eso la página principal casi siempre se llama así.

---

## Rutas: la "dirección" de un archivo

Una **ruta** (*path*) es el camino para llegar a un archivo, carpeta por carpeta:

```
C:\Users\maria\programacion\aprendiendo-a-programar\README.md     ← así lo escribe Windows
/c/Users/maria/programacion/aprendiendo-a-programar/README.md     ← así lo escribe Git Bash
```

Windows usa la barra invertida `\`; la web, Git Bash, Mac y Linux usan la barra normal `/`.
**En programación web usá siempre `/`.**

Las rutas son tan importantes que tienen su propia guía: [06 · Rutas de archivos](06-rutas-de-archivos.md).

---

## 🧪 Práctica

1. Activá las extensiones y los elementos ocultos en el Explorador.
2. En el Escritorio, creá un archivo de texto nuevo (clic derecho → Nuevo → Documento de texto).
   ¿Ves que se llama `Nuevo documento de texto.txt`?
3. Renombralo a `prueba.html`. Windows te va a advertir que cambiás la extensión: aceptá.
   ¿Cambió el ícono? Hacele doble clic: ¡se abre en el navegador!
4. Borralo.

---

Siguiente: [02 · El teclado y los atajos](02-teclado-y-atajos.md)
