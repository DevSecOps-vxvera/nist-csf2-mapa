# Mapa interactivo NIST CSF 2.0

Sitio estático, editable y listo para publicar con GitHub Pages. No requiere compilación, servidor, claves, servicios externos ni paquetes. Abre `index.html` para explorar el mapa. El directorio contiene `index.html`, `styles.css`, `app.js` y `data.js`.

## Contenido

- Seis funciones, 22 categorías y 106 subcategorías/resultados del CSF 2.0.
- Búsqueda por tema e identificador; tarjetas de función y categorías desplegables.
- Tres ejemplos contextuales por resultado: industria, financiero y retail.
- Diseño adaptable a pantallas pequeñas y navegación sin conexión.

**Precisión de términos:** NIST CSF 2.0 es una taxonomía de resultados deseados (Core), organizada en funciones, categorías y subcategorías. No prescribe un catálogo obligatorio de controles ni la forma de lograr cada resultado. Los ejemplos sectoriales fueron redactados para este recurso con finalidad didáctica; son ilustrativos, hipotéticos y no constituyen requisitos de NIST ni asesoría regulatoria.

## Fuentes

- NIST, *The NIST Cybersecurity Framework (CSF) 2.0*, CSWP 29 (2024): https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.29.pdf
- NIST CSF 2.0 Reference Tool: https://csrc.nist.gov/projects/cybersecurity-framework/filters
- NIST Cybersecurity Framework FAQs: https://www.nist.gov/cyberframework/faqs

Los textos de resultado en español son resúmenes/traducciones editoriales del Core oficial. Consultar la publicación para el texto oficial y las herramientas NIST para ejemplos de implementación e informative references actualizadas.

## Publicar con GitHub Pages (macOS)

### Opción A: crear un repositorio con GitHub CLI

1. Instala GitHub CLI si no está instalado: `brew install gh`.
2. En Terminal, entra al directorio del sitio (si lo acabas de descomprimir, reemplaza la ruta):

   ```sh
   cd "$HOME/Downloads/nist-csf2-mapa"
   ```

3. Inicia sesión y crea el repositorio:

   ```sh
   gh auth login
   git init
   git add .
   git commit -m "Publica mapa interactivo NIST CSF 2.0"
   git branch -M main
   gh repo create nist-csf2-mapa --public --source=. --remote=origin --push
   ```

4. Habilita el sitio en GitHub: repositorio → **Settings** → **Pages** → **Build and deployment** → **Deploy from a branch** → rama `main`, carpeta `/ (root)` → **Save**.
5. Cuando el despliegue termine, la dirección aparece en **Settings → Pages**. En un repositorio público con ese nombre suele ser `https://TU-USUARIO.github.io/nist-csf2-mapa/`.

### Opción B: usar un repositorio existente

```sh
cd "$HOME/Downloads/nist-csf2-mapa"
git init
git add .
git commit -m "Publica mapa interactivo NIST CSF 2.0"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/TU-REPOSITORIO.git
git push -u origin main
```

Después selecciona `main` y `/ (root)` en **Settings → Pages**. Si el repositorio ya tiene archivos o historial, clónalo y copia los cuatro archivos del sitio dentro de esa carpeta antes de ejecutar `git add`, `commit` y `push`.

Para actualizar más adelante, desde la carpeta local:

```sh
git add .
git commit -m "Actualiza el mapa CSF 2.0"
git push
```

El nombre `TU-USUARIO` es tu usuario real de GitHub. No uses una URL de repositorio ajena. GitHub Pages puede tardar unos minutos en publicar después del primer despliegue.
