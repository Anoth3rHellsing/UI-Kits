# Neon Pulse — UI Kit Specification

Sistema de diseño cyberpunk oscuro con neones, efectos de brillo y estética futurista.
Fondo negro profundo con grid perspectivo, tarjetas glassmorphism y acentos en cyan/magenta/verde ácido.

---

## Paleta de colores

| Token | Hex | Uso |
|-------|-----|-----|
| `--np-bg` | `#0a0a0f` | Fondo base |
| `--np-bg-card` | `rgba(15,15,25,.85)` | Tarjetas, paneles |
| `--np-bg-elevated` | `rgba(20,20,35,.9)` | Superficies elevadas |
| `--np-neon-cyan` | `#00f0ff` | Acento primario, enlaces, activos |
| `--np-neon-magenta` | `#ff00aa` | Acento secundario, hover, destacados |
| `--np-neon-green` | `#39ff14` | Éxito, estados positivos |
| `--np-neon-amber` | `#ffaa00` | Advertencias |
| `--np-neon-red` | `#ff2244` | Errores, destructivo |
| `--np-text` | `#e8e8f0` | Texto principal |
| `--np-text-sec` | `rgba(232,232,240,.7)` | Texto secundario |
| `--np-text-muted` | `rgba(232,232,240,.4)` | Hints, placeholders |
| `--np-border` | `rgba(0,240,255,.15)` | Bordes sutiles |
| `--np-border-active` | `rgba(0,240,255,.6)` | Bordes activos/focus |
| `--np-glow-cyan` | `0 0 20px rgba(0,240,255,.4)` | Glow cyan estándar |
| `--np-glow-magenta` | `0 0 20px rgba(255,0,170,.4)` | Glow magenta estándar |

## Tipografía

- **Familia:** `'Orbitron', 'Rajdhani', 'Segoe UI', monospace` (fallback chain)
- **Headings:** Orbitron o Rajdhani Bold, uppercase, letter-spacing 2-4px
- **Body:** Rajdhani o Segoe UI Regular
- **Mono:** `'Fira Code', 'Consolas', monospace` para código y datos

| Estilo | Tamaño | Peso | Letter-spacing | Uso |
|--------|--------|------|----------------|-----|
| H1 | 32px | Bold | 4px | Títulos de página |
| H2 | 22px | SemiBold | 3px | Secciones |
| H3 | 16px | SemiBold | 2px | Subsecciones |
| Body | 14px | Regular | 0.5px | Texto general |
| Small | 11px | Regular | 1px | Labels, metadata |
| Mono | 13px | Regular | 0 | Código, datos |

## Fondo

### Grid perspectivo
Líneas horizontales y verticales con perspectiva 3D, color cyan al 8% de opacidad:
```css
background-image:
  linear-gradient(rgba(0,240,255,.08) 1px, transparent 1px),
  linear-gradient(90deg, rgba(0,240,255,.08) 1px, transparent 1px);
background-size: 60px 60px;
```

### Scanlines
Overlay sutil de líneas horizontales para efecto CRT:
```css
background: repeating-linear-gradient(
  0deg, transparent, transparent 2px,
  rgba(0,0,0,.15) 2px, rgba(0,0,0,.15) 4px
);
```

### Viñeta
Gradiente radial oscuro en bordes para enfocar el centro:
```css
background: radial-gradient(ellipse at center, transparent 50%, rgba(0,0,0,.6) 100%);
```

## Componentes

### Card (tarjeta)
```
border-radius: 4px
background: var(--np-bg-card)
border: 1px solid var(--np-border)
backdrop-filter: blur(12px)
box-shadow: 0 4px 24px rgba(0,0,0,.5)
```
**Hover:** borde cyan activo, glow cyan sutil, translateY(-2px).
**Esquina decorativa:** línea diagonal cortada en esquina superior derecha (clip-path o pseudo-elemento).

### Botón Primario (Neon)
```
border-radius: 2px
background: transparent
border: 1px solid var(--np-neon-cyan)
color: var(--np-neon-cyan)
text-transform: uppercase
letter-spacing: 2px
box-shadow: var(--np-glow-cyan), inset 0 0 10px rgba(0,240,255,.1)
```
**Hover:** fondo cyan al 15%, glow intenso, text-shadow cyan.
**Active:** scale(0.97), glow reducido.

### Botón Secundario (Ghost)
```
border: 1px solid rgba(232,232,240,.2)
color: var(--np-text-sec)
```
**Hover:** borde magenta, color magenta, glow magenta.

### Input
```
background: rgba(0,0,0,.4)
border: 1px solid var(--np-border)
border-radius: 2px
color: var(--np-text)
```
**Focus:** borde cyan, glow cyan, scanline animation en el borde inferior.

### Badge / Tag
Pill pequeño con borde neon y texto uppercase 10px. Variante por color (cyan, magenta, green, amber, red).

### Progress Bar
Track oscuro con fill neon cyan animado. Glow en el borde derecho del fill.

### Toggle Switch
Track oscuro, knob cuadrado con borde cyan. Estado on: track cyan al 30%, knob cyan sólido con glow.

## Animaciones

| Nombre | Duración | Uso |
|--------|----------|-----|
| `npPulse` | 2s | Glow pulsante en elementos activos |
| `npFlicker` | 0.15s | Parpadeo tipo neon al aparecer |
| `npSlideUp` | 0.4s | Entrada desde abajo |
| `npScanline` | 3s | Línea de escaneo vertical |
| `npGlitch` | 0.3s | Distorsión glitch en hover de títulos |

## Responsive

| Breakpoint | Comportamiento |
|------------|---------------|
| > 1200px | Grid 4 columnas, sidebar visible |
| 900-1200px | Grid 3 columnas |
| 600-900px | Grid 2 columnas, sidebar colapsada |
| < 600px | Grid 1 columna, nav bottom bar |

## Accesibilidad

- Contraste mínimo WCAG AA sobre fondo oscuro
- Focus visible con outline cyan + glow
- `prefers-reduced-motion`: desactivar pulse/flicker/glitch
- No depender solo del color para estados (usar iconos + texto)