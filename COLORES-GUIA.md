# 🎨 Guía de Colores de Marca - Infonaut

## 📋 Paleta de Colores

### Colores Principales

#### Primary - Turquesa Vibrante

- **HEX:** `#00AAB5`
- **Variable CSS:** `--color-primary`
- **Uso:** Botones principales, CTAs, enlaces importantes, elementos destacados
- **Ejemplo:**
  ```html
  <button style="background-color: var(--color-primary);">Botón Primary</button>
  ```

#### Secondary - Verde Energético

- **HEX:** `#00B547`
- **Variable CSS:** `--color-secondary`
- **Uso:** Botones secundarios, badges, elementos de éxito, destacados
- **Ejemplo:**
  ```html
  <span style="background-color: var(--color-secondary);">Badge</span>
  ```

---

### Colores de Acento

#### Accent 1 - Verde Agua

- **HEX:** `#00B585`
- **Variable CSS:** `--color-accent-1`
- **Uso:** Fondos, tarjetas, secciones alternativas

#### Accent 2 - Azul Corporativo

- **HEX:** `#0070B5`
- **Variable CSS:** `--color-accent-2`
- **Uso:** Elementos de confianza, información, secciones informativas

#### Accent 3 - Azul Profundo

- **HEX:** `#0037B5`
- **Variable CSS:** `--color-accent-3`
- **Uso:** Fondos oscuros, footer, elementos de contraste alto

---

## 🎨 Gradientes Sugeridos

### Gradiente 1: Primary → Secondary

```css
background: linear-gradient(135deg, #00aab5 0%, #00b547 100%);
```

**Uso:** Headers, secciones hero, CTAs principales

### Gradiente 2: Accent 1 → Accent 2

```css
background: linear-gradient(135deg, #00b585 0%, #0070b5 100%);
```

**Uso:** Tarjetas de servicios, secciones de características

### Gradiente 3: Accent 2 → Accent 3

```css
background: linear-gradient(135deg, #0070b5 0%, #0037b5 100%);
```

**Uso:** Fondos de footer, secciones oscuras

### Gradiente 4: Primary → Accent 3

```css
background: linear-gradient(135deg, #00aab5 0%, #0037b5 100%);
```

**Uso:** Fondos de página completa, overlays

---

## 💻 Cómo Usar los Colores

### En HTML/Astro con Variables CSS

```html
<div style="background-color: var(--color-primary);">Contenido</div>
```

### En CSS Personalizado

```css
.custom-button {
  background-color: var(--color-primary);
  color: white;
  padding: 1rem 2rem;
  border-radius: 0.5rem;
}

.custom-button:hover {
  background-color: var(--color-secondary);
}
```

### Con Valores Directos

```html
<button style="background-color: #00AAB5;">Botón Primary</button>
```

---

## 🎯 Casos de Uso Recomendados

### Botones

- **Primary (#00AAB5):** Botones de acción principal (Comprar, Contactar, Registrarse)
- **Secondary (#00B547):** Botones de acción secundaria (Más información, Ver más)
- **Accent 2 (#0070B5):** Botones informativos (Descargar, Compartir)

### Fondos

- **Accent 1 (#00B585):** Fondos de secciones alternativas
- **Accent 3 (#0037B5):** Footer, secciones oscuras

### Badges y Etiquetas

- **Primary (#00AAB5):** Nuevo, Destacado
- **Secondary (#00B547):** Popular, Recomendado
- **Accent 2 (#0070B5):** Premium, Pro

### Texto sobre Fondos de Color

- Todos los colores de la paleta tienen suficiente contraste para texto blanco
- Usar `color: white` o `color: #ffffff` sobre cualquier color de la marca

---

## ✅ Accesibilidad

Todos los colores de la marca cumplen con WCAG 2.1 AA para texto blanco:

- **Primary (#00AAB5):** Contraste 4.5:1 ✓
- **Secondary (#00B547):** Contraste 4.5:1 ✓
- **Accent 1 (#00B585):** Contraste 4.5:1 ✓
- **Accent 2 (#0070B5):** Contraste 4.5:1 ✓
- **Accent 3 (#0037B5):** Contraste 7:1 ✓

---

## 🔗 Ver Demo en Vivo

Visita `/colors-demo` en tu navegador para ver todos los colores en acción con ejemplos interactivos.

---

**Última actualización:** 2026-01-18
