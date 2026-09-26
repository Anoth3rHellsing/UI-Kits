# Neon Pulse v1.0.0 — Release Notes

**Sistema de diseño cyberpunk con neones, grid perspectivo y glassmorphism**  
Estética futurista oscura con acentos cyan/magenta, scanlines CRT y efectos glitch.

---

## ✨ Novedades

### 🎨 Identidad Visual
- Paleta de 15 tokens CSS con neones cyan (`#00f0ff`), magenta (`#ff00aa`), verde ácido (`#39ff14`)
- Fondo negro profundo con grid perspectivo (líneas cyan al 8%, 60×60px)
- Overlay de scanlines CRT con `repeating-linear-gradient`
- Viñeta radial oscura en bordes para enfocar el centro visual
- Barra de scanline animada vertical recorriendo la pantalla cada 3s

### 🧩 Componentes Incluidos
- **Card**: glassmorphism con `backdrop-filter: blur(12px)` y esquina diagonal cortada decorativa
- **Botón Primario Neon**: borde cyan transparente con glow intenso y text-shadow en hover
- **Botón Secundario Ghost**: transición a magenta con glow en hover
- **Variantes de botón**: magenta y green con sus respectivos glows
- **Input**: fondo oscuro con foco cyan y glow exterior
- **Badges/Tags**: 5 variantes de color (cyan, magenta, green, amber, red)
- **Progress Bar**: fill neon cyan con glow en borde derecho
- **Toggle Switch**: knob cuadrado con glow cyan en estado activo

### 🔤 Tipografía
- Display: Orbitron/Rajdhani uppercase con letter-spacing 2-4px
- Body: Rajdhani/Segoe UI para texto general
- Mono: Fira Code/Consolas para datos y código

### 🎬 Animaciones
- `npPulse`: glow pulsante en elementos activos (2s)
- `npFlicker`: parpadeo tipo neón al aparecer (0.15s)
- `npSlideUp`: entrada desde abajo con fade (0.4s)
- `npScanline`: línea de escaneo vertical continua (3s)
- `npGlitch`: distorsión glitch en hover de títulos (0.3s)

### 📱 Responsive
- Grid adaptativo: 4→3→2→1 columnas en breakpoints 1200/900/600px
- Padding y tamaños tipográficos ajustados por breakpoint
- Nav bottom bar en móvil (< 600px)

### ♿ Accesibilidad
- Contraste WCAG AA sobre fondo oscuro verificado
- Focus visible con outline cyan + glow
- Soporte `prefers-reduced-motion`: desactiva pulse/flicker/glitch/scanline
- No dependencia exclusiva del color para estados

### 🔧 Técnico
- Prefijo `.np-` en todas las clases para evitar colisiones
- Variables CSS customizables en `:root`
- Reset CSS incluido para aislamiento de estilos
- Sin dependencias externas ni JavaScript requerido

### 📦 Contenido del Paquete
- `neonpulse.css` — Estilos completos del sistema
- `DESIGN-SPEC.md` — Especificación técnica de tokens y componentes
- `CHANGELOG.md` — Historial de versiones
- `RELEASE-NOTES.md` — Este archivo

## 🖥️ Compatibilidad
- Navegadores modernos (Chrome, Firefox, Safari, Edge)
- Soporte para `backdrop-filter` (con fallback graceful)
- Sin dependencias externas ni JavaScript requerido

## 🚀 Uso Rápido
```html
<link rel="stylesheet" href="neonpulse.css">
<div class="np-reset">
  <div class="np-bg"></div>
  <div class="np-scanlines"></div>
  <div class="np-vignette"></div>
  <div class="np-container">
    <!-- tu contenido aquí -->
  </div>
</div>
```

---

*Neon Pulse v1.0.0 · Lanzamiento inicial · Septiembre 2026*