# 2.4 Mosaicos NBR y dNBR

Índices espectrales calculados a partir del ráster multibanda, incluyendo el NBR para ambas fechas, el dNBR, las clases de severidad y los productos vectoriales derivados.

🔗 **[Descargar Mosaicos NBR y dNBR](https://drive.google.com/drive/folders/1-e7NFW8J_ZuteHfsDllwwZPJ7ze0pxLy?usp=sharing)**

**Contenido ráster:**

- `NBR_t1.tif`: Normalized Burn Ratio pre-incendio
- `NBR_t2.tif`: Normalized Burn Ratio post-incendio
- `dNBR.tif`: Differenced NBR (NBR_t1 − NBR_t2)
- `dNBR_clases_severidad.tif`: Ráster reclasificado por umbrales USGS

**Contenido vectorial:**

- `severidad_poligonos_raw.gpkg`: Polígonos de severidad sin filtrar (todas las clases)
- `cicatriz_blue_mountains.gpkg`: Polígonos filtrados con `clase_id > 2` (severidad moderada y alta)
- `area_por_severidad.gpkg`: Tabla de estadísticas zonales con el área total por clase de severidad

**Clases de severidad (USGS):**

| Rango dNBR  | Clase              |
| ----------- | ------------------ |
| < 0.10      | No quemado         |
| 0.10 – 0.27 | Baja severidad     |
| 0.27 – 0.66 | Moderada severidad |
| > 0.66      | Alta severidad     |

**Áreas afectadas (> 2):**

| Clase              | Polígonos   | Área (ha)      |
| ------------------ | ----------- | -------------- |
| Moderada severidad | 208.725     | 202.871,44     |
| Alta severidad     | 6.830       | 357,59         |
| **Total**          | **215.555** | **203.229,03** |
