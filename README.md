# Naturchem — Knowledge Base

Base de conocimiento estructurada del negocio Naturchem. Diseñada para ser consumida por modelos de IA (especialmente Claude) y por el equipo de InnoGrowth.

## Inicio rápido para IA

Leer primero: `CLAUDE.md` — contiene el contexto completo del negocio y el mapa de este repositorio.

## Estructura

```
naturchem_v2/
├── CLAUDE.md                              # Contexto principal para IA
├── business/
│   ├── overview.md                        # Perfil de la empresa
│   ├── products.md                        # Catálogo de productos
│   ├── customers.md                       # Segmentos de clientes
│   └── market-context.md                  # Mercado Colombia / Barranquilla
├── decisions/
│   ├── _index.md                          # Índice de todas las decisiones
│   ├── _template.md                       # Plantilla para nuevas decisiones
│   ├── 2026-01-21-digital-expansion.md    # ADR-001: Expansión digital
│   └── 2026-05-22-shopify-ecommerce.md    # ADR-002: Shopify
├── stack/
│   ├── overview.md                        # Mapa completo del stack
│   ├── google-workspace.md                # Google Suite
│   └── shopify.md                         # Shopify ecommerce
├── content/
│   ├── strategy.md                        # Estrategia de contenido
│   └── calendar-feb-mar-2026.md           # Calendario de referencia
└── reports/
    ├── reporte-estrategico-2026.html      # Reporte visual de resultados
    └── propuesta-comercial-2026-01.html   # Propuesta InnoGrowth (Ene 2026)
```

## Cómo mantener este repositorio

- **Nueva decisión estratégica** → crear archivo en `decisions/` + agregar fila a `decisions/_index.md`
- **Nueva tecnología** → actualizar `stack/overview.md` + crear archivo en `stack/`
- **Nuevo mes de contenido** → crear archivo en `content/calendar-[mes]-[año].md`
- **Datos desactualizados** → editar directamente el archivo correspondiente, los `[COMPLETAR]` son marcadores pendientes

## Responsables

| Rol | Persona |
|---|---|
| Estrategia digital | Jesús Reinaldo Barros Bolívar (InnoGrowth) |
| Negocio Naturchem | [COMPLETAR] |
