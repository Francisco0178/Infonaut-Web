# 🎨 Guía de Fuentes Personalizadas - Infonaut

## 📋 Resumen de Configuración

Tu proyecto Astro está configurado con **Tailwind CSS v4** y tiene 5 familias de fuentes personalizadas disponibles.

### Fuente Base del Sitio

- **Adinuee PRO** - Se aplica automáticamente a todo el sitio vía `font-sans`

---

## 🔤 Fuentes Disponibles

### 1. **Adinuee PRO** (Fuente Base)

- **Clase Tailwind:** `font-adinuee`
- **Uso:** Fuente principal del sitio, se aplica automáticamente
- **Ejemplo:**
  ```html
  <p class="font-adinuee">Texto con Adinuee PRO</p>
  ```

### 2. **Gotham**

- **Clase Tailwind:** `font-gotham`
- **Pesos disponibles:** Normal (400), Medium (500), Bold (700)
- **Uso:** Textos corporativos, navegación, botones
- **Ejemplos:**
  ```html
  <p class="font-gotham">Gotham Normal</p>
  <p class="font-gotham font-medium">Gotham Medium</p>
  <p class="font-gotham font-bold">Gotham Bold</p>
  ```

### 3. **Gotham Rounded**

- **Clase Tailwind:** `font-gotham-rounded`
- **Pesos disponibles:** Normal (400), Bold (700)
- **Uso:** Diseños más amigables y modernos
- **Ejemplo:**
  ```html
  <p class="font-gotham-rounded">Texto más amigable</p>
  ```

### 4. **Montserrat**

- **Clase Tailwind:** `font-montserrat`
- **Pesos disponibles:** Regular (400), Medium (500)
- **Uso:** Textos elegantes y versátiles
- **Ejemplo:**
  ```html
  <p class="font-montserrat">Texto elegante</p>
  ```

### 5. **Anton**

- **Clase Tailwind:** `font-anton`
- **Peso disponible:** Regular (400)
- **Uso:** Títulos grandes con impacto visual
- **Configuración automática:** Se aplica a `h1, h2, h3` por defecto
- **Ejemplo:**
  ```html
  <h1 class="font-anton text-6xl">TÍTULO IMPACTANTE</h1>
  ```

---

## 🎯 Jerarquía Tipográfica Configurada

Tu archivo `global.css` tiene esta jerarquía por defecto:

```css
/* Fuente base del sitio */
body {
  @apply font-sans; /* = Adinuee PRO */
}

/* Títulos principales */
h1,
h2,
h3 {
  @apply font-anton;
}

/* Títulos secundarios */
h4,
h5,
h6 {
  @apply font-gotham;
  font-weight: 700;
}
```

---

## 💡 Mejores Prácticas de Astro

### 1. **Importar estilos globales en el Layout**

✅ Ya lo tienes configurado en `MainLayout.astro`:

```astro
import "../styles/global.css";
```

### 2. **Usar clases de Tailwind en lugar de CSS inline**

❌ Evitar:

```astro
<p style="font-family: 'Gotham', sans-serif;">Texto</p>
```

✅ Mejor:

```astro
<p class="font-gotham">Texto</p>
```

### 3. **Scoped Styles para componentes específicos**

Si necesitas estilos únicos para un componente:

```astro
---
// Component logic
---

<div class="custom-component">
  <p>Contenido</p>
</div>

<style>
  /* Estos estilos solo afectan a este componente */
  .custom-component {
    /* estilos específicos */
  }
</style>
```

### 4. **Combinar clases de Tailwind**

```astro
<button class="font-gotham font-medium text-lg bg-blue-600 text-white px-6 py-3 rounded-lg hover:bg-blue-700 transition-colors">
  Botón Profesional
</button>
```

---

## 📁 Estructura de Archivos

```
Infonaut-Web/
├── public/
│   └── fonts/              # Fuentes personalizadas
│       ├── Anton-Regular.ttf
│       ├── Gotham-Book.otf
│       ├── Gotham-Medium.otf
│       ├── Gotham-Bold.otf
│       ├── GothamRnd-Book.otf
│       ├── GothamRnd-Bold.otf
│       ├── Montserrat-Regular.ttf
│       ├── Montserrat-Medium.ttf
│       └── adineue-PRO-Bold.ttf
├── src/
│   ├── styles/
│   │   └── global.css      # Configuración de Tailwind y fuentes
│   ├── layouts/
│   │   └── MainLayout.astro # Layout principal
│   ├── components/
│   │   └── NavBar.astro    # Componente de navegación
│   └── pages/
│       └── index.astro     # Página de inicio
└── astro.config.mjs        # Configuración de Astro + Tailwind
```

---

## 🚀 Próximos Pasos Recomendados

1. **Crear un sistema de colores personalizado** en `@theme`
2. **Definir componentes reutilizables** (botones, cards, etc.)
3. **Implementar responsive design** para móviles
4. **Agregar animaciones y transiciones** con Tailwind
5. **Optimizar imágenes** usando el componente `<Image>` de Astro

---

## 📚 Recursos Útiles

- [Documentación de Astro](https://docs.astro.build)
- [Tailwind CSS v4 Docs](https://tailwindcss.com/docs)
- [Astro + Tailwind Integration](https://docs.astro.build/en/guides/integrations-guide/tailwind/)

---

**Última actualización:** 2026-01-17
