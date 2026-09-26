# Retro Wave — Changelog

## [1.0.0] — 2026-09-09

### Added
- Sistema de diseño synthwave/retrowave completo con estética outrun años 80
- Paleta de 15 tokens CSS (`--rw-sunset-1`, `--rw-neon-blue`, `--rw-neon-purple`, etc.)
- Fondo con gradiente vertical sunset (violeta → púrpura → negro profundo)
- Horizon Glow radial en la parte inferior simulando sol poniente
- Grid perspectivo 3D con `perspective(400px) rotateX(55deg)` y animación de scroll infinito
- Sol retro stripeado con `repeating-linear-gradient` horizontal y mask-image fade superior
- Animación `rwSunRotate` con hue-rotate sutil (20s)
- Sistema de estrellas/partículas con twinkle en mitad superior
- Texto Chrome metálico con `background-clip: text` y shine deslizante (`rwChromeShine`)
- Componente Card con esquinas rectas, stripe sunset superior de 3px y hover rosa neón
- Botón Primario con gradiente sunset pink→purple y glow intenso en hover
- Botón Secundario Outline con borde azul neón y glow en hover
- Botón Ghost con transición a rosa en hover
- Input con border-bottom sunset y foco azul neón
- Badges/Tags rectangulares en 4 variantes (pink, blue, purple, gold)
- Progress Bar con fill gradiente sunset y glow
- Toggle Switch cuadrado con track gradiente sunset en estado on
- Grid layout responsive con `auto-fill` y `minmax(280px, 1fr)`
- Tipografía display (Monoton/Bungee Shade/Orbitron) uppercase con letter-spacing 6px
- Tipografía mono retro (VT323/Press Start 2P) para datos y labels
- 6 animaciones: rwPulse, rwSlideUp, rwGridScroll, rwSunRotate, rwFlicker, rwChromeShine
- Reset CSS con prefijo `.rw-reset` para aislamiento de estilos
- Soporte responsive: 4→3→2→1 columnas en breakpoints 1200/900/600px
- Sol y grid floor ocultos en móvil (< 600px) para rendimiento
- Accesibilidad: `prefers-reduced-motion`, focus-visible con outline rosa
- Fallback para texto chrome en navegadores sin `background-clip: text`
- DESIGN-SPEC.md con especificación completa de tokens, gradientes y componentes