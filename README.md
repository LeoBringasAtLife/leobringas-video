# leobringas.video

Landing page estatica para servicios de edicion de video.
El proyecto usa Tailwind CSS compilado localmente (sin CDN en produccion).

## Requisitos

- Node.js 18+ (recomendado: version LTS actual)
- npm

## Instalacion

```bash
npm install
```

## Scripts

### `npm run watch:css`

Compila Tailwind en modo observacion.
Usalo durante desarrollo para regenerar `assets/tailwind.css` automaticamente cada vez que cambies clases en `index.html`.

```bash
npm run watch:css
```

### `npm run build:css`

Genera una version minificada y optimizada de `assets/tailwind.css`.
Usalo antes de publicar/desplegar.

```bash
npm run build:css
```

## Estructura del proyecto

- `index.html`: pagina principal.
- `public/`: imagenes y archivos estaticos (ej: `public/leo.webp`, `public/leo.ico`).
- `src/tailwind.css`: archivo de entrada de Tailwind (`@import` + `@source`).
- `assets/tailwind.css`: CSS compilado que carga la web.

### Árbol de carpetas y archivos

```text
leobringas-video/
|-- assets/
|   `-- tailwind.css
|-- public/
|   |-- leo.ico
|   `-- leo.webp
|-- src/
|   `-- tailwind.css
|-- index.html
|-- package-lock.json
|-- package.json
`-- README.md
```

## Uso de imagenes en HTML

Referenciarlas con ruta relativa desde `index.html`, por ejemplo:

```html
<img src="public/leo.webp" alt="Leonardo Bringas">
<link rel="shortcut icon" href="public/leo.ico" type="image/x-icon">
```

## Nota de produccion

No se usa `cdn.tailwindcss.com` en runtime.
El CSS se genera localmente con Tailwind CLI para evitar warnings y mejorar estabilidad en produccion.
