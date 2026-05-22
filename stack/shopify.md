# Shopify en Naturchem

Ver decisión en `decisions/2026-05-22-shopify-ecommerce.md` para el contexto de por qué se eligió Shopify.

## Estado actual

**Estado:** En construcción (Mayo 2026)

## Plan recomendado

| Plan | Precio | Cuándo usar |
|---|---|---|
| Basic | USD 29/mes | Arrancar — hasta ~50 pedidos/mes |
| Shopify | USD 79/mes | Cuando supere 50 pedidos/mes o necesite reportes avanzados |
| Advanced | USD 299/mes | Escala mayor, múltiples ubicaciones |

**Recomendación actual:** empezar en **Basic**, migrar a Shopify plan cuando el volumen lo justifique.

## Dominio

- **Recomendación:** `naturchem.co` (dominio colombiano, .co disponible)
- Alternativa: `naturchem.com.co` o `naturchem.com`
- [COMPLETAR — dominio elegido]

## Pasarelas de pago (Colombia)

| Pasarela | Comisión aprox | Notas |
|---|---|---|
| **Wompi** (Bancolombia) | ~2.95% + IVA | Recomendada — mejor experiencia UX, integración nativa Shopify |
| Epayco | ~3.49% | Alternativa popular en Colombia |
| PayU | ~3.49% | Mayor reconocimiento, más complejo |
| Contraentrega | 0% pasarela | Para clientes que prefieren pagar al recibir |

**Recomendación:** Wompi como principal + opción de contraentrega.

## Integraciones prioritarias

### Fase 1 (lanzamiento)
- [ ] Google Merchant Center → Google Shopping
- [ ] Meta Business → Instagram Shopping + Facebook Shop
- [ ] Pasarela de pago colombiana (Wompi)
- [ ] WhatsApp Business (botón de contacto en producto)

### Fase 2 (crecimiento)
- [ ] Mercado Libre (app oficial en Shopify App Store)
- [ ] Google Analytics 4
- [ ] Email marketing (Klaviyo o Mailchimp)
- [ ] Shopify Inbox (chat en vivo)

## Estructura del catálogo en Shopify

### Colecciones sugeridas

```
Ceras
  ├── Cera de Soja
  ├── Cera de Molde
  └── Parafina
Glicerina
Ingredientes para Jabones
Bases para Cremas
Productos de Aseo
Línea Vitality
Kits / Combos
```

### Convenciones de producto

- Nombre: `[Producto] [Presentación]` ej: "Cera de Soja 500g"
- SKU: [COMPLETAR — definir formato]
- Imágenes: mínimo 4 por producto (frente, lateral, detalle, contexto uso)
- Descripción: qué es + para qué sirve + cómo usarlo
- Tags: materia-prima, velas, jabones, cremas, aseo (según categoría)

## Configuración de envíos

[COMPLETAR — zonas de envío, operadores logísticos, tiempos, costos]

Opciones logísticas a evaluar:
- Coordinadora
- Interrapidísimo
- Servientrega
- TCC
- Envíos locales Barranquilla (moto)

## Métricas clave a monitorear

| Métrica | Objetivo inicial |
|---|---|
| Tasa de conversión | > 2% |
| Valor promedio del pedido | [COMPLETAR] |
| Tasa de abandono de carrito | < 70% |
| Pedidos/mes | [COMPLETAR] |
