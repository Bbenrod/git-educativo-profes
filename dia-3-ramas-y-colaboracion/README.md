# Día 3 – Trabajo con ramas y colaboración

En esta práctica trabajarás con ramas, merges y colaboración en GitHub. Aprenderás a crear ramas, hacer cambios desde distintas ramas y resolver conflictos.

---

## Práctica 1: Crear ramas, trabajar en archivos y hacer merge a `main`

1. Crea una carpeta llamada `dia-3-ramas-y-colaboracion` dentro de tu repositorio local.

2. Haz commit para registrar la nueva carpeta:

   ```bash
   git add .
   git commit -m "Agrego carpeta para la práctica del día 3"
   ```

3. Crea y cambia a la rama `estructura-html`:

   ```bash
   git checkout -b estructura-html
   ```

4. Dentro de la carpeta `dia-3-ramas-y-colaboracion`, crea manualmente el archivo vacío `index.html`.

5. Haz commit:

   ```bash
   git add .
   git commit -m "Agrego index.html vacío"
   ```

6. Cambia a la rama `main` y luego crea la rama `estilos-css`:

   ```bash
   git checkout main
   git checkout -b estilos-css
   ```

7. Crea manualmente el archivo vacío `style.css` y haz commit:

   ```bash
   git add .
   git commit -m "Agrego style.css vacío"
   ```

8. Cambia a la rama `main` y luego crea la rama `logica-js`:

   ```bash
   git checkout main
   git checkout -b logica-js
   ```

9. Crea manualmente el archivo vacío `app.js` y haz commit:

   ```bash
   git add .
   git commit -m "Agrego app.js vacío"
   ```

10. Cambia a `main` y haz merge de las tres ramas, una por una:

```bash
git checkout main
git merge estructura-html
git merge estilos-css
git merge logica-js
```

11. Verifica que en la carpeta existan los tres archivos vacíos.

---

## Práctica 2: Conflictos al hacer merge de ramas

1. Asegúrate de estar en la carpeta `dia-3-ramas-y-colaboracion`.

2. Crea el archivo `info.md` y agrega el siguiente contenido:

   ```
   Proyecto de práctica Día 3
   ```

3. Haz commit y push:

   ```bash
   git add info.md
   git commit -m "Agrego info inicial en main"
   git push
   ```

4. Crea una nueva rama:

   ```bash
   git checkout -b edicion-info
   ```

5. Edita el archivo `info.md` y cambia el contenido por:

   ```
   Cambios desde la rama edicion-info
   ```

6. Haz commit:

   ```bash
   git add info.md
   git commit -m "Modifico info en edicion-info"
   ```

7. Cambia a la rama `main` y edita el archivo `info.md` nuevamente con un contenido distinto, por ejemplo:

   ```
   Cambios desde main
   ```

8. Haz commit:

   ```bash
   git add info.md
   git commit -m "Modifico info en main"
   ```

9. Intenta hacer merge de `edicion-info` en `main`:

   ```bash
   git merge edicion-info
   ```

10. Git mostrará un **conflicto**. Abre el archivo `info.md`, resuelve el conflicto manualmente, guarda los cambios y luego:

```bash
git add info.md
git commit -m "Resuelvo conflicto en info"
```
