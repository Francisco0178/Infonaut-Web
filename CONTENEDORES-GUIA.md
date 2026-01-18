# 📐 Sistema de Contenedores y Márgenes - Infonaut

## 📋 Resumen

El sitio Infonaut utiliza un sistema de contenedores consistente para mantener márgenes y anchos uniformes en todas las páginas.

---

## 🎯 Clases de Contenedores Disponibles

### 1. **`.site-container`** (Contenedor Principal)

- **Ancho máximo:** 1280px
- **Padding lateral:**
  - Móvil: 24px (1.5rem)
  - Tablet (≥768px): 32px (2rem)
  - Desktop (≥1024px): 48px (3rem)
- **Uso:** Contenedor principal para la mayoría del contenido del sitio

```html
<section class="site-container">
  <!-- Contenido con márgenes estándar -->
</section>
```

### 2. **`.content-container`** (Contenedor de Lectura)

- **Ancho máximo:** 960px
- **Padding lateral:** Igual que `.site-container`
- **Uso:** Contenido de lectura, artículos, texto largo

```html
<article class="content-container">
  <!-- Contenido más estrecho para mejor lectura -->
</article>
```

### 3. **`.wide-container`** (Contenedor Ancho)

- **Ancho máximo:** 1536px
- **Padding lateral:** Igual que `.site-container`
- **Uso:** Galerías, grids amplios, contenido que necesita más espacio

```html
<section class="wide-container">
  <!-- Contenido más ancho -->
</section>
```

---

## 🏗️ Estructura del MainLayout

El `MainLayout` aplica automáticamente `.site-container` al contenido:

```astro
<MainLayout title="Mi Página">
  <!-- Este contenido automáticamente tiene márgenes -->
  <section class="py-12">
    <h1>Título</h1>
    <p>Contenido...</p>
  </section>
</MainLayout>
```

### Opción: Ancho Completo

Si necesitas una página sin márgenes automáticos:

```astro
<MainLayout title="Mi Página" fullWidth={true}>
  <!-- Este contenido NO tiene márgenes automáticos -->
  <!-- Debes agregar tus propios contenedores -->
  <section class="site-container">
    <h1>Título</h1>
  </section>
</MainLayout>
```

---

## 📱 Comportamiento Responsive

### Móvil (< 768px)

```css
padding-left: 1.5rem; /* 24px */
padding-right: 1.5rem; /* 24px */
```

### Tablet (≥ 768px)

```css
padding-left: 2rem; /* 32px */
padding-right: 2rem; /* 32px */
```

### Desktop (≥ 1024px)

```css
padding-left: 3rem; /* 48px */
padding-right: 3rem; /* 48px */
```

---

## 💡 Ejemplos de Uso

### Ejemplo 1: Sección con Contenedor Principal

```astro
<MainLayout title="Servicios">
  <section class="py-20">
    <!-- El contenedor ya está aplicado por MainLayout -->
    <h2 class="text-4xl mb-8">Nuestros Servicios</h2>
    <div class="grid grid-cols-3 gap-6">
      <!-- Contenido -->
    </div>
  </section>
</MainLayout>
```

### Ejemplo 2: Sección de Ancho Completo con Contenedor Interno

```astro
<MainLayout title="Hero" fullWidth={true}>
  <!-- Fondo de ancho completo -->
  <section class="py-20 bg-blue-600">
    <!-- Contenido con márgenes -->
    <div class="site-container">
      <h1 class="text-6xl text-white">Título Hero</h1>
    </div>
  </section>
</MainLayout>
```

### Ejemplo 3: Múltiples Contenedores

```astro
<MainLayout title="Página" fullWidth={true}>
  <!-- Hero sin márgenes -->
  <section class="py-20 bg-linear-to-r from-blue-500 to-purple-500">
    <div class="site-container">
      <h1>Hero</h1>
    </div>
  </section>

  <!-- Contenido con márgenes estándar -->
  <section class="py-12 site-container">
    <h2>Contenido Principal</h2>
  </section>

  <!-- Contenido de lectura más estrecho -->
  <article class="py-12 content-container">
    <p>Artículo largo...</p>
  </article>
</MainLayout>
```

---

## ✅ Mejores Prácticas

### ✅ **Hacer:**

1. Usar `.site-container` para la mayoría del contenido
2. Usar `.content-container` para artículos y texto largo
3. Usar `fullWidth={true}` cuando necesites fondos de ancho completo
4. Mantener consistencia en los márgenes entre páginas

### ❌ **Evitar:**

1. No usar `container mx-auto px-4` (usar `.site-container` en su lugar)
2. No mezclar diferentes sistemas de contenedores
3. No agregar padding adicional a los contenedores (ya lo tienen)
4. No usar anchos máximos personalizados sin razón

---

## 🎨 Combinación con Colores de Marca

```astro
<!-- Sección con fondo de color y contenedor -->
<section class="py-20" style="background-color: var(--color-primary);">
  <div class="site-container text-white">
    <h2 class="text-4xl mb-4">Título</h2>
    <p>Contenido...</p>
  </div>
</section>
```

---

## 📊 Tabla de Referencia Rápida

| Clase                | Ancho Máximo | Uso Principal           |
| -------------------- | ------------ | ----------------------- |
| `.site-container`    | 1280px       | Contenido general       |
| `.content-container` | 960px        | Artículos, texto largo  |
| `.wide-container`    | 1536px       | Galerías, grids amplios |

---

## 🔗 Archivos Relacionados

- **Definición:** `src/styles/global.css` (líneas 20-90)
- **Implementación:** `src/layouts/MainLayout.astro`
- **Ejemplos:** `src/pages/index.astro`, `src/pages/colors-demo.astro`

---

**Última actualización:** 2026-01-18
