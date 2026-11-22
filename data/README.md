# Data

The included files are the same prepared 2023 emissions table and country
boundaries used in the course's mapping lecture. They are included here so this
homework works independently of the course repository.

## Emissions: `co2_2023.csv`

Source: [Our World in Data CO2 data](https://github.com/owid/co2-data), pinned to
commit [`382ee6c662b0ece26e111f263b44c029afad7787`](https://github.com/owid/co2-data/tree/382ee6c662b0ece26e111f263b44c029afad7787),
drawing on the Global Carbon Budget. Population sources are documented in the
[pinned codebook](https://github.com/owid/co2-data/blob/382ee6c662b0ece26e111f263b44c029afad7787/owid-co2-codebook.csv).

Each row is one country in 2023. The extract contains 169 rows, selected by year
and by the country codes present in the boundary file. It preserves the source
estimates and missing values; consumption-based estimates are available for
115 of these countries.

| Column | Meaning | Unit |
| --- | --- | --- |
| `country` | Country name in the emissions source | Text |
| `iso_code` | Three-letter country identifier | Text |
| `year` | Year of observation; 2023 throughout | Year |
| `population` | Population used for per-person measures | People |
| `co2` | Annual territorial CO2 emissions | Million tonnes of CO2 |
| `co2_per_capita` | Annual territorial CO2 emissions divided by population | Tonnes of CO2 per person |
| `consumption_co2` | Annual consumption-based CO2 emissions | Million tonnes of CO2 |
| `consumption_co2_per_capita` | Annual consumption-based CO2 emissions divided by population | Tonnes of CO2 per person |

Territorial emissions count CO2 emitted within a country's borders.
Consumption-based emissions adjust territorial emissions by adding emissions
embedded in imports and subtracting emissions embedded in exports. Both measures
cover fossil fuels and industrial processes and exclude land-use change.
They measure CO2, not all greenhouse gases. Missing entries are unavailable
estimates, not zeros.

OWID-produced data are available under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
Underlying third-party data retain their source terms; see the source column of
the pinned codebook and [OWID's licence statement](https://github.com/owid/co2-data#license).
Credit Our World in Data and the Global Carbon Budget when using the emissions data.

## Boundaries: `countries.geojson`

Source: [Natural Earth](https://www.naturalearthdata.com/), 1:110m country boundaries,
version [5.1.2](https://github.com/nvkelso/natural-earth-vector/blob/v5.1.2/geojson/ne_110m_admin_0_countries.geojson).
The data are [public domain](https://www.naturalearthdata.com/about/terms-of-use/).

The file has 176 features and three columns: `iso_code`, `map_name` and `geometry`.
Coordinates use WGS84 longitude and latitude (EPSG:4326).

Course preparation retains the source geometries, omits Antarctica and renames
`ISO_A3_EH` and `ADMIN` to `iso_code` and `map_name`. Three features without an ISO
code use local identifiers `NE_CYN`, `NE_KOS` and `NE_SOL`; these are not official
ISO codes. Those features and ATF, ESH, FLK and PRI have no matching row in the
emissions extract. The boundaries are simplified, omit some small territories
and follow Natural Earth's conventions for disputed areas.

These files were prepared by `scripts/fetch_data.py` in the course repository.
No emissions, per-person values or geometries were recalculated for this homework.
