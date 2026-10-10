# Black Summer Fire Detection — Blue Mountains (2019-2020)

Detección multitemporal de severidad de quema del evento **Black Summer** (Australia, 2019-2020) en el Parque Nacional Blue Mountains mediante índices espectrales NBR y dNBR, utilizando imágenes Sentinel-2 y QGIS.

---

## Integrantes

- Sara Castro
- Maria Alejandra Garcia
- Juan David Ortiz
- Eliana Pardo
- Ana Maria Romero

**Curso:** Tecnologías Emergentes

---

## Descripción del Proyecto

Durante la temporada 2019-2020, Australia sufrió una de las peores crisis de incendios forestales de su historia, conocida como el "Black Summer". El megaincendio de **Gospers Mountain**, iniciado el 26 de octubre de 2019, consumió más de 510.000 hectáreas y afectó aproximadamente el 80% del Área de Patrimonio Mundial de las Blue Mountains.

Este proyecto evalúa la severidad de la quema en el Parque Nacional Blue Mountains mediante:

- Cálculo del **Normalized Burn Ratio (NBR)** para dos fechas (antes y después del incendio).
- Cálculo del **differenced Normalized Burn Ratio (dNBR)** para cuantificar la magnitud del cambio.
- Reclasificación del dNBR según los umbrales estándar del USGS (No quemado, Baja, Moderada y Alta severidad).

---

## Datos Utilizados

| Parámetro                | Especificación                            |
| ------------------------ | ----------------------------------------- |
| Misión                   | Sentinel-2 MSI (MultiSpectral Instrument) |
| Nivel de procesamiento   | Level-2A (BOA - Bottom-Of-Atmosphere)     |
| Teselas MGRS             | T56HKH y T56HKJ                           |
| Fecha pre-incendio (t1)  | 27 de septiembre de 2019                  |
| Fecha post-incendio (t2) | 19 de febrero de 2020                     |
| Bandas utilizadas        | B02, B03, B04, B08, B12                   |
| Proyección               | GDA2020 / MGA zone 56 (EPSG:7856)         |
| Plataforma de descarga   | Copernicus Data Space Ecosystem           |

---

## Acceso a las Capas del Proyecto

Todas las capas del proyecto (originales, mosaicos, recortes, NBR, dNBR y severidad) se encuentran alojadas en Google Drive debido a su tamaño (algunos archivos superan 1GB). Este es el **medio principal de descarga** para el proyecto.

🔗 **[Descargar Capas del Proyecto](https://drive.google.com/drive/folders/18ocPg6jwTcxh4KBdHqUr4ZonwC6s2EwE?usp=sharing)**

**Contenido en Drive:**

- `1. Capas Originales/` — Bandas B02, B03, B04, B08 y B12 de Sentinel-2 (t1 y t2)
- `2.1 Mosaicos Iniciales/` — Mosaicos por banda
- `2.2 Mosaicos Recortados/` — Mosaicos recortados al ROI
- `2.3 Mosaicos Terminados/` — Ráster multibanda unificado
- `2.4 Mosaicos NBR y dNBR/` — Índices y clases de severidad

**Fechas de referencia:**

- t1 (pre-incendio): 27 de septiembre de 2019
- t2 (post-incendio): 19 de febrero de 2020

---

## Metodología

El proyecto sigue un flujo de trabajo estructurado en cinco fases:

1. **Fase 1: Definición del problema y adquisición de datos**
   - Selección de fechas t1 y t2.
   - Descarga de imágenes Sentinel-2 L2A.

2. **Fase 2: Preprocesamiento**
   - Verificación del nivel de procesamiento (L2A, BOA).
   - Ensamblaje de mosaicos por banda.
   - Reproyección a EPSG:7856.
   - Remuestreo de B12 a 10 m.
   - Recorte al polígono del ROI.
   - Gestión de valores nulos (NoData).

3. **Fase 3: Procesamiento de imágenes y análisis**
   - Cálculo del NBR para t1 y t2.
   - Cálculo del dNBR.
   - Reclasificación por umbrales USGS.
   - Vectorización de polígonos de severidad.

4. **Fase 4: Post-procesamiento y evaluación de precisión**
   - Validación con imágenes de alta resolución.
   - Matriz de confusión, Kappa y F1-Score.

5. **Fase 5: Documentación y presentación**
   - Informe técnico en LaTeX.
   - Mapas temáticos.
   - Presentación oral.

---

## Referencias

- BoM (2020). _Black Summer_ — Bureau of Meteorology, Australia.
- Abatzoglou et al. (2021). Anthropogenic influences on Australian wildfires.
- Filkov et al. (2020). Impact of Australia's catastrophic 2019/20 bushfires.
- Key & Benson (2006). Landscape Assessment: Ground measure of severity, the Composite Burn Index.
- Lillesand et al. (2015). _Remote Sensing and Image Interpretation_.
