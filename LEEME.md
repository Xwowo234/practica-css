# FragHub — Sitio sobre Valorant (Práctica 3: Sitio CSS)

Cómo abrirlo: descomprime la carpeta y abre `index.html` directamente en el navegador (doble clic). No necesita servidor, Azure ni máquina virtual — es HTML y CSS puro.

## Cómo cumple cada requisito

**1. Layout**
- a/b. Header y footer en todas las páginas (`.site-header` / `.site-footer` en `styles.css`).
- c. Menú horizontal con 5 secciones (Agentes, Mapas, Armas, Modos de juego, Comunidad); es multinivel: cada sección despliega un submenú con sus 5 entradas al pasar el cursor.
- d. Menú vertical dentro de cada sección, con 5 entradas. En "Agentes" tiene un segundo nivel extra (`<details>`) para demostrar el multinivel.
- e. Responsividad con menú hamburguesa por debajo de 780px (ver media queries al final de `styles.css`).

**2. Grid** (todas en `styles.css`, buscar los comentarios "GRID PROPUESTA")
- Flexbox #1: `armas-todas-armas.html` (tarjetas iguales en fila).
- Flexbox #2: `modos-todos-modos.html` (tarjeta destacada con `flex:2`).
- CSS Grid #1: `agentes-todos-agentes.html` (`repeat(auto-fit, minmax())`).
- CSS Grid #2: `mapas-todos-mapas.html` (dos columnas fijas con `grid-template-columns: 1fr 1fr`).

**3. Contenido**
- 5 secciones en el menú horizontal, cada una con 5 entradas en su menú vertical (25 páginas de contenido + `index.html`).
- Cada entrada del menú vertical apunta a un HTML distinto.
- Elementos variados entre las páginas: tablas (estadísticas de armas, tier list, parches), imágenes (íconos SVG propios, sin usar arte oficial de Riot), enumeraciones (ordenadas y no ordenadas) y formularios (eventos, torneos, foro).

## Nota sobre las imágenes
No se usó ningún arte oficial de Riot Games/Valorant (evita derechos de autor). Los "íconos" de agentes/mapas/armas son gráficos SVG simples generados para este proyecto.

## Estructura de archivos
- `styles.css` — toda la hoja de estilos.
- `index.html` — inicio.
- `agentes-*.html`, `mapas-*.html`, `armas-*.html`, `modos-*.html`, `comunidad-*.html` — las 25 páginas de contenido.
