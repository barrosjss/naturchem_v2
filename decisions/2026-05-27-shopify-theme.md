# ADR-003: Tema Shopify — Sense

**Fecha:** 2026-05-27
**Estado:** Propuesta
**Área:** Diseño / Ecommerce

---

## Contexto

Con la decisión de usar Shopify (ADR-002) tomada, se necesita elegir un tema base. El tema determina la estructura visual, las capacidades del editor, y el trabajo de customización necesario.

Dirección visual definida: **natural / orgánico** — tonos tierra, verdes, beige. Conecta con la naturaleza de los productos (ceras vegetales, glicerina, ingredientes artesanales).

## Opciones consideradas

### 1. Dawn (gratis)
- Pro: Tema oficial de Shopify, muy bien mantenido, altamente personalizable, velocidad excelente
- Pro: Documentación extensa, comunidad grande
- Contra: Estética muy neutra/minimalista — requiere más trabajo para lograr look natural/orgánico

### 2. Sense (gratis)
- Pro: Diseñado específicamente para productos de salud, belleza y bienestar
- Pro: Paleta de colores y tipografía ya orientada a lo natural/orgánico
- Pro: Secciones de "ingredientes" y "beneficios" nativas — perfectas para describir materias primas
- Pro: Gratis en Shopify Theme Store
- Contra: Menos flexible que Dawn en algunas customizaciones

### 3. Craft (gratis)
- Pro: Enfoque artesanal, perfecto para marcas handmade
- Pro: Fuerte énfasis visual en la historia del producto
- Contra: Más orientado a tiendas de 1 artesano, no catálogos de distribuidor

### 4. Tema de pago (ej. Prestige, Impulse)
- Pro: Más features, más polished
- Contra: USD 180-350 costo único — no justificado en etapa inicial

## Decisión

**Elegimos: Sense**

Sense fue diseñado para el nicho exacto de Naturchem: productos naturales, wellness, ingredientes. Las secciones nativas (descripción de ingredientes, galería de proceso, call-to-action de WhatsApp/contacto) reducen el trabajo de customización. La dirección visual del tema se alinea directamente con la paleta elegida en `web/design-spec.md`.

## Consecuencias

**Positivas:**
- Cero costo de tema
- Menos customización CSS necesaria (paleta ya compatible)
- Secciones de producto adecuadas para materias primas
- Mobile-first por diseño

**Negativas / trade-offs:**
- Si se necesitan features avanzadas (filtros complejos, bundles) → requiere apps de Shopify
- Puede verse similar a otras tiendas que usan Sense — diferenciación depende de fotos y copy

## Próximos pasos

- [ ] Crear tienda Shopify
- [ ] Instalar tema Sense desde Shopify Theme Store
- [ ] Correr `shopify theme pull` para backup local (ver `web/shopify-workflow.md`)
- [ ] Aplicar paleta de colores Naturchem (ver `web/design-spec.md`)
- [ ] Configurar tipografía: Playfair Display + Inter

---

*Decisión propuesta por: InnoGrowth Consulting (Jesús Barros)*
*Aprobar con: equipo Naturchem*
