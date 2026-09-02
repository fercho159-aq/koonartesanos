# Handoff — Auditoría web Koon Artesanos

Documento de traspaso. Contiene todo lo necesario para continuar el trabajo
sin acceso a la conversación original.

---

## 1. Contexto

**Cliente:** Koon Artesanos (razón social: Koon Blanc, S.A. de C.V.).
Marca mexicana fundada en 2002. Artículos de piel 100 % hechos a mano por
artesanos mexicanos: decoración, interiorismo, accesorios personales y —línea
de mayor ticket— **regalos corporativos**. Tienda física en Prado Norte 540,
CDMContacto: contacto@koonartesanos.com. ~29 K seguidores en Instagram.

**Situación:** la marca migró de una tienda Shopify (plantilla comprada,
código sobrescrito por varios desarrolladores, diseño desalineado de la
identidad) a un sitio independiente fuera de Shopify. El encargo original fue
auditar la transición en seguridad, SEO técnico y rendimiento.

**Propiedades web implicadas:**

| Host | Plataforma | Estado |
|---|---|---|
| `koonartesanos.com` (y `www.`) | Desarrollo a medida | Activo — sitio nuevo |
| `store.koonartesanos.com` | Shopify | Activo e indexado |
| `koonartesanos.myshopify.com` | Shopify (dominio técnico) | Activo e indexado |

Los tres sirven catálogo simultáneamente. La tienda Shopify **sí declara
canonical hacia `koonartesanos.com`**, pero no hay redirecciones 301.

---

## 2. Datos medidos (1 de septiembre de 2026)

Todas las cifras son mediciones reales. **Ninguna es estimada.**

### 2.1 SEOQuake — portada de cada sitio

| Concepto | Shopify | Sitio nuevo |
|---|---|---|
| Aprobados / Avisos / Errores | 15 / 5 / 1 | 16 / 3 / 2 |
| Título | «Accesorios de piel y regalos corporativos \| Koon Artesanos» (58 car.) | «Koon Artesanos» (14 car.) |
| Meta descripción | 220 caracteres | 294 caracteres |
| Encabezados | H1:1, H2:1, H4:2 | **H1:0**, H2:27, H3:1, H4:74, H5:1, H6:53 |
| Texto / HTML | 22,55 % | **2,9 %** (error) |
| Sitemap XML | Sí | **No existe** (error) |
| robots.txt | Sí | Sí |
| Schema.org | No (error) | Sí — `Organization` |
| Idioma declarado | `en` (incorrecto) | `es` (correcto) |
| Imágenes con ALT | Todas | Todas |
| Marcos (iframe) | Sí | No |
| Enlaces internos / externos | 32 / 15 | 71 / 5 |
| Palabras en portada | 201 | 847 |
| Backlinks (L / LD / LRD) | 0 / 0 / 0 | 213 / 259 / 356 |
| Canonical | → `https://koonartesanos.com/` | → `https://www.koonartesanos.com` |
| Open Graph / Twitter Card | Sí / tipo indeterminado | Sí / tipo indeterminado |

**Densidad de palabras — Shopify:** piel 3,98 %, colores 3,48 %, oficina 2,99 %,
hogar, vinos, viajes, mujer, hombre, catálogo 2,99 %. Frases: «de piel» 7,96 %,
«colores de piel» 10,45 %, «regalos corporativos» 3,98 %, «bordado otomí»,
«artesanía huichol», «papel amate».

**Densidad — sitio nuevo:** piel 3,78 % (32 apariciones), más 1,77 %, para,
ver 1,42 %, regalos, premium 1,30 %. Frases: «de piel» 3,54 %, «ver más» 2,83 %,
«piel genuina» 1,89 %, «regalos corporativos» 1,18 %. Aparecen fechas sueltas
del blog («prehispánico 07 31 2017») entre los términos más repetidos.

### 2.2 Google PageSpeed Insights

Puntuaciones sobre 100:

| Categoría | Shopify escritorio | Shopify móvil | Nuevo escritorio | Nuevo móvil |
|---|---|---|---|---|
| Rendimiento | 65 | 51 | **79** | **48** |
| Accesibilidad | 84 | 91 | 85 | 85 |
| Prácticas recomendadas | 73 | 73 | 92 | 96 |
| SEO | 100 | 100 | 100 | 100 |
| Navegación agéntica | 3/4 | 4/4 | 1/2 | 1/2 |

Métricas:

| Métrica | Shopify escritorio | Shopify móvil | Nuevo escritorio | Nuevo móvil |
|---|---|---|---|---|
| FCP | 0,7 s | 8,5 s | 0,5 s | 4,6 s |
| LCP | 1,2 s | **20,5 s** | 2,7 s | **16,7 s** |
| TBT | 810 ms | 280 ms | 70 ms | 540 ms |
| CLS | 0,001 | 0 | 0,001 | 0 |
| Speed Index | 2,3 s | 9,5 s | 2,6 s | 5,9 s |

Móvil: Moto G Power emulado, 4G lenta, Lighthouse 13.4.1.
**Ninguno de los dos sitios tiene datos de campo (CrUX)**: no alcanzan el
volumen mínimo de visitas.

### 2.3 Pingdom Tools (Washington D.C., banda ancha)

| Concepto | Shopify | Sitio nuevo |
|---|---|---|
| Calificación | D · 66 | **B · 82** |
| Peso de página | 2,9 MB | **542,6 KB** |
| Peticiones | 159 | **19** |
| Tiempo de carga | 923 ms | **292 ms** |

---

## 3. Conclusiones

### 3.1 El sitio nuevo está mejor construido que el anterior

Gana en peso (5×), peticiones (8×), tiempo de carga (3×), rendimiento en
escritorio (79 vs 65), prácticas recomendadas (92-96 vs 73), contenido
(847 vs 201 palabras), enlaces internos (71 vs 32), idioma declarado,
Schema.org y perfil de backlinks (213 vs 0).

La narrativa inicial del encargo —«la agencia descuidó el SEO»— resultó
**parcialmente incorrecta**: el trabajo técnico de base está bien hecho; lo
que faltó fue el acabado.

### 3.2 Fallos reales del sitio nuevo

1. **LCP móvil 16,7 s** (umbral 2,5 s) — el más caro comercialmente.
2. **No existe `sitemap.xml`.**
3. **H1 = 0** en la portada.
4. **Título de 14 caracteres** sin palabras clave («Koon Artesanos»).
5. **Texto/HTML 2,9 %** (mínimo sano 15 %).
6. Secundarios: meta descripción de 294 car. (se corta ~160), jerarquía de
   encabezados caótica (74 H4, 53 H6 usados como estilo), accesibilidad 85,
   navegación agéntica 1/2, texto de relleno («ver más») y fechas sueltas
   mezcladas con el contenido.

### 3.3 Causa raíz del LCP — hallazgo clave

Pingdom y PageSpeed parecen contradecirse (292 ms vs 16,7 s). No se
contradicen: **con 542 KB de peso total, la lentitud no puede deberse al
tamaño de las imágenes.** La única explicación compatible con las tres
herramientas es que la imagen de portada **no viene en la carga inicial** y se
solicita después de descargar y ejecutar el JavaScript. En escritorio esa
cadena es instantánea; en 4G con teléfono de gama media son ~15 s de pantalla
vacía.

**Implicación práctica:** la corrección es de **orden de carga** (declarar la
imagen LCP en el HTML inicial con prioridad alta, `preload` / `fetchpriority`,
quitar cualquier `lazy` sobre ella), **no de compresión de imágenes**. Es más
acotada y más barata de lo que sugería el diagnóstico inicial.

**Causas distintas por plataforma:** Shopify es lento por peso bruto (2,9 MB,
159 archivos); el sitio nuevo por secuencia de carga.

### 3.4 Correcciones de diagnóstico ocurridas durante el trabajo

Registradas para que no se repitan errores ya descartados:

- ~~«No hay ninguna señal de consolidación hacia el .com»~~ → **falso**: la
  tienda Shopify sí declara canonical hacia `koonartesanos.com`. Lo que falta
  son las 301.
- ~~«Los metadatos se renderizan por JavaScript»~~ → **descartado**: SEOQuake
  lee título y descripción sin problema; el título existe, solo es corto.
- ~~«La lentitud móvil la causó la migración»~~ → **falso**: Shopify era peor
  (20,5 s vs 16,7 s).
- ~~«La ausencia de datos CrUX confirma el bajo tráfico del sitio nuevo»~~ →
  **matizado**: falta en ambas plataformas; habla del tráfico de la marca en
  conjunto.
- ~~«Hay que optimizar/comprimir la imagen de portada»~~ → **reformulado**: el
  problema es el orden de carga, no el peso (ver 3.3).

### 3.5 Seguridad — sin medir

No se ha ejecutado revisión de servidor. Pendiente comprobar: cadena TLS y
cobertura de `www`/no-`www`, caducidad y alerta, cabeceras HTTP (HSTS, CSP,
X-Frame-Options, X-Content-Type-Options, Referrer-Policy, Permissions-Policy),
política de actualizaciones, protección de formularios, copias de seguridad
con restauración probada, WAF/CDN.

Punto favorable verificado: el sitio publica **Aviso de Privacidad** conforme
a LFPDPPP, con responsable identificado, domicilio del área de datos
personales y canal de revocación.

Punto a verificar: que las **políticas de servicio y devoluciones** que
existían en Shopify (`/pages/politicas-de-servicio`) estén publicadas en el
sitio nuevo.

---

## 4. Plan de acción vigente (8 acciones)

| # | Acción | Prioridad |
|---|---|---|
| 1 | Corregir el orden de carga de la imagen de portada en celular | Alta |
| 2 | Publicar `sitemap.xml` | Alta |
| 3 | Añadir H1 único por página | Alta |
| 4 | Reescribir títulos y meta descripciones con intención de búsqueda | Alta |
| 5 | Decidir el futuro de la tienda Shopify y redirigir con 301 | Alta |
| 6 | Revisar seguridad del servidor | Alta |
| 7 | Aligerar código y ordenar contenido | Media |
| 8 | Crear landing de regalos corporativos con formulario | Media |

**Métricas de éxito a 90 días:** velocidad móvil 48 → 90+, LCP móvil 16,7 s →
<2,5 s, errores SEOQuake 2 → 0, texto/HTML 2,9 % → >15 %, peso <1,5 MB,
Pingdom B 82 → A 90+, accesibilidad 85 → 90+, solicitudes corporativas
medidas y en crecimiento.

### Mapa 301 (base, ampliable con la exportación completa de Shopify)

URLs de origen verificadas en el índice público:
`/collections/all`, `/collections/oficina`, `/collections/decoracion`,
`/collections/charolas-de-piel`, `/collections/all/marcos`,
`/collections/regalos-corporativos`, `/collections/regalos-corporativos-premium`,
`/collections/koon-artesanos-artesanos-a-a`, `/collections/te-amamos-mexico`,
`/collections/productos-seleccionados`, `/products/porta-lapices`,
`/products/charola-cama`, `/products/charola-rectangular-chica`,
`/products/basurero-redondo`, `/products/perchero-trajes`,
`/products/cartera-hombre`, `/products/archivero`, `/pages/sobre-nosotros`,
`/pages/politicas-de-servicio`, `/pages/bolsa-de-trabajo`,
`/pages/koon-artesanos-prado-norte`, `/blogs/noticias`.

Reglas: 301 y no 302, un solo salto, sin bucles ni destinos 404, mantener
12 meses mínimo. El dominio `myshopify.com` nunca debe ser indexable —
verificar la asignación de dominio primario en Shopify.

**Patrón de título que funcionaba en Shopify y conviene recuperar:**
`{Producto} 100% de piel hecho a mano | Koon Artesanos`

---

## 5. Entregable actual

- **Repositorio:** `fercho159-aq/koonartesanos`
- **Rama:** `claude/koon-artesanos-migration-audit-v9ozbv`
- **Archivo:** `reporte-auditoria-koon-artesanos.html` — HTML autocontenido,
  sin dependencias externas, responsive, con hoja de impresión (exporta a PDF
  desde el navegador). ~351 líneas / 24 KB.

**Estructura (5 secciones):** El veredicto · Los números · Las pruebas ·
El único fallo grave explicado · Qué hacer.

**Estilos:** paleta de marca (tonos piel/artesanía) en variables CSS al inicio
del archivo (`:root`). Sustituir esos tokens actualiza todo el documento.
Tipografía serif (Georgia) para títulos, sans del sistema para cuerpo.
Los medidores circulares de PageSpeed están reproducidos en SVG inline con la
misma escala de color de Google (rojo <50, naranja 50-89, verde 90+).

**Capturas:** las 14 capturas de las herramientas están en `capturas/` con
nombres descriptivos y ya incorporadas. Seis se muestran en el cuerpo del
reporte (diagnóstico SEOQuake de cada sitio, PageSpeed móvil de cada sitio y
Pingdom de cada sitio) y ocho quedan enlazadas como material complementario
(densidad de palabras clave y detalle de métricas de PageSpeed en ambos
dispositivos). Inventario completo en `capturas/LEEME.md`.

**Historial:** existe una versión anterior más extensa (692 líneas, 13
acciones, glosario, protocolo de verificación con comandos) en el commit
`e5b1844`, recuperable si se necesita un anexo técnico para desarrollo.

---

## 6. Pendientes

1. **Revisión de seguridad del servidor** — requiere acceso al hosting; no se
   puede medir desde fuera.
2. **Decisión de dirección** sobre el futuro de la tienda Shopify.
3. Opcional: exportación completa de URLs de Shopify para cerrar el mapa 301.

---

## 7. Restricciones del entorno de trabajo

Relevantes si se continúa con otra IA en condiciones similares:

- El entorno tenía **egreso de red bloqueado** hacia los dominios auditados:
  no fue posible hacer `curl` ni cargar los sitios. Todas las mediciones
  provienen de capturas de herramientas aportadas por el cliente, más
  evidencia recuperada del índice público de buscadores.
- Las imágenes pegadas en el chat **no se pueden guardar en disco** desde el
  asistente; deben aportarse como archivos.
