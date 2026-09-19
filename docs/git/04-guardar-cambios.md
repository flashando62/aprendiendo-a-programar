# 04 · Guardar cambios (commit)

Hacer un commit tiene siempre la misma receta de 3 pasos:

```
1. git status   → mirar qué cambió
2. git add      → elegir qué va a la foto
3. git commit   → sacar la foto
```

Vamos a practicarlo.

---

## Paso 0 · Crear una rama de práctica

Para no tocar la versión oficial del curso, vamos a practicar en una **rama** aparte
(qué es una rama lo vemos bien en la guía 06; por ahora pensala como "un borrador").

```bash
git switch -c practica
```

## Paso 1 · Hacer un cambio

En VS Code, creá un archivo nuevo llamado `prueba.txt` en la raíz del repo y escribí:

```
Hola, este es mi primer archivo con Git.
```

Guardalo (`Ctrl + S`).

> ⚠️ **Guardar en VS Code NO es lo mismo que hacer un commit.** Guardar escribe el archivo
> en el disco. El commit guarda una foto en el historial de Git. Necesitás las dos cosas.

## Paso 2 · Mirar qué cambió: `git status`

```bash
git status
```

```
On branch practica
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        prueba.txt
```

Git dice: *"Hay un archivo nuevo que no estoy vigilando"* (*untracked*). Aparece en **rojo**.

## Paso 3 · Prepararlo: `git add`

```bash
git add prueba.txt
```

Volvé a mirar:

```bash
git status
```

```
Changes to be committed:
        new file:   prueba.txt
```

Ahora está en **verde**: está en la zona de preparación, listo para la foto. 📦

> 💡 Para agregar **todos** los cambios de una: `git add .` (el punto = "todo lo de esta carpeta").
> Es lo que vas a usar casi siempre. Pero antes mirá `git status` para no subir algo sin querer.

## Paso 4 · Sacar la foto: `git commit`

```bash
git commit -m "Agrego mi primer archivo de prueba"
```

La `-m` significa *mensaje*. El mensaje explica **qué hiciste**.

```
[practica 3f2a1b9] Agrego mi primer archivo de prueba
 1 file changed, 1 insertion(+)
 create mode 100644 prueba.txt
```

¡Tu primer commit! 🎉📸

## Paso 5 · Ver el historial: `git log`

```bash
git log --oneline
```

```
3f2a1b9 (HEAD -> practica) Agrego mi primer archivo de prueba
a1b2c3d (origin/main, main) Estructura inicial del curso
```

Cada línea es un commit. El código raro del principio (`3f2a1b9`) es su identificador único.

> Si el log es largo y la terminal "se queda trabada" mostrando `:` abajo, apretá **`q`** para salir.

---

## Modificar un archivo existente

Cambiá el texto de `prueba.txt`, guardá, y mirá:

```bash
git status          # dice "modified: prueba.txt"
git diff            # muestra QUÉ líneas cambiaron (- lo viejo en rojo, + lo nuevo en verde)
git add .
git commit -m "Cambio el texto de prueba"
```

## Borrar el archivo de prueba

```bash
git rm prueba.txt
git commit -m "Borro el archivo de prueba"
```

---

## ✍️ Cómo escribir buenos mensajes de commit

El mensaje es para la *vos del futuro* (o para tu compañero de equipo). Tiene que decir **qué hiciste**.

| ❌ Malo | ✅ Bueno |
|---|---|
| `cambios` | `Agrego la sección de contacto` |
| `asdasd` | `Corrijo el color del título` |
| `listo` | `Termino el ejercicio html-02` |
| `arreglé cosas` | `Arreglo el enlace roto del menú` |

Una buena regla: que complete la frase *"Este commit..."* → *"Este commit **agrega la sección de contacto**"*.

---

## ¿Cada cuánto hago commit?

Cada vez que termines **una cosa que funciona**. Commits chicos y frecuentes > un commit gigante al final.

Pensalo como el "guardar partida" de un videojuego: guardás antes de cada jefe. 🎮

---

Siguiente: [05 · Subir y bajar cambios](05-subir-y-bajar.md)
