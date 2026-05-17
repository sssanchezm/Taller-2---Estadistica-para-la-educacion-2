# Modelos continuos

Proyecto Quarto en R sobre modelos continuos: normal, ji-cuadrado, t de Student, F de Fisher y Teorema del Limite Central.

La pagina principal del sitio es `index.html`. El documento fuente es `modelos_continuos.qmd` y tambien se conserva `modelos_continuos.html` como salida directa del render. La app interactiva aparece al final de la pagina, en la seccion **Laboratorio interactivo**. La app esta convertida con Shinylive, por lo que funciona en GitHub Pages sin servidor de R.

## Requisitos

- R 4.5 o superior
- Quarto
- Paquetes de R: `ggplot2`, `shiny` y `shinylive`
- Extension Quarto: `quarto-ext/shinylive`

Instalacion de paquetes:

```r
install.packages(c("ggplot2", "shiny", "shinylive"))
```

Instalacion de la extension:

```powershell
quarto add quarto-ext/shinylive
```

## Ejecutar localmente

Para revisar la pagina localmente:

```powershell
quarto preview modelos_continuos.qmd
```

Para generar el HTML:

```powershell
quarto render modelos_continuos.qmd
```

Despues de renderizar, si quieres que GitHub Pages abra directamente la pagina en la raiz del sitio, copia la salida a `index.html`:

```powershell
Copy-Item modelos_continuos.html index.html -Force
```

## Publicar en GitHub Pages

El repositorio debe subirse completo a GitHub con estos archivos y carpetas:

- `index.html`
- `modelos_continuos.html`
- `modelos_continuos.qmd`
- `modelos_continuos_files/`
- `_extensions/`
- `shinylive-sw.js`
- `Logo_UT.png` y `Logo_UT_monograma.png`
- `.nojekyll`

GitHub Pages debe configurarse desde la rama `main`, carpeta raiz `/`.

La app del laboratorio usa Shinylive: se ejecuta dentro del navegador con WebAssembly/webR, asi que puede ser interactiva en GitHub Pages.
