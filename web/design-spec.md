# Naturchem — Especificación de Diseño Web (Shopify)

**Fecha:** 2026-05-27
**Estado:** En definición
**Tema elegido:** Ver `decisions/2026-05-27-shopify-theme.md`

---

## Dirección visual

**Concepto:** Natural / orgánico — evoca materias primas de origen natural, artesanía, proceso.

**Palabras clave:** limpio, accesible, confiable, artesanal, educativo.

**Referente:** Tiendas de ingredientes naturales latinoamericanas. Sensación de mercado especializado, no supermercado.

---

## Paleta de colores

| Nombre | Hex | Uso |
|---|---|---|
| **Verde bosque** | `#2D5A27` | Color primario — CTAs, headings, acento fuerte |
| **Verde salvia** | `#6B8F5E` | Color secundario — iconos, elementos de apoyo |
| **Crema** | `#F5F0E8` | Background principal — evoca papel natural |
| **Tierra** | `#8B6F47` | Terciario — separadores, texto secundario |
| **Dorado** | `#C4A45E` | Acento — badges, precios, highlights |
| **Blanco** | `#FFFFFF` | Cards de productos, modal, limpieza |
| **Texto oscuro** | `#1C2B1A` | Texto principal — casi negro con tono verde |

```css
/* Variables CSS para Shopify */
--color-primary: #2D5A27;
--color-primary-light: #6B8F5E;
--color-background: #F5F0E8;
--color-accent-earth: #8B6F47;
--color-accent-gold: #C4A45E;
--color-white: #FFFFFF;
--color-text: #1C2B1A;
```

---

## Tipografía

| Rol | Fuente | Peso | Tamaño ref |
|---|---|---|---|
| **Headings** | Playfair Display | 700 | 32–48px |
| **Subheadings** | Playfair Display | 600 | 20–28px |
| **Body** | Inter | 400 | 16px |
| **Labels / badges** | Inter | 600 | 12–14px |
| **Precios** | Inter | 700 | 18–24px |

> Playfair Display = serif elegante, evoca lo artesanal. Inter = legibilidad perfecta en mobile.

---

## Estructura de páginas

### Homepage

```
[ Hero ]
  - Headline: "Tu punto de partida para crear"
  - Subheadline: "Materias primas naturales al mejor precio en Colombia"
  - CTA: "Explorar catálogo" + "Ver más populares"
  - Imagen: materiales naturales (cera, glicerina, jabones crudos)

[ Propuesta de valor ]
  - 3 columnas: Precio competitivo | Envío nacional | Educación incluida

[ Colecciones destacadas ]
  - Grid 3x2: Ceras / Glicerina / Jabones / Cremas / Aseo / Vitality

[ Productos más vendidos ]
  - Carrusel horizontal, 4-6 productos

[ Banner educativo ]
  - "¿No sabes por dónde empezar?"
  - CTA a guías / tutoriales

[ Testimonios / reseñas ]
  - Reviews de clientes

[ Footer ]
  - WhatsApp | Instagram | Email | Política de envíos
```

### Página de producto

```
[ Galería ] - mínimo 4 imágenes (ver products.md)
[ Nombre + SKU ]
[ Precio ] - en COP con IVA incluido
[ Variantes ] - presentación (500g, 1kg, 5kg, etc.)
[ Botón "Agregar al carrito" ] - verde primario
[ Botón "Consultar por WhatsApp" ] - verde outline
[ Descripción ] - qué es + para qué sirve
[ Cómo usarlo ] - sección colapsable
[ Productos relacionados ]
```

### Colección

```
[ Header colección ] - nombre + descripción
[ Filtros sidebar ] - por presentación, precio
[ Grid de productos ] - 3 columnas desktop, 2 mobile
[ Paginación ]
```

---

## Componentes clave

### Badge de producto
- "Más vendido" → fondo dorado `#C4A45E`
- "Nuevo" → fondo verde `#2D5A27`
- "Agotado" → fondo tierra `#8B6F47`

### Botón WhatsApp
Presente en cada producto. Texto: "Consultar disponibilidad"
Link: `https://wa.me/573004986307?text=Hola, me interesa [PRODUCTO]`

### Carrito
- Mostrar envío estimado desde `$X` para Colombia
- Mention de pasarela: "Paga con Wompi o contraentrega"

---

## Mobile-first notes

- 60%+ de tráfico esperado es mobile (Colombia, redes sociales → Instagram → tienda)
- Hero imagen: versión vertical / square para mobile
- Botón WhatsApp: sticky en mobile, visible siempre
- Grid productos: 2 columnas en mobile

---

## Contenido pendiente para lanzar

- [ ] Catálogo completo de productos con precios — ver `business/products.md`
- [ ] Fotos profesionales (50 productos — propuesta $1,600,000 COP)
- [ ] Copy de cada página de colección
- [ ] Política de envíos y devoluciones
- [ ] Dominio elegido — ver `stack/shopify.md`
- [ ] Pasarela de pago configurada (Wompi recomendado)
