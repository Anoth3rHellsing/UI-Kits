# AeroGlass UI Kit v1.0.0 — Release Notes

**Sistema de diseño Frutiger Aero para WPF y Web**  
Estética glossy con gradientes hard-stop, vidrio translúcido y sombras coloreadas.

---

## ✨ Novedades

### 🎨 Identidad Visual
- Paleta de 13 tokens de color con jerarquía semántica (Deep, Ink, Muted, Line, Glass)
- Gradiente SkyBrush diagonal obligatorio como fondo raíz
- Overlay TopGloss de 170px simulando iluminación cenital sobre vidrio
- Botones Glossy con firma visual hard-stop en offset 0.49→0.51
- Shine interior de 17px en botones para efecto "wet look"
- Sombras coloreadas `#0A3A56` integradas en la temperatura de color de la escena
- Burbujas decorativas asimétricas con RadialGradientBrush off-center

### 🧩 Componentes WPF
- **Gloss Button**: estándar (40px) y grande (62px) con glow ring en hover
- **Ghost Button**: transparente con borde alpha-white
- **Chrome Button**: controles de ventana (minimizar, maximizar, cerrar)
- **Nav RadioButton**: navegación lateral con barra indicadora izquierda
- **Toggle Switch**: track con gradiente verde al activar, knob con sombra suave
- **CheckBox**: estado checked con GlossBlue fill y checkmark blanco
- **Card**: contenedor con CardBrush, padding 18px y SoftShadow
- **ProgressBar**: track translúcido con indicador GlossBlue y highlight superior
- **TextBox**: fondo `#B3FFFFFF` con borde alpha y foco azul
- **ListView**: filas con hover/selected states diferenciados
- **TabControl**: pestañas con estados inactive/hover/selected
- **ScrollBar**: thumb redondeado semi-transparente

### 🌐 Port Web CSS
- Implementación completa en index.html con `backdrop-filter: blur()`
- Carousel interactivo con dots, navegación y auto-advance (5s)
- Search filter en tiempo real sobre tarjetas de aplicaciones
- Tema musical incluido con autoplay y fallback por interacción
- Animaciones fadeUp, float, shimmer y pulse

### 🔍 QA & Verificación
- SKILL.md con protocolo de aplicación y verificación automatizada
- QA-CHECKLIST.md con 7 dimensiones de auditoría:
  - Color Token Compliance
  - Gradient Fidelity
  - Spacing & Layout
  - Interactive States
  - Typography
  - Accessibility
  - Integration & Resource Merging
- Scripts PowerShell para detección automática de violaciones comunes
- Clasificación de severidad (Critical → Info)

### ♿ Accesibilidad
- Contraste WCAG AA verificado: Deep-on-glass ≥ 4.5:1, Muted-on-glass ≥ 3:1
- Focus indicators visibles en todos los elementos interactivos
- Estados disabled distinguibles sin depender solo del color
- Touch targets ≥ 32px en todas las variantes

### 📦 Contenido del Paquete
- `index.html` — Demo web completa con carousel, search y audio
- `DESIGN-SPEC.md` — Especificación canónica de tokens y componentes
- `SKILL.md` — Guía de aplicación y verificación QA
- `QA-CHECKLIST.md` — Protocolo de auditoría con scripts
- `Another Shop Theme (HQ).mp3` — Tema musical ambiental
- `CHANGELOG.md` — Historial de versiones

## 🖥️ Compatibilidad
- **WPF**: .NET Framework 4.8+ / .NET 6+, Windows 10 1809+
- **Web**: Chrome, Firefox, Safari, Edge (con soporte backdrop-filter)
- **Portabilidad**: notas incluidas para WinUI/MAUI y Flutter

## 🚀 Uso Rápido (WPF)
```xml
<ResourceDictionary.MergedDictionaries>
    <ResourceDictionary Source="Resources/AeroGlassResources.xaml"/>
</ResourceDictionary.MergedDictionaries>
```

## 🚀 Uso Rápido (Web)
```html
<link rel="stylesheet" href="aeroglass.css">
<div class="ag-reset">
  <div class="ag-bg"></div>
  <div class="ag-container">
    <!-- tu contenido aquí -->
  </div>
</div>
```

---

*AeroGlass UI Kit v1.0.0 · Lanzamiento inicial · Septiembre 2026*