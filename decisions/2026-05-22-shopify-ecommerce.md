# ADR-002: Shopify como Plataforma de Ecommerce Principal

**Fecha:** 2026-05-22
**Estado:** Aceptada
**Área:** Tecnología / Producto

---

## Contexto

Naturchem necesita una plataforma de ecommerce propio para vender directamente al consumidor. La decisión de tener marketplace propio estaba incluida en ADR-001. Se evaluaron las principales opciones disponibles en Colombia.

## Opciones consideradas

1. **Shopify**
   - Pro: Fácil de usar, excelente ecosistema de apps, escalable, integraciones con Mercado Libre / Facebook / Google Shopping
   - Pro: Pasarelas de pago colombianas disponibles (Wompi, Epayco, PayU)
   - Pro: Nativo en mobile, SEO sólido, soporte confiable
   - Contra: Costo mensual (USD 29-79/mes según plan)

2. **WooCommerce (WordPress)**
   - Pro: Más barato a corto plazo, flexible
   - Contra: Requiere hosting propio, mantenimiento técnico constante, más frágil

3. **Tiendanube / Wix**
   - Pro: Fácil de arrancar
   - Contra: Ecosistema más limitado, menos escalable para crecer

4. **Mercado Libre + marketplace de terceros únicamente**
   - Pro: Sin costo de plataforma
   - Contra: Sin base de datos de clientes propia, sin control de experiencia, comisiones altas

## Decisión

**Elegimos: Shopify**

Shopify es el estándar de la industria para ecommerce D2C (direct-to-consumer). Su ecosistema de integraciones permite conectar con todos los canales (Google, Meta, Mercado Libre) desde un solo punto de verdad de inventario y pedidos. La inversión mensual se justifica por la reducción de complejidad técnica.

## Consecuencias

**Positivas:**
- Un solo dashboard para inventario, pedidos y clientes
- Integraciones nativas con Instagram Shopping, Google Shopping, Facebook Catalog
- Escalable: funciona igual para 10 pedidos/mes que para 10,000
- Base de datos de clientes 100% propia (email, comportamiento de compra)

**Negativas / trade-offs:**
- Costo mensual en dólares (se encarece si el peso colombiano se devalúa)
- Dependencia de plataforma externa (Shopify puede cambiar precios/políticas)

## Stack de Shopify para Naturchem

Ver detalles en `stack/shopify.md`

## Próximos pasos

- [ ] Crear cuenta Shopify (plan Basic o Shopify según volumen esperado)
- [ ] Configurar dominio (naturchem.co o naturchem.com)
- [ ] Cargar catálogo completo de productos
- [ ] Configurar pasarela de pago colombiana (Wompi recomendado)
- [ ] Conectar con Google Merchant Center (para Shopping Ads)
- [ ] Conectar con Meta Business (para Instagram Shopping)
- [ ] Integrar con Mercado Libre (app Shopify ML)

---

*Decisión tomada por: Naturchem + InnoGrowth Consulting (Jesús Barros)*
*Revisión: a los 6 meses de operación*
