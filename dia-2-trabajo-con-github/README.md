# Día 2 – Trabajo con GitHub

En esta práctica trabajarás con repositorios remotos en GitHub. Crearás y conectarás repositorios tanto **desde lo local hacia lo remoto**, como **desde lo remoto hacia lo local**.

## Archivos a usar

- `index.html`
- `style.css`

Disponibles en: `/dia-2-trabajo-con-github`

---

## Flujo 1: Crear un repositorio local y conectarlo a GitHub

1. Asegúrate de tener una carpeta con los archivos `index.html` y `style.css`.
2. Abre esa carpeta en tu terminal.
3. Ejecuta los comandos que GitHub te proporciona al crear un nuevo repositorio (puedes copiarlos directamente después de hacer clic en **"Create repository"** sin README).
   Generalmente se ven así:

   ```bash
   git init
   git add .
   git commit -m "Primer commit"
   git branch -M main
   git remote add origin https://github.com/usuario/nombre-del-repo.git
   git push -u origin main
   ```

---

## Flujo 2: Clonar un repositorio remoto, modificar y subir cambios

1. Clona un repositorio existente:

   ```bash
   git clone https://github.com/usuario/otro-repo.git
   ```

2. Entra a la carpeta clonada.

3. Abre y edita los archivos `index.html` o `style.css` (agrega datos, estructura o estilos).

4. Guarda tus cambios y haz un commit:

   ```bash
   git add .
   git commit -m "Agrego información a la página"
   ```

5. Sube los cambios al repositorio remoto:

   ```bash
   git push
   ```

---

## Flujo 3: Crear, subir archivo, modificar en GitHub y actualizar local con pull

1. En tu repositorio local, crea un archivo llamado `material-compartido.txt` con algún contenido inicial.

2. Haz commit y push para subirlo a GitHub:

   ```bash
   git add material-compartido.txt
   git commit -m "Agrego archivo material-compartido.txt inicial"
   git push
   ```

3. En GitHub, abre el repositorio y edita directamente el archivo `material-compartido.txt` (desde la interfaz web).

4. Guarda los cambios haciendo commit en GitHub.

5. Regresa a tu terminal, dentro de la carpeta local del repositorio.

6. Ejecuta para traer los cambios desde GitHub a tu local:

   ```bash
   git pull
   ```

7. Observa que el archivo `material-compartido.txt` en tu local se actualizó con los cambios que hiciste desde GitHub.

---

> **Consejo:** Usa repositorios remotos diferentes para practicar cada flujo y evitar conflictos.
