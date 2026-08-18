# Portfolio

Portfolio estático (HTML + CSS puro, sin frameworks ni build step), con la
misma identidad visual del [CV online](https://ainaragil.github.io/curriculum/):
paleta beige/negro/rosa/verde/naranja, nav en píldora, headers de sección en
píldora y tipografías Manrope + Playfair Display italic.

## Estructura

```
index.html                                   → portada con grilla de proyectos
proyecto-rediseno-web-corporativa.html        → vista de detalle de un proyecto
proyecto-identidad-evento-blockchain.html     → vista de detalle de otro proyecto
proyecto-landing-fintech.html                 → vista de detalle de otro proyecto
assets/css/styles.css                         → todos los estilos
assets/img/covers/                            → portadas para las cards
assets/img/shots/<proyecto>/                  → imágenes de cada proyecto
```

Todas las imágenes son placeholders en SVG generados a modo de ejemplo.
Reemplazalas por tus capturas reales manteniendo el mismo nombre de archivo,
o cambiá la ruta en el HTML.

## Editar contenido

- **Textos e info personal**: abrí `index.html` y reemplazá "Tu Nombre", el
  texto del hero, la intro, "Sobre mí" y los links de contacto (LinkedIn,
  email, Instagram).
- **Cada proyecto**: abrí su archivo `proyecto-*.html` y editá título,
  resumen, metadatos (`cliente`, `rol`, `año`, `herramientas`) y los
  párrafos de cada bloque de texto.

## Cómo funciona la vista de proyecto

Cada página de proyecto es una sola sección que scrollea de corrido,
armada con bloques que podés combinar como quieras:

- `project-block--full` → una imagen sola, ancho completo (como en Behance).
- `project-block--two-col` → dos imágenes lado a lado.
- `project-block--text` → un bloque de texto (para contar proceso, contexto, etc.).

Copiá y pegá los bloques que necesites, en el orden que quieras, dentro del
`<main>` de cada página de proyecto.

## Agregar un proyecto nuevo

1. Duplicá uno de los archivos `proyecto-*.html` y renombralo
   (ej: `proyecto-mi-nuevo-proyecto.html`).
2. Editá su contenido y las rutas de las imágenes.
3. En `index.html`, copiá un bloque `<a class="card">...</a>` dentro de
   `.projects__grid` y apuntá el `href` al nuevo archivo.
4. Sumá una portada en `assets/img/covers/` y las imágenes del proyecto en
   `assets/img/shots/<nombre-del-proyecto>/`.

## Subir a GitHub Pages

1. Creá un repositorio nuevo en GitHub (por ejemplo `portfolio`).
2. Subí todos estos archivos a la raíz del repo (respetando la carpeta
   `assets/`).
3. En el repo: **Settings → Pages → Source**, elegí la rama `main` y la
   carpeta `/ (root)`.
4. En un par de minutos tu portfolio queda publicado en:
   `https://tu-usuario.github.io/portfolio/`

Si preferís que la web quede en `https://tu-usuario.github.io/` directo
(sin `/portfolio`), llamá al repositorio `tu-usuario.github.io`.
