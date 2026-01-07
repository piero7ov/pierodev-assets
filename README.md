# pierodev-assets 📚

Biblioteca simple de **assets (logos / banners / destacados)** para reutilizar en cualquier HTML (web o email) usando URLs públicas de **GitHub Pages**.

## ✅ Activar GitHub Pages

Repo → **Settings → Pages**
- Source: **Deploy from a branch**
- Branch: **main**
- Folder: **/(root)**

Luego abre:
- `https://piero7ov.github.io/pierodev-assets/`

## 🚀 Uso rápido

### 1) En HTML (img)
```html
<img src="https://piero7ov.github.io/pierodev-assets/brand/pierodev/logos/logo.png" alt="Logo">
````

### 2) En CSS (background)

```css
.hero{
  background: url("https://piero7ov.github.io/pierodev-assets/brand/pierodev/banner/banner1.png") center/cover no-repeat;
}
```

> Tip: en correos, algunos clientes bloquean imágenes por defecto; es normal que el usuario deba dar “Mostrar imágenes”.

## ➕ Agregar nuevas imágenes

1. Sube la imagen dentro de `brand/` (ej: `brand/pierodev/logos/`, `brand/pierodev/banner/`, etc.)
2. Añade el item en `manifest.json`:

   * `name`
   * `path`
   * `tags`
   * (recomendado) `category` y `email_width`
   * `notes` (opcional pero útil)

Ejemplo:

```json
{
  "name": "Logo blanco (PNG)",
  "path": "brand/pierodev/logos/logo-white.png",
  "category": "logos",
  "tags": ["logo", "white", "png", "email"],
  "notes": "Ideal para fondo oscuro.",
  "email_width": 220
}
```

## ⚠️ Buenas prácticas (para no romper URLs)

* Evita **renombrar o mover** archivos ya publicados (rompe enlaces).
* Si necesitas cambios, sube una versión nueva:

  * `logo.png` → `logo-v2.png`
* Si una imagen tarda en actualizar por caché:

  * usa `?v=2` en la URL (solo para pruebas).

## Archivos clave

* `index.html` → galería (buscador + filtros + copiar URL/snippets)
* `manifest.json` → lista de imágenes que se muestran
* `.nojekyll` → evita comportamientos de Jekyll que a veces molestan con assets

