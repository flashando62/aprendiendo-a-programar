# 👩‍💻 Aprendiendo a programar desde cero

¡Bienvenida! Este repositorio es tu cuaderno de programación. Acá vas a encontrar
**todo el material** del curso y acá también vas a **subir tus ejercicios**.

No necesitás saber nada de antemano. Vamos paso a paso.

---

## 🗺️ ¿Qué vas a aprender?

| Módulo | Tema | Para qué sirve |
|---|---|---|
| 0 | [Preparar la compu](docs/git/00-preparar-la-compu.md) | Instalar las herramientas |
| 1 | **Git y GitHub** | Guardar y compartir tu código (lo vas a usar en TODO el curso) |
| 2 | **HTML** | El contenido de una página web (textos, imágenes, enlaces) |
| 3 | **CSS** | El diseño de una página web (colores, tamaños, posiciones) |
| 4 | **JavaScript** | El comportamiento de una página web (botones, cálculos, interacción) |
| 🏁 | **Proyecto final** | Tu propio portfolio publicado en internet |

El detalle semana por semana está en 👉 **[PLAN.md](PLAN.md)**.

---

## 🚀 ¿Por dónde empiezo?

1. Leé [PLAN.md](PLAN.md) para ver el camino completo.
2. Seguí las guías de Git **en orden**:
   0. [Preparar la compu](docs/git/00-preparar-la-compu.md)
   1. [La terminal sin miedo](docs/git/01-la-terminal.md)
   2. [¿Qué es Git y qué es GitHub?](docs/git/02-que-es-git.md)
   3. [Descargar este repo a tu compu (clonar)](docs/git/03-clonar-el-repo.md)
   4. [Guardar cambios (commit)](docs/git/04-guardar-cambios.md)
   5. [Subir y bajar cambios (push y pull)](docs/git/05-subir-y-bajar.md)
   6. [Ramas y Pull Requests: cómo entregar ejercicios](docs/git/06-ramas-y-pull-requests.md)
   7. [¡Socorro! Errores comunes](docs/git/07-errores-comunes.md)
   8. [Machete de comandos](docs/git/08-machete.md)
3. Hacé los ejercicios de la carpeta [`ejercicios/`](ejercicios/).
4. Marcá tu avance en [PROGRESO.md](PROGRESO.md).

---

## 📁 Cómo está organizado este repo

```
📦 Aprendizaje Repo
├── README.md            ← estás acá
├── PLAN.md              ← el plan de estudio semana por semana
├── PROGRESO.md          ← tu checklist de avance (lo vas completando vos)
├── GUIA-MENTOR.md       ← instrucciones para quien te enseña
├── docs/
│   └── git/             ← guías paso a paso de Git
└── ejercicios/
    ├── 01-git/
    ├── 02-html/
    ├── 03-css/
    ├── 04-javascript/
    └── 05-proyecto-final/
```

Cada ejercicio tiene su propia carpeta con un `README.md` que explica **qué hay que hacer**.
Vos creás tus archivos dentro de la subcarpeta `solucion/` de ese ejercicio.

---

## 🔁 El ciclo de cada ejercicio (resumen)

```bash
git switch main            # 1. Volver a la rama principal
git pull                   # 2. Bajar lo último
git switch -c html-01      # 3. Crear una rama para el ejercicio
# ... programar ...
git add .                  # 4. Preparar los cambios
git commit -m "Hago el ejercicio html-01"   # 5. Guardarlos
git push -u origin html-01 # 6. Subirlos a GitHub
# 7. Abrir un Pull Request en GitHub y esperar la revisión 🙌
```

Si esto hoy no se entiende nada, **no pasa nada**: está explicado en detalle en la
[guía 6](docs/git/06-ramas-y-pull-requests.md).

---

## 💡 Reglas de oro

- **Equivocarse es parte de aprender.** Con Git casi todo tiene arreglo.
- **Preguntá siempre.** No existen preguntas tontas.
- **Escribí el código vos**, no lo copies y pegues. Los dedos también aprenden.
- **Un poquito todos los días** rinde más que mucho un solo día.
- Si algo no funciona, leé el mensaje de error con calma: casi siempre dice qué pasa.

## 🔒 Ojo: este repo es público

Cualquier persona en internet puede ver lo que subas acá (¡y queda en el historial aunque después lo borres!).
**Nunca subas:** tu dirección, teléfono, DNI, contraseñas, fecha de nacimiento completa ni fotos que no quieras que vea cualquiera.
Para los ejercicios alcanza con tu nombre, tu ciudad y datos inventados.
