# NorthEast_HIACT: supporting data and public-data outputs

Public energy statistics, straightforward historical summaries, source references and fictional examples for North East England and the Humber.

## Data

| Collection | Contents |
| --- | --- |
| [DESNZ final energy consumption](data/raw/Subnational_total_final_consumption_2005_2024.xlsx) | Original published workbook for 2005–2024. |
| [DESNZ residual fuels](data/raw/RESP-D023_residual_fuel_2005_2023.xlsx) | Original published historical workbook for 2005–2023. |
| [2024 local-authority gas](data/source_extracts/RESP-D022_gas_2024_study_authorities.csv) | Public statistics selected for the 16 study authorities. Consumption fields are GWh. |
| [ONS boundary subset](data/geography/RESP-D024_study_LAD_December_2024.geojson) | The 16 local-authority polygons from the December 2024 product. |
| [Study geography](data/derived/study_geography.csv) | Names, codes and two study-area labels for those authorities. |
| [Historical authority summaries](data/derived/local_authority_energy_2005_2024.csv) | Public energy statistics reshaped for 2005–2024. |
| [Historical study-area summaries](data/derived/study_area_energy_2005_2024.csv) | Simple sums over the listed authorities. |
| [2024 all-sector fuel totals](data/derived/local_authority_fuel_totals_2024.csv) | Public fuel totals, not industry-only or hydrogen demand. |
| [Fictional examples](data/synthetic/illustrative_process_parameters.csv) | Eight clearly fictional cases illustrating parameter units and table structure. |

## Public-data output

[2024 energy summary](outputs/public_energy_summary_2024.csv) contains eight summary records derived solely from the deposited public DESNZ statistics. See [OUTPUTS.md](OUTPUTS.md). No model simulation is used to produce it.

## Source references

Publisher links and historical citation metadata are supplied for [Saltend](data/evidence/RESP-D034_source_links.csv), [Aldbrough Pathfinder](data/evidence/RESP-D035_source_links.csv), and [Humber Pipeline / Project Union](data/evidence/RESP-D036_source_links.csv). These are links, not mirrored documents or a current project-status assessment. Other public sources are listed in [metadata/public_sources.csv](metadata/public_sources.csv).

## Scope

This collection contains selected public source data, simple historical extracts and sums, and explicitly fictional teaching examples. It does not contain the paper's research-specific spatial allocations, site/bus mapping, substitution and adoption assumptions, calibrated inputs, model code, generated network, paper figures or analytical results. It cannot reproduce the paper.

Read [DATA_USE.md](DATA_USE.md), [SYNTHESIS.md](SYNTHESIS.md) and [DATA_LICENCE.md](DATA_LICENCE.md) for methods, units and reuse terms. File hashes and dictionaries are in `metadata/`. Updated 21 October 2026. No repository DOI or archived release has been assigned.
