# 02 · ¿Qué es Git y qué es GitHub?

## El problema

¿Alguna vez hiciste un trabajo práctico y terminaste con archivos así?

```
tp-final.docx
tp-final-v2.docx
tp-final-v2-corregido.docx
tp-final-AHORA-SI.docx
tp-final-AHORA-SI-definitivo(1).docx
```

Git resuelve exactamente eso. 🙌

---

## Git: la máquina de fotos

**Git** guarda "fotos" de tu proyecto cada vez que vos se lo pedís. Cada foto se llama **commit**.

```
📸 commit 1: "Creo la página de inicio"
    │
📸 commit 2: "Agrego mi foto"
    │
📸 commit 3: "Cambio el color del título"
```

Con eso podés:
- Ver **qué cambió** y **cuándo**.
- **Volver atrás** si rompiste algo.
- Trabajar con otras personas **sin pisarse**.

Tenés **un solo archivo** con todo su historial adentro, en vez de 15 copias.

---

## GitHub: el álbum en la nube

**GitHub** es una página web donde subís tu proyecto con toda su historia. Sirve para:
- Tener un **respaldo** (si se rompe la compu, no perdés nada).
- **Compartir** tu código y que otros lo revisen.
- Mostrar tu trabajo: ¡es como el Instagram de los programadores!

> Git es el programa. GitHub es un sitio web que usa Git.
> Es como la diferencia entre *la cámara* y *el álbum online*.

---

## Palabras que vas a escuchar mucho

| Palabra | Qué es | Analogía |
|---|---|---|
| **Repositorio (repo)** | Una carpeta de proyecto que Git está vigilando | Un álbum de fotos |
| **Commit** | Una foto guardada de tus cambios, con un mensaje | Una foto con epígrafe |
| **Rama (branch)** | Una línea de trabajo paralela | Un borrador aparte, para probar sin romper el original |
| **`main`** | La rama principal, la "versión oficial" | El documento final |
| **Remoto (`origin`)** | La copia del repo que está en GitHub | El álbum en la nube |
| **Clonar** | Descargar un repo de GitHub a tu compu (la primera vez) | Bajar el álbum |
| **Push** | Subir tus commits a GitHub | Subir fotos a la nube |
| **Pull** | Bajar de GitHub los cambios nuevos | Sincronizar el álbum |
| **Pull Request (PR)** | Pedir que tus cambios se sumen a `main` | Entregar el TP para que lo corrijan |

---

## Las 3 zonas de Git (importante 🧠)

Tus archivos pasan por tres lugares:

```
  📝 Carpeta de trabajo   ──git add──►   📦 Zona de preparación   ──git commit──►   📚 Historial
  (donde editás)                         (lo que va a entrar                         (las fotos
                                          en la próxima foto)                         guardadas)
```

1. **Editás** archivos normalmente en VS Code.
2. Con `git add` elegís **qué cambios** van a entrar en la foto (como acomodar a la gente antes de sacar la foto).
3. Con `git commit` **sacás la foto** y la guardás en el historial.
4. Con `git push` la **subís** a GitHub.

No hace falta entenderlo 100% ahora. Va a tener sentido cuando lo practiques.

---

Siguiente: [03 · Descargar este repo a tu compu](03-clonar-el-repo.md)
