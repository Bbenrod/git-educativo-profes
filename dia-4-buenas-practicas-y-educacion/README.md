# Día 4 – Buenas prácticas y trabajo profesional con Git

En esta práctica aplicarás una convención común en proyectos reales: **proteger archivos sensibles con `.gitignore`**, y manejar archivos de entorno con `.env` y `.env-example`.

---

## Objetivo

Simular un proyecto que utiliza variables de entorno sensibles y asegurar que **no se suban al repositorio**, mientras se comparte una plantilla (`.env-example`) para uso colaborativo.

---

## Pasos

1. Crea un nuevo repositorio en GitHub (puede ser con nombre como `entorno-seguro` o el que prefieras).

2. Clónalo en tu equipo y entra en la carpeta.

3. Crea un archivo llamado `.env` con variables de entorno. Ejemplo:

   ```env
   PORT=3000
   DB_HOST=localhost
   DB_USER=root
   DB_PASS=supersecreta
   API_KEY=123456789abcdef
   ```

4. Copia ese archivo y nómbralo `.env-example`, dejando los valores vacíos:

   ```env
   PORT=
   DB_HOST=
   DB_USER=
   DB_PASS=
   API_KEY=
   ```

5. Agrega ambos archivos y haz commit:

   ```bash
   git add .env .env-example
   git commit -m "Agrego archivos de entorno iniciales"
   git push
   ```

6. Crea un archivo `.gitignore` y añade:

   ```
   .env
   ```

7. Elimina `.env` del control de versiones y actualiza tu repositorio:

   ```bash
   git rm --cached .env
   git commit -m "Ignoro archivo .env y lo elimino del repo"
   git push
   ```

8. Verifica que el archivo `.env` sigue en tu equipo pero **ya no está en GitHub**.

---

> **Consejo:** Esta es una práctica estándar en el desarrollo profesional para proteger datos sensibles y permitir que otros configuren su entorno sin riesgos.
