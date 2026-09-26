# Neon Pulse — Changelog

## [1.0.0] — 2026-09-09

### Added
- Sistema de diseño cyberpunk completo con estética neón y glassmorphism
- Paleta de 15 tokens CSS (`--np-neon-cyan`, `--np-neon-magenta`, `--np-neon-green`, etc.)
- Fondo con grid perspectivo (líneas cyan al 8% de opacidad, 60×60px)
- Overlay de scanlines CRT con `repeating-linear-gradient`
- Viñeta radial oscura en bordes para enfocar el centro
- Barra de scanline animada vertical (`npScanline`, 3s)
- Componente Card con backdrop-filter blur(12px) y esquina diagonal cortada
- Botón Primario Neon con borde cyan, glow y text-shadow en hover
- Botón Secundario Ghost con transición a magenta en hover
- Variantes de botón: magenta, green con sus respectivos glows
- Input con fondo oscuro, foco cyan y glow
- Badges/Tags en 5 variantes de color (cyan, magenta, green, amber, red)
- Progress Bar con fill neon cyan y glow en borde derecho
- Toggle Switch cuadrado con knob cyan y glow en estado on
- Grid layout responsive con `auto-fill` y `minmax(280px, 1fr)`
- Tipografía display (Orbitron/Rajdhani) uppercase con letter-spacing 2-4px
- Tipografía mono (Fira Code/Consolas) para datos y código
- 5 animaciones: npPulse, npFlicker, npSlideUp, npScanline, npGlitch
- Reset CSS con prefijo `.np-reset` para aislamiento de estilos
- Soporte responsive: 4→3→2→1 columnas en breakpoints 1200/900/600px
- Accesibilidad: `prefers-reduced-motion`, focus-visible con outline cyan
- DESIGN-SPEC.md con especificación completa de tokens, componentes y animaciones