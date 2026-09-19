# 01 · La terminal sin miedo

La **terminal** (también llamada consola o línea de comandos) es una ventana donde le
das órdenes a la compu **escribiendo**, en lugar de hacer clic.

Parece de película de hackers, pero en realidad es como mandarle mensajes de texto a la compu. 📱

---

## Abrir la terminal

- **Windows:** buscá **Git Bash** en el menú inicio.
- **Mac:** abrí la app **Terminal**.
- **Dentro de VS Code:** menú *Terminal → Nueva terminal* (o `` Ctrl + ` ``).

Vas a ver algo así:

```
maria@MI-COMPU MINGW64 ~
$
```

El `$` significa *"estoy esperando que escribas algo"*. **No lo copies** cuando veas comandos
en las guías: solo escribí lo que viene después.

El `~` es tu **carpeta personal** (en Windows, `C:\Users\tu-nombre`).

---

## Anatomía de un comando

Todos los comandos tienen la misma forma. Aprendela y vas a poder leer cualquiera:

```
git  commit  -m  "Agrego mi foto"
└┬┘  └──┬─┘  └┬┘ └──────┬───────┘
programa  │  opción   valor de la opción
      subcomando
```

| Parte | Qué es | Ejemplo |
|---|---|---|
| **Programa** | Quién hace el trabajo | `git`, `cd`, `ls` |
| **Subcomando** | Qué le pedís (algunos programas, como git, tienen muchos) | `commit`, `push`, `status` |
| **Argumento** | Sobre qué cosa actuar | `cd Documents` → `Documents` |
| **Opción** (*flag*) | Modifica cómo trabaja. Empieza con `-` (letra) o `--` (palabra) | `-m`, `-u`, `--global`, `--oneline` |

- Las partes se separan con **un espacio**. `git commit` ✅ · `gitcommit` ❌
- Si un valor tiene espacios, va **entre comillas**: `-m "Mi primer commit"`.
- Lo que va después de un `#` es un **comentario** (una nota en las guías). Si lo copiás, se ignora.
- Apretás **Enter** para ejecutar. Si no pasa nada y vuelve a aparecer el `$`, casi siempre
  significa que **salió bien**. (Los programas de terminal suelen hablar solo cuando hay algo para decir.)

> 💡 Casi todos los comandos tienen ayuda: `git status --help` o `ls --help`.

> ⚠️ Recordá: en la terminal **`Ctrl + C` cancela**, no copia. Para pegar usá **clic derecho → Paste** o `Shift + Insert`
> (ver [El teclado y los atajos](../fundamentos/02-teclado-y-atajos.md)).

---

## Los 6 comandos que necesitás

### 1. `pwd` — ¿Dónde estoy?
*Print Working Directory.* Muestra en qué carpeta estás parada.

```bash
pwd
```
```
/c/Users/maria
```

### 2. `ls` — ¿Qué hay acá?
*List.* Muestra los archivos y carpetas de donde estás.

```bash
ls
```
```
Desktop/  Documents/  Downloads/  Music/  Pictures/
```
Las que terminan en `/` son carpetas.

### 3. `cd` — Ir a otra carpeta
*Change Directory.*

```bash
cd Documents      # entrar a la carpeta Documents
cd ..             # volver a la carpeta de arriba (la "madre")
cd ~              # volver a tu carpeta personal
```

> 💡 **Truco del Tab:** escribí `cd Doc` y apretá la tecla **Tab**. ¡Se completa sola!
> Usalo siempre: es más rápido y evita errores de tipeo.

### 4. `mkdir` — Crear una carpeta
*Make Directory.*

```bash
mkdir programacion
```

### 5. `code .` — Abrir la carpeta actual en VS Code
El `.` significa *"la carpeta donde estoy"*.

```bash
code .
```

### 6. `clear` — Limpiar la pantalla
Cuando hay mucho texto y te mareás. (También funciona `Ctrl + L`.)

---

## 🧪 Práctica

Hacé esto en orden y fijate qué pasa en cada paso:

```bash
cd ~
pwd
ls
mkdir programacion
ls                 # ¿aparece "programacion"?
cd programacion
pwd                # ¿cambió?
cd ..
pwd                # ¿volviste?
```

Vamos a usar esa carpeta `programacion` para guardar el repo del curso. 

---

## 🆘 Si algo sale mal

| Mensaje | Qué significa |
|---|---|
| `No such file or directory` | Esa carpeta no existe donde estás. Hacé `ls` para ver qué hay. |
| `command not found` | Escribiste mal el comando (¿un espacio de más? ¿mayúsculas?). |
| La terminal "no responde" | Probablemente está esperando algo. Apretá `Ctrl + C` para cancelar. |

> ⚠️ En la terminal **las mayúsculas importan**: `Documents` no es lo mismo que `documents`.
> Y los nombres con espacios hay que ponerlos entre comillas: `cd "Mis Documentos"`.
> Por eso los programadores evitamos espacios en los nombres de carpetas y archivos.

---

Siguiente: [02 · ¿Qué es Git y qué es GitHub?](02-que-es-git.md)
