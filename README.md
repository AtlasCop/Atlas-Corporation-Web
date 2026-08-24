# Atlas Corporation — Landing Page

Landing page de Atlas Corporation: un único archivo `index.html` estático, con [Tailwind CSS](https://tailwindcss.com/) vía CDN. No requiere build ni dependencias de Node para funcionar en producción.

## Estructura

```
index.html      Página completa (markup + estilos Tailwind + JS del fondo interactivo)
assets/         Imágenes usadas por la página (logo, robot, fondo de circuito)
```

## Desarrollo local

Al ser un sitio estático, basta con servirlo con cualquier servidor HTTP simple:

```bash
python -m http.server 8000
# o
npx serve .
```

Luego abre `http://localhost:8000`.

> Abrir `index.html` directamente con doble clic (`file://`) también funciona, salvo por el efecto de brillo interactivo del fondo del hero, que necesita `http://` para leer los píxeles del canvas sin restricciones de seguridad del navegador.

## Despliegue en Vercel

Este proyecto no necesita configuración especial: es un sitio 100% estático.

1. Sube el repositorio a GitHub (ver abajo).
2. En [vercel.com](https://vercel.com), **Add New → Project** e importa el repositorio.
3. Framework Preset: **Other** (o "Static"). No hay comando de build ni carpeta de salida que configurar — Vercel servirá `index.html` tal cual.
4. Deploy.

Cada push a la rama principal generará un nuevo deploy automáticamente.

## Subir a GitHub

```bash
git remote add origin https://github.com/<tu-usuario>/<tu-repo>.git
git branch -M main
git push -u origin main
```
