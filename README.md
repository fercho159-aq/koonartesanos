# Reporte de auditoría — Koon Artesanos / Alfa Jardín

Reporte comparativo técnico y estratégico de la transición entre la tienda
Shopify de Koon Artesanos y el nuevo sitio independiente `koonartesanos.com`.

- **Entregable:** [`reporte-auditoria-koon-artesanos.html`](reporte-auditoria-koon-artesanos.html)
- **Formato:** HTML autocontenido (sin dependencias externas), responsive y con
  hoja de estilo de impresión. Se abre directamente en el navegador o se exporta
  a PDF con *Imprimir → Guardar como PDF*.

Versión orientada a cliente: lenguaje llano, sin jerga técnica y apoyada en
mediciones reales de herramientas.

## Bloques

1. En una página — marcador comparativo y los cuatro fallos a corregir
2. Comparativa SEO — datos reales de SEOQuake sobre ambos sitios
3. Seguridad — qué cambió al salir de una plataforma administrada
4. Velocidad — pendiente de PageSpeed Insights y Pingdom Tools
5. Qué hacer ahora — doce acciones priorizadas y calendario
6. Glosario

## Origen de los datos

| Bloque | Herramienta | Estado |
|---|---|---|
| Comparativa SEO | SEOQuake (ambos sitios) | Datos reales incorporados |
| Velocidad | PageSpeed Insights (ambos sitios) | Datos reales incorporados |
| Velocidad | Pingdom Tools (ambos sitios) | Datos reales incorporados |
| Seguridad | Revisión de servidor | Pendiente de ejecutar |

Las tres herramientas SEO y de rendimiento están completas. Queda pendiente
únicamente la revisión de configuración del servidor descrita en el bloque 3
(certificado, actualizaciones y protección de formularios), señalada como tal
en el documento. No se publican cifras estimadas.

## Personalización visual

La paleta y la tipografía se definen como variables CSS al inicio del archivo
(`:root`). Sustituir esos valores por los tokens exactos del manual de marca
actualiza todo el documento.
