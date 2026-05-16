# Modelos continuos

Proyecto Quarto en R sobre modelos continuos: normal, ji-cuadrado, t de Student, F de Fisher y Teorema del Límite Central.

El documento principal es `modelos_continuos.qmd`. Incluye una app interactiva al final de la página, en la sección **Laboratorio interactivo**. La app está convertida con Shinylive, por lo que puede funcionar en GitHub Pages sin un servidor de R.

## Requisitos

- R 4.5 o superior
- Quarto
- Paquetes de R: `ggplot2`, `shiny` y `shinylive`
- Extensión Quarto: `quarto-ext/shinylive`

Puedes instalarlos con:

```r
install.packages(c("ggplot2", "shiny", "shinylive"))
```

La extensión se instala con:

```powershell
quarto add quarto-ext/shinylive
```

## Ejecutar localmente

Para revisar la página localmente:

```powershell
quarto preview modelos_continuos.qmd
```

Para generar el HTML:

```powershell
quarto render modelos_continuos.qmd
```

## Publicar en GitHub Pages

El repositorio puede subirse completo a GitHub con el `.qmd`, el HTML generado, `index.html`, `modelos_continuos_files/`, `_extensions/`, `shinylive-sw.js`, las imágenes y `.nojekyll`.

`index.html` redirige automáticamente a `modelos_continuos.html`, por lo que GitHub Pages abrirá la página principal al entrar a la URL del sitio.

La app del laboratorio usa Shinylive: se ejecuta dentro del navegador con WebAssembly/webR, así que puede ser interactiva en GitHub Pages.
