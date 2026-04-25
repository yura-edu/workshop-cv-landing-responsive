# Landing Page Responsive HTML5/CSS

> **Tipo:** CODE_QUALITY · **Duración estimada:** 180 min · **Nivel:** Básico-Intermedio

## Objetivo

Construir la landing page de **Yura** con HTML5 semántico, CSS puro (sin frameworks), 3 breakpoints responsive, y obtener Lighthouse ≥ 90 en Performance y Accessibility.

## Instrucciones

### 1. Prepara tu entorno

```bash
git clone <url-de-tu-repositorio>
cd workshop-cv-landing-responsive/starter-code
```

Abre `wireframe.svg` en tu navegador para ver el diseño de referencia.

### 2. Implementa el HTML

Edita `index.html`. El archivo tiene 6 secciones definidas con comentarios que explican qué implementar en cada una:
- `<header>` + `<nav>` con hamburger CSS-only para mobile
- `<section id="inicio">` — Hero
- `<section id="caracteristicas">` — 3 feature cards
- `<section id="precios">` — 2 pricing cards
- `<section id="testimonios">` — 2-3 testimonios
- `<footer>` — links y copyright

**Reglas de accesibilidad obligatorias:**
- Todas las imágenes tienen `alt` descriptivo
- La jerarquía de headings es h1 → h2 → h3
- Los links tienen texto descriptivo (no "click aquí")
- El contraste de texto cumple WCAG AA (≥ 4.5:1 para texto normal)

### 3. Implementa el CSS

Edita `css/styles.css` con los estilos base (ya tiene el reset y las custom properties).

Edita `css/responsive.css` con los 3 breakpoints (ya tienen el esqueleto):
```
mobile:  @media (max-width: 767px)
tablet:  @media (min-width: 768px) and (max-width: 1199px)
desktop: @media (min-width: 1200px)
```

**Sin JavaScript.** El menú hamburger se implementa con `<input type="checkbox">` + `<label>` + CSS.

### 4. Verifica con Lighthouse

```bash
# Sirve la landing localmente
npx serve . -p 3000
# Luego abre Chrome → DevTools → Lighthouse → Analizar
```

Objetivos antes de entregar:
- Performance ≥ 90
- Accessibility ≥ 90
- Best Practices ≥ 90

### 5. Despliega y abre el Pull Request

#### Opción A — GitHub Pages
```bash
git push origin main   # GitHub Pages publica automáticamente si está configurado
```
URL: `https://<usuario>.github.io/<repo>/`

#### Opción B — Vercel
```bash
npx vercel --prod
```
El archivo `vercel.json` ya está configurado.

El PR debe incluir la **URL desplegada** en la descripción.

## Criterios de evaluación

| Métrica | Peso | Umbral |
|---|---|---|
| Lighthouse Performance | 25% | ≥ 90 |
| Lighthouse Accessibility | 25% | ≥ 90 |
| Media queries responsive | 25% | ≥ 3 breakpoints en CSS |
| Errores de HTML | 25% | 0 errores (html-validate) |

## Recursos

- [MDN — HTML5 Semántico](https://developer.mozilla.org/es/docs/Glossary/Semantics#semantics_in_html)
- [MDN — CSS Media Queries](https://developer.mozilla.org/es/docs/Web/CSS/CSS_media_queries/Using_media_queries)
- [Trucos CSS — Menú hamburger sin JS](https://css-tricks.com/three-css-alternatives-to-javascript-navigation/)
- [WebAIM — Contrast Checker](https://webaim.org/resources/contrastchecker/)
- [Lighthouse — Getting Started](https://developer.chrome.com/docs/lighthouse/overview)
