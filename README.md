# Reporte de auditoría — Koon Artesanos / Alfa Jardín

Reporte comparativo técnico y estratégico de la transición entre la tienda
Shopify de Koon Artesanos y el nuevo sitio independiente `koonartesanos.com`.

- **Entregable:** [`reporte-auditoria-koon-artesanos.html`](reporte-auditoria-koon-artesanos.html)
- **Formato:** HTML autocontenido (sin dependencias externas), responsive y con
  hoja de estilo de impresión. Se abre directamente en el navegador o se exporta
  a PDF con *Imprimir → Guardar como PDF*.

## Bloques

0. Alcance, método y trazabilidad del dato
1. Resumen ejecutivo
2. Auditoría de seguridad web (TLS, cabeceras HTTP, SaaS gestionado vs. sitio a medida)
3. Auditoría SEO on-page y técnico (criterios SEOQuake)
4. Rendimiento y Core Web Vitals (PageSpeed Insights / Pingdom)
5. Plan de acción y roadmap de corrección
6. Anexos: protocolo de verificación, trazabilidad de evidencia y glosario

## Nota sobre los datos

El reporte se elaboró desde un entorno con egreso de red restringido, sin acceso
HTTP directo a los dominios auditados.

- Los hallazgos de **arquitectura, indexación, URLs y metadatos** se sustentan en
  evidencia real recuperada del índice público de buscadores y están marcados
  como *Evidencia* (la trazabilidad completa está en el bloque 6.4).
- Las métricas que exigen respuesta del servidor (cadena TLS, cabeceras HTTP,
  LCP/INP/CLS/TTFB, peso de página) **no se estimaron ni se inventaron**: aparecen
  como *Pendiente*, junto al umbral de referencia y al comando exacto para
  obtenerlas. El bloque 6 permite completarlas en ~45 minutos sin alterar ninguna
  conclusión estructural.

## Personalización visual

La paleta y la tipografía se definen como variables CSS al inicio del archivo
(`:root`). Sustituir esos valores por los tokens exactos del manual de marca
actualiza todo el documento.
