# Retro Wave — UI Kit Specification

Sistema de diseño synthwave/retrowave con gradientes rosa-azul-violeta, tipografía retro futurista,
grid perspectivo estilo años 80 y efectos de brillo neón suave. Estética "outrun" con horizontes infinitos.

---

## Paleta de colores

| Token | Hex | Uso |
|-------|-----|-----|
| `--rw-bg-deep` | `#0d0221` | Fondo más oscuro (horizonte inferior) |
| `--rw-bg-mid` | `#1a0533` | Fondo medio |
| `--rw-bg-top` | `#2b1055` | Fondo superior |
| `--rw-sunset-1` | `#ff6ec7` | Rosa brillante (acentos primarios) |
| `--rw-sunset-2` | `#ff9a56` | Naranja cálido (gradientes sunset) |
| `--rw-sunset-3` | `#ffd700` | Amarillo dorado (highlights) |
| `--rw-neon-blue` | `#00d4ff` | Azul cyan (acentos secundarios, enlaces) |
| `--rw-neon-purple` | `#b026ff` | Violeta neón (hover, destacados) |
| `--rw-chrome` | `#c0c0c0` | Texto metálico, bordes |
| `--rw-text` | `#ffffff` | Texto principal |
| `--rw-text-sec` | `rgba(255,255,255,.75)` | Texto secundario |
| `--rw-text-muted` | `rgba(255,255,255,.45)` | Hints, metadata |
| `--rw-glass` | `rgba(255,255,255,.08)` | Paneles, tarjetas |
| `--rw-glass-border` | `rgba(255,255,255,.15)` | Bordes sutiles |
| `--rw-grid-line` | `rgba(255,110,199,.2)` | Líneas del grid perspectivo |

## Gradientes clave

### Sunset Gradient (fondos principales)
```css
background: linear-gradient(180deg, #2b1055 0%, #1a0533 40%, #0d0221 100%);
```

### Horizon Glow
Gradiente radial en la parte inferior simulando el sol poniente:
```css
background: radial-gradient(ellipse at 50% 100%, rgba(255,110,199,.3) 0%, transparent 60%);
```

### Chrome Text
Efecto metálico para títulos grandes:
```css
background: linear-gradient(180deg, #fff 0%, #c0c0c0 40%, #fff 60%, #a0a0a0 100%);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
```

### Neon Border Glow
```css
box-shadow: 0 0 10px rgba(255,110,199,.4), 0 0 30px rgba(255,110,199,.15), inset 0 0 10px rgba(255,110,199,.1);
```

## Tipografía

- **Display:** `'Monoton', 'Bungee Shade', 'Orbitron', sans-serif` (títulos retro)
- **Body:** `'Rajdhani', 'Segoe UI', sans-serif`
- **Mono:** `'VT323', 'Press Start 2P', monospace` (datos, labels retro)

| Estilo | Tamaño | Peso | Letter-spacing | Uso |
|--------|--------|------|----------------|-----|
| Display | 48px | Regular | 6px | Títulos hero, logos |
| H1 | 32px | Bold | 4px | Títulos de página |
| H2 | 22px | SemiBold | 3px | Secciones |
| Body | 15px | Regular | 0.5px | Texto general |
| Label | 11px | Bold | 2px | Tags, badges, uppercase |
| Mono | 14px | Regular | 0 | Datos, código retro |

## Fondo

### Grid Perspectivo
Líneas horizontales convergentes + verticales paralelas creando efecto 3D outrun:
```css
/* Verticales */
background-image: linear-gradient(90deg, var(--rw-grid-line) 1px, transparent 1px);
background-size: 80px 100%;
/* Horizontales con perspectiva via transform */
transform: perspective(400px) rotateX(40deg);
```

### Sol Retro
Círculo con gradiente horizontal stripeado en la parte inferior:
```css
background: repeating-linear-gradient(
  0deg,
  #ff6ec7 0px, #ff6ec7 8px,
  #ff9a56 8px, #ff9a56 16px,
  #ffd700 16px, #ffd700 24px,
  transparent 24px, transparent 32px
);
border-radius: 50%;
mask-image: linear-gradient(to top, black 40%, transparent 100%);
```

### Stars / Partículas
Puntos blancos pequeños con twinkle lento en la mitad superior.

## Componentes

### Card
```
border-radius: 0 (esquinas rectas retro)
background: var(--rw-glass)
border: 1px solid var(--rw-glass-border)
backdrop-filter: blur(8px)
box-shadow: 0 4px 20px rgba(0,0,0,.4)
```
**Hover:** borde rosa neón, glow rosa sutil, translateY(-3px).
**Stripe decorativo:** línea horizontal de 3px con gradiente sunset en la parte superior.

### Botón Primario (Neon)
```
border-radius: 0
background: linear-gradient(180deg, #ff6ec7 0%, #b026ff 100%)
border: none
color: #fff
text-transform: uppercase
letter-spacing: 3px
box-shadow: 0 0 15px rgba(255,110,199,.5), 0 4px 15px rgba(0,0,0,.3)
```
**Hover:** glow intenso, scale(1.03), brightness(1.1).
**Active:** scale(0.97), glow reducido.

### Botón Secundario (Outline)
```
border: 2px solid var(--rw-neon-blue)
color: var(--rw-neon-blue)
background: transparent
```
**Hover:** fondo azul al 15%, glow azul.

### Input
```
background: rgba(0,0,0,.4)
border: 1px solid var(--rw-glass-border)
border-bottom: 2px solid var(--rw-sunset-1)
border-radius: 0
color: #fff
```
**Focus:** border-bottom azul neón, glow azul.

### Badge / Tag
Rectangular (sin border-radius), borde neon, texto uppercase 10px bold. Variante por color.

### Progress Bar
Track oscuro con fill gradiente sunset animado. Glow en el fill.

### Toggle Switch
Track oscuro, knob cuadrado. Estado on: track gradiente sunset, knob blanco con glow rosa.

## Animaciones

| Nombre | Duración | Uso |
|--------|----------|-----|
| `rwPulse` | 2.5s | Glow pulsante en elementos activos |
| `rwSlideUp` | 0.5s | Entrada desde abajo con fade |
| `rwGridScroll` | 4s | Grid perspectivo moviéndose hacia el espectador |
| `rwSunRotate` | 20s | Rotación lenta del sol retro |
| `rwFlicker` | 3s | Parpadeo sutil tipo neón viejo |
| `rwChromeShine` | 3s | Brillo deslizante sobre texto chrome |

## Responsive

| Breakpoint | Comportamiento |
|------------|---------------|
| > 1200px | Grid 4 columnas, sidebar visible |
| 900-1200px | Grid 3 columnas |
| 600-900px | Grid 2 columnas, sidebar colapsada |
| < 600px | Grid 1 columna, nav bottom bar, sol oculto |

## Accesibilidad

- Contraste mínimo WCAG AA sobre fondo oscuro
- Focus visible con outline rosa + glow
- `prefers-reduced-motion`: desactivar pulse/flicker/grid-scroll
- No depender solo del color para estados
- Texto chrome debe tener fallback legible sin background-clip