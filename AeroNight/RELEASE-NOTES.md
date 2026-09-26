# AeroNight v1.0.0 — Release Notes

**Sistema de diseño oscuro inspirado en Wii Menu / Wii Shop Channel**  
Fondo azul profundo con ondas animadas, tiles glossy y glow cyan.

---

## ✨ Novedades

### 🎨 Identidad Visual
- Paleta de 11 tokens CSS con fondo radial elíptico (`#051525` → `#1a4a7a`)
- Ondas SVG animadas en 2 capas (12s y 18s, direcciones opuestas)
- Sistema de partículas/estrellas con animación `twinkle`
- Gradientes de iconos en 6 colores con overlay glossy superior

### 🧩 Componentes Incluidos
- **Channel Tile**: cuadrícula de canales con hover `scale(1.08)` y estado activo con glow cyan intenso
- **Selected Channel Panel**: icono 180×180px, título, descripción y botón de descarga
- **Botón de Descarga**: gradiente cyan→azul con glow y efecto press
- **Control de Audio**: pill con barras animadas y toggle play/pause
- **Search Overlay**: modal con `backdrop-filter: blur(8px)` y foco neon
- **Barra Inferior**: logo itálica con glow, reloj en tiempo real, botones circulares

### 📱 Responsive
- Layout horizontal (45%/55%) en escritorio
- Colapso vertical automático en pantallas < 900px
- Tiles adaptables con `minmax(140px, 1fr)` → `minmax(100px, 1fr)`

### ♿ Accesibilidad
- Contraste WCAG AA sobre fondos oscuros
- Focus visible con outline cyan
- Soporte `prefers-reduced-motion` para desactivar animaciones

### 🔧 Técnico
- Prefijo `.an-` en todas las clases para evitar colisiones
- Variables CSS customizables en `:root`
- Reset CSS incluido para aislamiento de estilos
- Documentación completa en DESIGN-SPEC.md

---

## 📦 Contenido del Paquete
- `aeronight.css` — Estilos completos del sistema
- `DESIGN-SPEC.md` — Especificación técnica de tokens y componentes
- `CHANGELOG.md` — Historial de versiones

## 🖥️ Compatibilidad
- Navegadores modernos (Chrome, Firefox, Safari, Edge)
- Soporte para `backdrop-filter` (con fallback graceful)
- Sin dependencias externas ni JavaScript requerido

## 🚀 Uso Rápido
```html
<link rel="stylesheet" href="aeronight.css">
<div class="an-reset">
  <div class="an-bg"><!-- ondas y estrellas --></div>
  <div class="an-container">
    <!-- tu contenido aquí -->
  </div>
</div>
```

---

*AeroNight v1.0.0 · Lanzamiento inicial · Septiembre 2026*