# Tratto Pastas — Web

Sitio estático (landing) de **Tratto Pastas** — pasta fresca artesanal en Montevideo.

🌐 Producción: https://pastastratto.com

## Stack

Sitio estático puro: un único `index.html` con CSS embebido + assets (imágenes, iconos PWA, `sitemap.xml`, `robots.txt`). **No requiere build.**

## Estructura

```
.
├── index.html          # Página principal (HTML + CSS inline)
├── tratto-logo.jpeg    # Logo
├── tratto-logo.webp    # Logo (formato moderno)
├── og-image.jpg        # Imagen para redes (Open Graph)
├── favicon.ico
├── apple-touch-icon.png
├── icon-192.png        # Iconos PWA
├── icon-512.png
├── robots.txt
├── sitemap.xml
└── netlify.toml        # Config de deploy
```

## Desarrollo local

Al ser estático, alcanza con abrir `index.html` en el navegador, o levantar un server simple:

```bash
npx serve .
```

## Deploy (CI/CD)

Conectado a **Netlify** con despliegue continuo:

- Cada `git push` a `main` → Netlify publica automáticamente.
- Los Pull Requests generan *deploy previews*.

No hay comando de build; Netlify publica la raíz del repo (ver `netlify.toml`).
