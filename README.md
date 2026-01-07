# pierodev-assets

Biblioteca simple de **assets (logos / banners / destacados)** para reutilizar en cualquier HTML (web o email) usando URLs públicas de **GitHub Pages**.

## Uso rápido

1) Activa GitHub Pages:
- Repo → **Settings → Pages**
- Source: **Deploy from a branch**
- Branch: **main**
- Folder: **/(root)**

2) Abre la galería:
- `https://piero7ov.github.io/pierodev-assets/`

3) Copia la URL desde la galería y úsala en tu HTML:

```html
<img src="https://piero7ov.github.io/pierodev-assets/brand/pierodev/logos/logo.png" alt="Logo">
```

## Agregar nuevas imágenes

1) Sube la imagen a una carpeta dentro de `brand/` (por ejemplo `brand/pierodev/logos/`, `brand/pierodev/banner/`, etc.)
2) Añade el item en `manifest.json` (nombre, path y tags)

> Tip: evita renombrar/mover archivos que ya estés usando en emails o páginas, para no romper URLs.

## Archivos clave
- `index.html` → galería (buscador + filtros + copiar URL/snippet)
- `manifest.json` → lista de imágenes que se muestran
- `.nojekyll` → evita comportamientos de Jekyll que a veces molestan con assets
