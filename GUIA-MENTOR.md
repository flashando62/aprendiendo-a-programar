# 🧑‍🏫 Guía para el mentor

Instrucciones para quien arma el repo y acompaña a la alumna.

---

## 1. Subir el repo a GitHub (una sola vez)

1. En GitHub: **New repository** → nombre (ej. `aprendiendo-a-programar`) → **Public** →
   **sin** README, .gitignore ni licencia (ya están acá) → *Create repository*.
2. En la carpeta de este proyecto:

```bash
git init -b main
git add .
git commit -m "Estructura inicial del curso"
git remote add origin https://github.com/TU-USUARIO/aprendiendo-a-programar.git
git push -u origin main
```

## 2. Darle acceso a la alumna

1. Ella crea su cuenta de GitHub (guía [00](docs/git/00-preparar-la-compu.md)) y te pasa su usuario.
2. En el repo: **Settings → Collaborators → Add people** → su usuario.
3. Ella acepta la invitación (le llega por mail o en https://github.com/notifications).

> Así puede hacer `push` directo al repo, sin necesidad de *fork*. Es más simple para empezar.

## 3. Proteger la rama `main` (recomendado)

Para que todo pase por Pull Request y puedas revisar:

**Settings → Branches → Add branch ruleset** (o *Add rule*) sobre `main`:
- ✅ Require a pull request before merging
- ✅ Require approvals: 1
- ✅ Block force pushes

> Si en algún momento esto la frustra demasiado al principio, se puede activar recién
> después del ejercicio git-03. Lo importante es que el hábito del Pull Request quede.

## 4. Cómo revisar un Pull Request

1. Pestaña **Pull requests** → abrir el de ella.
2. Pestaña **Files changed** → podés dejar comentarios en cualquier línea con el `+` azul.
3. Al terminar: **Review changes** →
   - *Comment*: solo comentarios
   - *Request changes*: tiene que corregir algo (ella hace nuevos commits en la misma rama y se actualiza solo)
   - *Approve*: todo bien
4. Aprobado → **Merge pull request** (lo puede hacer ella, así aprende).

### Consejos para la revisión
- Empezá siempre por algo que esté **bien**. La motivación es lo más importante al principio.
- Máximo 2 o 3 correcciones por PR. Si hay más, elegí las más importantes.
- Preguntá en vez de afirmar: *"¿Qué pasa si el número es negativo?"* enseña más que *"falta validar negativos"*.
- No le escribas la solución: dale una pista o un link a MDN.
- Celebrá los hitos: primer commit, primer PR, primera página publicada.

### 🔒 Privacidad
El repo es público. En cada revisión fijate que no haya datos sensibles (dirección, teléfono, DNI,
fecha de nacimiento, fotos que ella no quiera exponer). Si algo se subió por error, borrarlo en un
commit nuevo **no alcanza** (queda en el historial): avisá y se limpia con ayuda.

## 5. Ritmo sugerido

- Una **charla semanal** corta (30 min): qué aprendió, qué le costó, qué sigue.
- Revisar los PRs dentro de las 24–48 h para que no pierda el envión.
- Si se traba más de 30 minutos con algo, que pregunte. Si se traba 5 minutos, que siga intentando.

## 6. Etapa 2 (Node.js y React)

- No arrancar hasta que maneje con soltura funciones, arrays, objetos y el DOM. Si React "no le entra",
  casi siempre el problema es JavaScript base: volver a jsm-01.
- Al revisar PRs de Node/React, lo primero: que **no** haya `node_modules` ni `.env` en *Files changed*
  (el `.gitignore` los excluye, pero conviene verificarlo).
- Para probar sus PRs: `git fetch`, `git switch RAMA`, entrar a `solucion/`, `npm install` y `npm run dev`.
- En el proyecto final de la etapa 2, pedile el `PLAN.md` y aprobalo **antes** de que empiece a programar,
  y que trabaje con varias ramas chicas en vez de un PR gigante.

## 7. Publicar el proyecto final con GitHub Pages

**Settings → Pages → Source: Deploy from a branch → Branch: `main`, carpeta `/ (root)`** → Save.

El portfolio quedará en:
`https://TU-USUARIO.github.io/aprendiendo-a-programar/ejercicios/05-proyecto-final/solucion/`

(También puede crear después su propio repo `SU-USUARIO.github.io` para tener una URL más linda.)
