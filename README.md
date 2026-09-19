# 👩‍💻 Aprendiendo a programar desde cero

¡Bienvenida! Este repositorio es tu cuaderno de programación. Acá vas a encontrar
**todo el material** del curso y acá también vas a **subir tus ejercicios**.

No necesitás saber nada de antemano. Vamos paso a paso.

---

## 🗺️ ¿Qué vas a aprender?

### 🌱 Etapa 1 · Fundamentos web

| Módulo | Tema | Para qué sirve |
|---|---|---|
| 0 | [Fundamentos](docs/fundamentos/README.md) y [preparar la compu](docs/git/00-preparar-la-compu.md) | Entender las bases e instalar las herramientas |
| 1 | **Git y GitHub** | Guardar y compartir tu código (lo vas a usar en TODO el curso) |
| 2 | **HTML** | El contenido de una página web (textos, imágenes, enlaces) |
| 3 | **CSS** | El diseño de una página web (colores, tamaños, posiciones) |
| 4 | **JavaScript** | El comportamiento de una página web (botones, cálculos, interacción) |
| 🏁 | **Proyecto final** | Tu propio portfolio publicado en internet |

### 🚀 Etapa 2 · Full stack (cuando termines la Etapa 1)

| Módulo | Tema | Para qué sirve |
|---|---|---|
| 5 | **JavaScript moderno y APIs** | Las herramientas de JS que usan Node y React; pedir datos a internet |
| 6 | **Node.js y Express** | Hacer tu propio backend: servidores y APIs |
| 7 | **React** | Interfaces modernas con componentes |
| 🏆 | **Proyecto final** | Tu propia aplicación full stack (React + Node) |

El detalle semana por semana está en 👉 **[PLAN.md](PLAN.md)**.

---

## 🚀 ¿Por dónde empiezo?

1. Leé [PLAN.md](PLAN.md) para ver el camino completo.
2. Empezá por los **[Fundamentos](docs/fundamentos/README.md)**: lo que nadie explica porque "se da por sabido".
   1. [Archivos y carpetas](docs/fundamentos/01-archivos-y-carpetas.md)
   2. [El teclado y los atajos](docs/fundamentos/02-teclado-y-atajos.md)
   3. [Cómo funciona la web](docs/fundamentos/03-como-funciona-la-web.md)
   4. [¿Qué es programar?](docs/fundamentos/04-que-es-programar.md)
   5. [Visual Studio Code](docs/fundamentos/05-vs-code.md)
   6. [Rutas de archivos](docs/fundamentos/06-rutas-de-archivos.md)
   7. [Markdown](docs/fundamentos/07-markdown.md)
   8. [Cómo aprender, buscar y pedir ayuda](docs/fundamentos/08-aprender-y-pedir-ayuda.md)
   9. [Glosario](docs/fundamentos/09-glosario.md) 📖
3. Seguí las guías de Git **en orden**:
   0. [Preparar la compu](docs/git/00-preparar-la-compu.md)
   1. [La terminal sin miedo](docs/git/01-la-terminal.md)
   2. [¿Qué es Git y qué es GitHub?](docs/git/02-que-es-git.md)
   3. [Descargar este repo a tu compu (clonar)](docs/git/03-clonar-el-repo.md)
   4. [Guardar cambios (commit)](docs/git/04-guardar-cambios.md)
   5. [Subir y bajar cambios (push y pull)](docs/git/05-subir-y-bajar.md)
   6. [Ramas y Pull Requests: cómo entregar ejercicios](docs/git/06-ramas-y-pull-requests.md)
   7. [¡Socorro! Errores comunes](docs/git/07-errores-comunes.md)
   8. [Machete de comandos](docs/git/08-machete.md)
4. Antes de cada lenguaje, leé sus **conceptos clave**:
   [HTML](docs/html/conceptos-clave.md) · [CSS](docs/css/conceptos-clave.md) · [JavaScript](docs/javascript/conceptos-clave.md)
   · Etapa 2: [JavaScript moderno](docs/javascript-moderno/conceptos-clave.md) · [Node.js](docs/node/conceptos-clave.md) · [React](docs/react/conceptos-clave.md)
5. Hacé los ejercicios de la carpeta [`ejercicios/`](ejercicios/).
6. Marcá tu avance en [PROGRESO.md](PROGRESO.md).

---

## 📁 Cómo está organizado este repo

```
📦 Aprendizaje Repo
├── README.md            ← estás acá
├── PLAN.md              ← el plan de estudio semana por semana
├── PROGRESO.md          ← tu checklist de avance (lo vas completando vos)
├── GUIA-MENTOR.md       ← instrucciones para quien te enseña
├── docs/
│   ├── fundamentos/     ← las bases: archivos, teclado, web, programar, VS Code...
│   ├── git/             ← guías paso a paso de Git
│   ├── html/            ← conceptos clave de HTML
│   ├── css/             ← conceptos clave de CSS
│   ├── javascript/      ← conceptos clave de JavaScript
│   ├── javascript-moderno/  ← Etapa 2
│   ├── node/                ← Etapa 2
│   └── react/               ← Etapa 2
└── ejercicios/
    ├── 01-git/
    ├── 02-html/
    ├── 03-css/
    ├── 04-javascript/
    ├── 05-proyecto-final/
    ├── 06-javascript-moderno/       ← Etapa 2
    ├── 07-node/                     ← Etapa 2
    ├── 08-react/                    ← Etapa 2
    └── 09-proyecto-final-etapa-2/   ← Etapa 2
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
