# Retro Wave v1.0.0 — Release Notes

**Sistema de diseño synthwave/retrowave con estética outrun años 80**  
Gradientes sunset rosa-azul-violeta, grid perspectivo infinito, sol retro stripeado y texto chrome metálico.

---

## ✨ Novedades

### 🎨 Identidad Visual
- Paleta de 15 tokens CSS con sunset pink (`#ff6ec7`), naranja (`#ff9a56`), dorado (`#ffd700`), azul neón (`#00d4ff`) y violeta (`#b026ff`)
- Fondo con gradiente vertical sunset (violeta → púrpura → negro profundo)
- Horizon Glow radial en la parte inferior simulando sol poniente
- Grid perspectivo 3D con `perspective(400px) rotateX(55deg)` y scroll infinito hacia el espectador
- Sol retro stripeado horizontal con mask-image fade superior y animación hue-rotate sutil
- Sistema de estrellas/partículas con twinkle en mitad superior del viewport

### 🔤 Tipografía Chrome
- Texto Display metálico con `background-clip: text` y gradiente blanco→plateado
- Efecto shine deslizante sobre texto chrome (`rwChromeShine`, 3s)
- Fallback legible para navegadores sin soporte `background-clip`
- Tipografía mono retro (VT323/Press Start 2P) para datos y labels

### 🧩 Componentes Incluidos
- **Card**: esquinas rectas retro con stripe sunset de 3px en borde superior y hover rosa neón
- **Botón Primario Sunset**: gradiente pink→purple con glow intenso y brightness en hover
- **Botón Secundario Outline**: borde azul neón con glow y fondo translúcido en hover
- **Botón Ghost**: transición a rosa con glow sutil en hover
- **Input**: border-bottom sunset con foco azul neón y glow exterior
- **Badges/Tags**: rectangulares (sin border-radius) en 4 variantes (pink, blue, purple, gold)
- **Progress Bar**: fill gradiente sunset con glow continuo
- **Toggle Switch**: track gradiente sunset en estado on, knob blanco con glow rosa

### 🎬 Animaciones
- `rwPulse`: glow pulsante rosa/violeta en elementos activos (2.5s)
- `rwSlideUp`: entrada desde abajo con fade (0.5s)
- `rwGridScroll`: grid perspectivo moviéndose infinitamente hacia el espectador (4s)
- `rwSunRotate`: rotación lenta del sol retro con hue-rotate (20s)
- `rwFlicker`: parpadeo sutil tipo neón viejo (3s)
- `rwChromeShine`: brillo deslizante sobre texto chrome metálico (3s)

### 📱 Responsive
- Grid adaptativo: 4→3→2→1 columnas en breakpoints 1200/900/600px
- Sol y grid floor ocultos en móvil (< 600px) para rendimiento
- Tamaños tipográficos y padding ajustados por breakpoint

### ♿ Accesibilidad
- Contraste WCAG AA sobre fondos oscuros verificado
- Focus visible con outline rosa + glow
- Soporte `prefers-reduced-motion`: desactiva pulse/flicker/grid-scroll/sun/chrome-shine
- Fallback de texto chrome para navegadores sin `background-clip: text`
- No dependencia exclusiva del color para estados

### 🔧 Técnico
- Prefijo `.rw-` en todas las clases para evitar colisiones
- Variables CSS customizables en `:root`
- Reset CSS incluido para aislamiento de estilos
- Sin dependencias externas ni JavaScript requerido
- Mask-image con prefijo `-webkit-` para compatibilidad Safari

### 📦 Contenido del Paquete
- `retrowave.css` — Estilos completos del sistema
- `DESIGN-SPEC.md` — Especificación técnica de tokens, gradientes y componentes
- `CHANGELOG.md` — Historial de versiones
- `RELEASE-NOTES.md` — Este archivo

## 🖥️ Compatibilidad
- Navegadores modernos (Chrome, Firefox, Safari, Edge)
- Soporte para `backdrop-filter`, `mask-image` y `background-clip: text`
- Fallback graceful para navegadores sin soporte de propiedades avanzadas
- Sin dependencias externas ni JavaScript requerido

## 🚀 Uso Rápido
```html
<link rel="stylesheet" href="retrowave.css">
<div class="rw-reset">
  <div class="rw-bg">
    <div class="rw-horizon"></div>
    <div class="rw-grid-floor"></div>
    <div class="rw-sun"></div>
    <div class="rw-stars"></div>
  </div>
  <div class="rw-container">
    <!-- tu contenido aquí -->
  </div>
</div>
```

---

*Retro Wave v1.0.0 · Lanzamiento inicial · Septiembre 2026*