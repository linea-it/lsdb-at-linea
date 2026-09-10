# Databases

LIneA provides public and private astronomical catalogs in **PostgreSQL** databases through the [User Query](https://userquery.linea.org.br/) platform. Users can query the data with **SQL** or **ADQL** and save results as tables in their personal area (MyDB), which is also accessible from [Target Viewer](https://target.linea.org.br/) and [JupyterHub](https://jupyter.linea.org.br/).

## Available content

### [Dark Energy Survey - Data Release 2](https://userquery.linea.org.br/metadata/des_dr2/) (`des_dr2`)

A photometric catalog from the DES survey covering approximately 5,000 square degrees of the southern sky, with astrometry, *grizY* photometry, star/galaxy classification, and quality flags.

### [DES Year 6 Gold](https://userquery.linea.org.br/metadata/des_y6_gold/) (`des_y6_gold`)

Final DES Y6 products for cosmological analyses: the Gold galaxy and star catalog, a WaZP galaxy cluster catalog, and its member galaxies, including membership probabilities and photometry.

### [Gaia Data Release 3](https://userquery.linea.org.br/metadata/gaia_dr3/) (`gaia_dr3`)

Gaia DR3 astrometric and photometric data, including positions, parallaxes, proper motions, radial velocities, variability, astrophysical parameters, and source classifications.

### [LSST Data Preview 1](https://userquery.linea.org.br/metadata/lsst_dp1/) (`lsst_dp1`)

Catalogs produced from Rubin Observatory Data Preview 1, with source and object measurements derived from the first LSSTComCam observations and related products.

### [Minor Planet Center - SBN mirror](https://userquery.linea.org.br/metadata/mpc_sbn/) (`mpc_sbn`)

A mirror of Minor Planet Center data provided by the Small Bodies Node, with observations, orbits, designations, names, and observatory information for small Solar System bodies. Some tables remain under development or are only partially populated.

### [Two Micron All Sky Survey](https://userquery.linea.org.br/metadata/twomass/) (`twomass`)

The 2MASS Point Source Catalog, from a near-infrared survey of nearly the entire sky, containing positions, magnitudes, and quality indicators in the *J*, *H*, and *Ks* bands.

Complete descriptions of schemas, tables, and columns are available directly in [User Query](https://userquery.linea.org.br/). Instructions, tutorials, and query examples are provided in the [platform documentation](https://userquery.linea.org.br/cms/services/).

!!! abstract "🔒 Access control"
    Schema availability follows each project's data policy. Restricted catalogs are visible and queryable only to authorized users.
