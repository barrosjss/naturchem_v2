# ADR-004 — Carga del catálogo vía Shopify Admin API

**Fecha:** 2026-06-18
**Estado:** Aceptada
**Área:** Tecnología / Operaciones

## Contexto

El cliente entregó el catálogo completo en formato CSV exportado de su sistema contable (`PRODUCTO(Datos).csv`). El archivo contenía ~580 registros con código, categoría y nombre. Sin precios ni imágenes.

Se necesitaba cargar masivamente los productos a Shopify sin hacerlo uno a uno por el admin.

## Decisión

Usar la Shopify Admin REST API para carga automatizada, con una app de Partners configurada con OAuth para obtener el access token.

**App creada:** "Agente Claude" en Shopify Partners dashboard
**Scopes:** `read_products`, `write_products`, `read_inventory`, `write_inventory`
**Shop:** `naturchem-colombia.myshopify.com`

## Proceso ejecutado

1. Exportar CSV del sistema contable → filtrar ANULADOS y registros genéricos
2. Configurar app Partners con OAuth redirect a `http://localhost:3000/callback`
3. Servidor local captura el `code` → intercambia por `access_token`
4. Carga masiva: 562 productos creados vía API (0 errores)
5. Activar todos: status `draft` → `active`
6. Publicar todos: `published_at: null` → timestamp actual (era la causa de que no aparecían en la tienda)

## Resultado

- **564 productos** activos y visibles en `naturchemcolombia.com`
- Todos con precio `$0` — pendiente lista de precios del cliente
- Todos sin imagen — pendiente sesión fotográfica

## Categorías cargadas

| Tipo | Cantidad |
|---|---|
| Envases y Moldes | 272 |
| Fragancias | 92 |
| Colorantes | 48 |
| Aceites y Extractos | 40 |
| Materias Primas | 36 |
| Ingredientes | 29 |
| Bases y Ceras | 24 |
| Insumos | 21 |

## Consecuencias

- El access token OAuth es temporal — si expira o se reinstala la app se necesita re-autenticar
- Para gestión continua de catálogo (precios, imágenes, colecciones) se puede usar la misma API
- Pendiente: crear colecciones en Shopify y asignar productos para mejorar navegación en tienda
