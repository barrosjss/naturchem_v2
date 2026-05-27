# Shopify — Workflow Local y Backup via CLI

Guía para editar el tema Shopify de Naturchem localmente y mantener backup en git.

---

## Setup inicial (una sola vez)

### 1. Autenticar Shopify CLI

```bash
shopify auth login --store naturchem.myshopify.com
```

> Reemplazar con el store handle real una vez creada la tienda.

### 2. Clonar tema activo a este repo

```bash
cd /Users/jesusbarros/Documents/GitHub/naturchem_v2
shopify theme pull --store naturchem.myshopify.com --path ./web/theme
```

Esto crea `web/theme/` con todos los archivos `.liquid`, `assets/`, `config/`, etc.

### 3. Agregar `web/theme/` a git

```bash
git add web/theme/
git commit -m "feat: backup inicial tema Shopify"
```

---

## Workflow de desarrollo diario

### Modo desarrollo en vivo

```bash
cd web/theme
shopify theme dev --store naturchem.myshopify.com
```

Abre preview en browser con hot-reload. Cambios en `.liquid` se reflejan al guardar.

### Subir cambios al store

```bash
shopify theme push --store naturchem.myshopify.com
```

### Guardar backup en git después de cada sesión

```bash
git add web/theme/
git commit -m "feat: [descripción del cambio en el tema]"
```

---

## Estructura del tema (post-pull)

```
web/theme/
├── assets/          ← CSS, JS, imágenes del tema
├── config/          ← settings_data.json (customizaciones del editor)
├── layout/          ← theme.liquid (estructura HTML base)
├── locales/         ← traducciones
├── sections/        ← bloques de homepage y páginas
├── snippets/        ← componentes reutilizables
└── templates/       ← product.liquid, collection.liquid, etc.
```

**Archivos más importantes a editar:**

| Archivo | Qué controla |
|---|---|
| `config/settings_data.json` | Todos los settings del tema editor |
| `sections/header.liquid` | Navbar, logo, menú |
| `sections/footer.liquid` | Footer links, WhatsApp |
| `templates/product.liquid` | Layout de página de producto |
| `templates/collection.liquid` | Layout de colección |
| `sections/featured-collection.liquid` | Carrusel homepage |
| `assets/base.css` | Estilos globales del tema |

---

## Customizaciones CSS para paleta Naturchem

Una vez descargado el tema, agregar en `assets/naturchem-custom.css`:

```css
:root {
  --color-primary: #2D5A27;
  --color-primary-light: #6B8F5E;
  --color-background: #F5F0E8;
  --color-accent-earth: #8B6F47;
  --color-accent-gold: #C4A45E;
  --color-text: #1C2B1A;
}

/* Override tema base con colores Naturchem */
.btn-primary, .button--primary {
  background-color: var(--color-primary);
  color: white;
}

.btn-primary:hover {
  background-color: var(--color-primary-light);
}

body {
  background-color: var(--color-background);
  color: var(--color-text);
}
```

Incluir en `layout/theme.liquid` antes del `</head>`:
```liquid
{{ 'naturchem-custom.css' | asset_url | stylesheet_tag }}
```

---

## Pasos para crear la tienda Shopify

1. Ir a shopify.com/free-trial o shopify.com/co
2. Crear cuenta con email `jesusr.barrosb@gmail.com`
3. Store name: `naturchem` → genera `naturchem.myshopify.com`
4. Plan: **Basic** ($29 USD/mes)
5. Una vez creada → correr `shopify auth login` del paso 1
6. Instalar tema **Sense** (ver decisión `decisions/2026-05-27-shopify-theme.md`)
7. Pull tema → backup en git

---

## Notas

- `config/settings_data.json` contiene todas las customizaciones del editor visual — **siempre incluirlo en git**
- Nunca editar directamente en admin si hay cambios locales no pusheados — se pierden
- Antes de publicar cambios grandes: duplicar tema en Shopify admin como backup adicional
