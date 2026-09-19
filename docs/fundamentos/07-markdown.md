# 07 · Markdown: escribir con formato usando solo texto ✍️

> 📌 Leela antes del ejercicio **git-01**.

Todos los archivos `.md` de este curso (incluido este) están escritos en **Markdown**:
una forma de darle formato a un texto (títulos, negritas, listas) usando **símbolos simples**.

GitHub lo muestra lindo automáticamente. Es el formato estándar para documentar proyectos:
casi todo repositorio del mundo tiene un `README.md`.

---

## Lo básico

| Escribís | Se ve |
|---|---|
| `# Título grande` | <h1>Título grande</h1> |
| `## Título mediano` | <h2>Título mediano</h2> |
| `### Título chico` | <h3>Título chico</h3> |
| `**negrita**` | **negrita** |
| `*cursiva*` | *cursiva* |
| `` `código` `` | `código` |
| `[texto del enlace](https://github.com)` | [texto del enlace](https://github.com) |
| `---` | una línea separadora |

### Párrafos
Para separar párrafos, dejá **una línea en blanco** entre ellos.
Un solo Enter no alcanza: Markdown lo junta con la línea anterior.

### Listas

```markdown
- Manzana
- Banana
  - Banana verde      ← con 2 espacios adelante, queda adentro

1. Primero
2. Segundo

- [ ] Tarea pendiente
- [x] Tarea hecha
```

### Imágenes

```markdown
![Descripción de la imagen](img/foto.png)
```
(Igual que un enlace, pero con `!` adelante.)

### Bloques de código

Para mostrar código, envolvelo en **tres acentos graves** (`` ``` ``) y poné el lenguaje:

````markdown
```html
<h1>Hola</h1>
```
````

### Citas

```markdown
> Esto es una cita o una nota destacada.
```

### Tablas

```markdown
| Nombre | Edad |
|--------|------|
| Ana    | 18   |
```

---

## Ver cómo queda

- **En VS Code:** abrí un `.md` y apretá `Ctrl + Shift + V` → vista previa.
  (O `Ctrl + K` y después `V` para verla al costado, mientras escribís.)
- **En GitHub:** después de hacer push, abrí el archivo y ya se ve con formato.

> 💡 Los emojis también funcionan: podés pegarlos directo (en Windows: `Windows + .`). 🎉

---

## 🧪 Práctica

Abrí [PROGRESO.md](../../PROGRESO.md) en VS Code con la vista previa (`Ctrl + Shift + V`).
Mirá el código de un lado y el resultado del otro. ¿Reconocés cada símbolo?

📖 Guía completa (en inglés, muy visual): https://www.markdownguide.org/cheat-sheet/

---

Siguiente: [08 · Cómo aprender y pedir ayuda](08-aprender-y-pedir-ayuda.md)
