# Panel Uno 3D

Tienda de cómics con scroll 3D: un cómic que se abre y pasa las páginas, onomatopeyas que entran desde los costados y un carrusel de portadas reales. Modo claro/noche, sonido opcional y cursor propio.

**Stack:** Vite + React 19 + React Three Fiber + drei + postprocessing + Lenis.

## Correr
```bash
npm install
npm run dev          # desarrollo
npm run build        # producción (carpeta dist/)
npm run build:artifact   # un solo .html autocontenido
```
Probar niveles de calidad: `?tier=low|medium|high` en la URL.

## Datos
`src/data/comics.js` trae los 10 cómics de la base de datos de la tienda original (portadas en `src/data/covers/`). Si el backend de la tienda corre en `http://localhost:3001`, la web usa sus datos en vivo; si no, usa la copia embebida.

## Estructura
- `src/Sections.jsx`: contenido HTML de cada escena (`<section data-scene>`).
- `src/scroll/keyframes.js`: guion de escenas en números (un keyframe por escena).
- `src/three/`: escena 3D (cómic, onomatopeyas, carrusel, texturas generadas por código).
