# Produtos FITS do LSST DP1

O **Legacy Survey of Space and Time Data Preview 1 (LSST DP1)** reúne produtos de imagens e catálogos gerados pelo Rubin Science Pipelines v29 a partir de observações reais da LSST Commissioning Camera (ComCam), realizadas em sete campos durante sete semanas de 2024. O lançamento oficial ocorreu em 30 de junho de 2025.

- [Documentação oficial do DP1](https://dp1.lsst.io/)
- [Produtos de imagem do DP1](https://dp1.lsst.io/products/images/index.html)
- [Citação oficial do dataset](https://doi.org/10.71929/rubin/2570308)

## Nível de acesso

!!! private "Acesso restrito"
    O DP1 é proprietário e está disponível somente para detentores de direitos de dados do Rubin, conforme a [política de dados](https://rubinobservatory.org/for-scientists/data-products/data-policy) e o documento [RDO-013](https://docushare.lsst.org/docushare/dsweb/Get/RDO-013).

## Produtos disponíveis no LIneA

!!! info "Inventário local"
    As quantidades apresentadas nesta página documentam os arquivos disponíveis na infraestrutura do LIneA. Elas podem divergir dos totais publicados pelo Rubin devido à organização e ao estado da cópia local.

## Cobertura do céu por banda

O DP1 observou sete campos de aproximadamente 1 grau quadrado cada. A cobertura não é igual entre as bandas:

- **u:** ECDFS, EDFS, campo de baixa latitude galáctica e Nebulosa da Gaivota.
- **g e r:** todos os sete campos.
- **i:** todos, exceto a Nebulosa da Gaivota.
- **z:** campo de baixa latitude eclíptica, ECDFS, EDFS, campo de baixa latitude galáctica e Nebulosa da Gaivota.
- **y:** 47 Tuc, ECDFS, EDFS e campo de baixa latitude galáctica.

A tabela apresenta o centro de cada campo e o número oficial de visitas por banda. Zero indica que o campo não foi observado naquela banda.

| Campo | Centro (RA, Dec; graus) | u | g | r | i | z | y |
|---|---|---:|---:|---:|---:|---:|---:|
| Aglomerado globular 47 Tuc | 6,02; −72,08 | 0 | 10 | 32 | 19 | 0 | 5 |
| Campo de baixa latitude eclíptica | 37,86; 6,98 | 0 | 44 | 40 | 55 | 20 | 0 |
| Galáxia anã esferoidal de Fornax | 40,00; −34,45 | 0 | 5 | 25 | 12 | 0 | 0 |
| Extended Chandra Deep Field South (ECDFS) | 53,13; −28,10 | 43 | 230 | 237 | 162 | 153 | 30 |
| Euclid Deep Field South (EDFS) | 59,10; −48,73 | 20 | 61 | 87 | 42 | 42 | 20 |
| Campo de baixa latitude galáctica | 95,00; −25,00 | 33 | 82 | 84 | 23 | 60 | 10 |
| Nebulosa da Gaivota | 106,23; −10,51 | 10 | 37 | 43 | 0 | 10 | 0 |

!!! info "Como interpretar a cobertura"
    Esses números descrevem as visitas observadas pelo Rubin. Os deep coadds incluem somente exposições que atendem aos critérios de qualidade; patches de borda podem ter regiões sem dados, identificadas pela máscara `NO_DATA`. A quantidade de arquivos locais por banda aparece nas tabelas de produtos abaixo.

Fontes oficiais: [observações e filtros](https://dp1.lsst.io/overview/observations.html), [qualidade e profundidade das imagens](https://dp1.lsst.io/overview/iqsummary.html) e [processamento dos coadds](https://dp1.lsst.io/processing/coaddition/index.html).

### Deep coadd

Combinação, por banda e região do céu, de exposições calibradas e com background subtraído. O empilhamento usa média ponderada pelo inverso da variância. Cada arquivo representa um patch em uma das seis bandas `u`, `g`, `r`, `i`, `z` e `y`.

- **Formato:** FITS (`.fits`)
- **Inventário local:** 2.654 arquivos, 166 GB
- **Conteúdo:** planos de imagem (nJy), variância (nJy²) e máscara, além de PSF, calibração fotométrica e WCS
- **Documentação oficial:** [Deep coadd](https://dp1.lsst.io/products/images/deep_coadd.html), [coadição de imagens](https://dp1.lsst.io/processing/coaddition/index.html) e [planos de máscara](https://dp1.lsst.io/products/images/deep_coadd_mask_planes.html)

| Banda | Arquivos | Tamanho |
|---|---:|---:|
| u | 274 | 16 GB |
| g | 583 | 37 GB |
| r | 581 | 39 GB |
| i | 510 | 32 GB |
| z | 432 | 28 GB |
| y | 263 | 15 GB |

### Deep coadd background

Mapas bidimensionais do nível de fundo do céu medido e subtraído das imagens deep coadd.

- **Formato:** FITS (`.fits`)
- **Inventário local:** 2.655 arquivos, 53 MB
- **Documentação relacionada:** [subtração de background](https://dp1.lsst.io/processing/calibration/backgrounds.html) e [coadição de imagens](https://dp1.lsst.io/processing/coaddition/index.html)

| Banda | Arquivos | Tamanho |
|---|---:|---:|
| u | 274 | 5,5 MB |
| g | 583 | 12 MB |
| r | 582 | 12 MB |
| i | 510 | 11 MB |
| z | 432 | 8,6 MB |
| y | 263 | 5,2 MB |

!!! note
    `deep_coadd_background` é um produto preservado na cópia do IDAC-BR, mas não possui uma página própria entre os tipos de imagens publicados na documentação oficial do DP1.

### Deep coadd n-image

Mapas bidimensionais com o número de exposições empilhadas em cada pixel do deep coadd. São úteis para avaliar cobertura e profundidade relativa.

- **Formato:** FITS (`.fits`)
- **Inventário local:** 2.721 arquivos, 1,7 GB
- **Documentação relacionada:** [Deep coadd](https://dp1.lsst.io/products/images/deep_coadd.html)

| Banda | Arquivos | Tamanho |
|---|---:|---:|
| u | 280 | 126 MB |
| g | 594 | 391 MB |
| r | 601 | 439 MB |
| i | 520 | 306 MB |
| z | 444 | 272 MB |
| y | 271 | 112 MB |

!!! note
    `deep_coadd_n_image` é um produto preservado na cópia do IDAC-BR, mas não aparece como tipo de imagem independente na documentação oficial do DP1.

### Mapas HealSparse FITS

Doze mapas de propriedades do levantamento, com um arquivo por banda (`u`, `g`, `r`, `i`, `z`, `y`), totalizando 72 arquivos e 451 MB. O formato é FITS com extensão `.hsp`.

- **Documentação oficial:** [Survey property maps](https://dp1.lsst.io/products/spmaps/index.html)

| Produto | Descrição |
|---|---|
| `deepCoadd_dcr_ddec_consolidated_map_weighted_mean` | Deslocamento DCR médio ponderado em declinação |
| `deepCoadd_dcr_dra_consolidated_map_weighted_mean` | Deslocamento DCR médio ponderado em ascensão reta |
| `deepCoadd_dcr_e1_consolidated_map_weighted_mean` | Componente `e1` média ponderada da distorção DCR |
| `deepCoadd_dcr_e2_consolidated_map_weighted_mean` | Componente `e2` média ponderada da distorção DCR |
| `deepCoadd_epoch_consolidated_map_max` | Época máxima das exposições contribuintes |
| `deepCoadd_epoch_consolidated_map_mean` | Época média das exposições contribuintes |
| `deepCoadd_epoch_consolidated_map_min` | Época mínima das exposições contribuintes |
| `deepCoadd_psf_e1_consolidated_map_weighted_mean` | Componente `e1` média ponderada da PSF |
| `deepCoadd_psf_e2_consolidated_map_weighted_mean` | Componente `e2` média ponderada da PSF |
| `deepCoadd_psf_size_consolidated_map_weighted_mean` | Tamanho médio ponderado da PSF |
| `deepCoadd_sky_background_consolidated_map_weighted_mean` | Nível médio ponderado do background do céu |
| `deepCoadd_sky_noise_consolidated_map_weighted_mean` | Ruído médio ponderado do céu |

## Limites deste inventário

Esta página descreve somente os produtos FITS atualmente documentados na cópia local do LIneA. O DP1 oficial também oferece outros produtos de imagem — como raw exposures, visit images, template coadds e difference images — que não estão registrados como disponíveis nesses diretórios locais. Consulte o [índice oficial de imagens](https://dp1.lsst.io/products/images/index.html).
