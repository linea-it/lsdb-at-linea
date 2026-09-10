# Productos FITS del LSST DP1

El **Legacy Survey of Space and Time Data Preview 1 (LSST DP1)** contiene productos de imágenes y catálogos generados por Rubin Science Pipelines v29 a partir de observaciones reales de la LSST Commissioning Camera (ComCam), realizadas en siete campos durante siete semanas de 2024. El lanzamiento oficial fue el 30 de junio de 2025.

- [Documentación oficial del DP1](https://dp1.lsst.io/)
- [Productos de imagen del DP1](https://dp1.lsst.io/products/images/index.html)
- [Citación oficial del conjunto](https://doi.org/10.71929/rubin/2570308)

## Nivel de acceso

!!! private "Acceso restringido"
    El DP1 es propietario y está disponible solamente para titulares de derechos de datos de Rubin, según la [política de datos](https://rubinobservatory.org/for-scientists/data-products/data-policy) y el documento [RDO-013](https://docushare.lsst.org/docushare/dsweb/Get/RDO-013).

## Productos disponibles en LIneA

!!! info "Inventario local"
    Las cantidades presentadas en esta página documentan los archivos disponibles en la infraestructura de LIneA. Pueden diferir de los totales publicados por Rubin debido a la organización y al estado actual de la copia local.

## Cobertura del cielo por banda

El DP1 observó siete campos de aproximadamente un grado cuadrado cada uno. La cobertura no es igual entre las bandas:

- **u:** ECDFS, EDFS, campo de baja latitud galáctica y Nebulosa de la Gaviota.
- **g y r:** los siete campos.
- **i:** todos excepto la Nebulosa de la Gaviota.
- **z:** campo de baja latitud eclíptica, ECDFS, EDFS, campo de baja latitud galáctica y Nebulosa de la Gaviota.
- **y:** 47 Tuc, ECDFS, EDFS y campo de baja latitud galáctica.

La tabla presenta el centro de cada campo y el número oficial de visitas por banda. Cero indica que el campo no fue observado en esa banda.

| Campo | Centro (RA, Dec; grados) | u | g | r | i | z | y |
|---|---|---:|---:|---:|---:|---:|---:|
| Cúmulo globular 47 Tuc | 6,02; −72,08 | 0 | 10 | 32 | 19 | 0 | 5 |
| Campo de baja latitud eclíptica | 37,86; 6,98 | 0 | 44 | 40 | 55 | 20 | 0 |
| Galaxia enana esferoidal de Fornax | 40,00; −34,45 | 0 | 5 | 25 | 12 | 0 | 0 |
| Extended Chandra Deep Field South (ECDFS) | 53,13; −28,10 | 43 | 230 | 237 | 162 | 153 | 30 |
| Euclid Deep Field South (EDFS) | 59,10; −48,73 | 20 | 61 | 87 | 42 | 42 | 20 |
| Campo de baja latitud galáctica | 95,00; −25,00 | 33 | 82 | 84 | 23 | 60 | 10 |
| Nebulosa de la Gaviota | 106,23; −10,51 | 10 | 37 | 43 | 0 | 10 | 0 |

!!! info "Cómo interpretar la cobertura"
    Estas cifras describen las visitas observadas por Rubin. Los deep coadds incluyen solamente exposiciones que cumplen los criterios de calidad; los patches de borde pueden contener regiones sin datos, identificadas por la máscara `NO_DATA`. Las cantidades de archivos locales por banda aparecen en las tablas de productos siguientes.

Fuentes oficiales: [observaciones y filtros](https://dp1.lsst.io/overview/observations.html), [calidad y profundidad de las imágenes](https://dp1.lsst.io/overview/iqsummary.html) y [procesamiento de los coadds](https://dp1.lsst.io/processing/coaddition/index.html).

### Deep coadd

Combinación por banda y región del cielo de exposiciones calibradas y con el fondo sustraído, mediante una media ponderada por el inverso de la varianza. Cada archivo representa un patch en una de las seis bandas `u`, `g`, `r`, `i`, `z` e `y`.

- **Formato:** FITS (`.fits`)
- **Inventario local:** 2654 archivos, 166 GB
- **Contenido:** planos de imagen (nJy), varianza (nJy²) y máscara, además de PSF, calibración fotométrica y WCS
- **Documentación oficial:** [Deep coadd](https://dp1.lsst.io/products/images/deep_coadd.html), [coadición de imágenes](https://dp1.lsst.io/processing/coaddition/index.html) y [planos de máscara](https://dp1.lsst.io/products/images/deep_coadd_mask_planes.html)

| Banda | Archivos | Tamaño |
|---|---:|---:|
| u | 274 | 16 GB |
| g | 583 | 37 GB |
| r | 581 | 39 GB |
| i | 510 | 32 GB |
| z | 432 | 28 GB |
| y | 263 | 15 GB |

### Deep coadd background

Mapas bidimensionales del nivel de fondo del cielo medido y sustraído de las imágenes deep coadd.

- **Formato:** FITS (`.fits`)
- **Inventario local:** 2655 archivos, 53 MB
- **Documentación relacionada:** [sustracción de fondo](https://dp1.lsst.io/processing/calibration/backgrounds.html) y [coadición de imágenes](https://dp1.lsst.io/processing/coaddition/index.html)

| Banda | Archivos | Tamaño |
|---|---:|---:|
| u | 274 | 5,5 MB |
| g | 583 | 12 MB |
| r | 582 | 12 MB |
| i | 510 | 11 MB |
| z | 432 | 8,6 MB |
| y | 263 | 5,2 MB |

!!! note
    `deep_coadd_background` se conserva en la copia del IDAC-BR, pero no posee una página propia entre los tipos de imágenes publicados en la documentación oficial del DP1.

### Deep coadd n-image

Mapas bidimensionales con el número de exposiciones apiladas en cada píxel del deep coadd. Son útiles para evaluar la cobertura y la profundidad relativa.

- **Formato:** FITS (`.fits`)
- **Inventario local:** 2721 archivos, 1,7 GB
- **Documentación relacionada:** [Deep coadd](https://dp1.lsst.io/products/images/deep_coadd.html)

| Banda | Archivos | Tamaño |
|---|---:|---:|
| u | 280 | 126 MB |
| g | 594 | 391 MB |
| r | 601 | 439 MB |
| i | 520 | 306 MB |
| z | 444 | 272 MB |
| y | 271 | 112 MB |

!!! note
    `deep_coadd_n_image` se conserva en la copia del IDAC-BR, pero no aparece como tipo de imagen independiente en la documentación oficial del DP1.

### Mapas HealSparse FITS

Doce mapas de propiedades del levantamiento, con un archivo por banda (`u`, `g`, `r`, `i`, `z`, `y`), totalizando 72 archivos y 451 MB. Utilizan FITS con extensión `.hsp`.

- **Documentación oficial:** [Survey property maps](https://dp1.lsst.io/products/spmaps/index.html)

| Producto | Descripción |
|---|---|
| `deepCoadd_dcr_ddec_consolidated_map_weighted_mean` | Desplazamiento DCR medio ponderado en declinación |
| `deepCoadd_dcr_dra_consolidated_map_weighted_mean` | Desplazamiento DCR medio ponderado en ascensión recta |
| `deepCoadd_dcr_e1_consolidated_map_weighted_mean` | Componente `e1` media ponderada de la distorsión DCR |
| `deepCoadd_dcr_e2_consolidated_map_weighted_mean` | Componente `e2` media ponderada de la distorsión DCR |
| `deepCoadd_epoch_consolidated_map_max` | Época máxima de las exposiciones contribuyentes |
| `deepCoadd_epoch_consolidated_map_mean` | Época media de las exposiciones contribuyentes |
| `deepCoadd_epoch_consolidated_map_min` | Época mínima de las exposiciones contribuyentes |
| `deepCoadd_psf_e1_consolidated_map_weighted_mean` | Componente `e1` media ponderada de la PSF |
| `deepCoadd_psf_e2_consolidated_map_weighted_mean` | Componente `e2` media ponderada de la PSF |
| `deepCoadd_psf_size_consolidated_map_weighted_mean` | Tamaño medio ponderado de la PSF |
| `deepCoadd_sky_background_consolidated_map_weighted_mean` | Nivel medio ponderado del fondo del cielo |
| `deepCoadd_sky_noise_consolidated_map_weighted_mean` | Ruido medio ponderado del cielo |

## Límites del inventario

Esta página describe solamente los productos FITS actualmente documentados en la copia local de LIneA. El DP1 oficial también ofrece raw exposures, visit images, template coadds y difference images que no están registrados como disponibles en estos directorios locales. Consulta el [índice oficial de productos de imagen](https://dp1.lsst.io/products/images/index.html).
