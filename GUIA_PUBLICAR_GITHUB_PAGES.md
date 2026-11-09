# Publicar en GitHub Pages desde Mac

1. Descarga y descomprime `nist-csf2-mapa.zip`.
2. Abre Terminal y cambia al directorio descargado:

   ```sh
   cd "$HOME/Downloads/nist-csf2-mapa"
   ```

3. Para crear un repositorio nuevo, instala GitHub CLI (una sola vez) e inicia sesión:

   ```sh
   brew install gh
   gh auth login
   ```

4. Publica la carpeta desde Terminal:

   ```sh
   git init
   git add .
   git commit -m "Publica mapa interactivo NIST CSF 2.0"
   git branch -M main
   gh repo create nist-csf2-mapa --public --source=. --remote=origin --push
   ```

5. En GitHub, abre el repositorio y ve a **Settings → Pages**.
6. En **Build and deployment**, elige **Deploy from a branch**, selecciona `main` y `/(root)`, y guarda.
7. Espera a que GitHub muestre la dirección del sitio en la sección Pages. Tendrá este formato: `https://TU-USUARIO.github.io/nist-csf2-mapa/`.

Para subir cambios luego, vuelve a esta carpeta y ejecuta:

```sh
git add .
git commit -m "Actualiza el mapa"
git push
```

Si ya tienes el repositorio, clónalo primero con `git clone https://github.com/TU-USUARIO/TU-REPOSITORIO.git`, copia el contenido del sitio en la carpeta clonada y realiza el `add`, `commit` y `push`. Sustituye `TU-USUARIO` por tu usuario de GitHub.
