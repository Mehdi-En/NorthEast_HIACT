# Northeast_HIACT

Selected public source data, derived summaries and fictional examples for regional hydrogen research in North East England and the Humber.

## Data catalogue

| File | Contents | Data kind |
| --- | --- | --- |
| [Original DESNZ workbook](data/raw/Subnational_total_final_consumption_2005_2024.xlsx) | UK energy consumption, 2005–2024, by geography, sector and fuel | Original published statistics |
| [Study geography](data/derived/study_geography.csv) | 12 North East and 4 Humber local authorities | Author-defined geographic membership |
| [Local authority energy](data/derived/local_authority_energy_2005_2024.csv) | 1,280 records: 16 authorities × 20 years × 4 all-fuel measures | Published values extracted and converted to GWh |
| [Study area energy](data/derived/study_area_energy_2005_2024.csv) | 160 records: 2 areas × 20 years × 4 measures | Sums over the listed authorities |
| [2024 fuel totals](data/derived/local_authority_fuel_totals_2024.csv) | 96 records: 16 authorities × 6 fuel groups, all sectors | Published values extracted and converted to GWh |
| [Illustrative process parameters](data/synthetic/illustrative_process_parameters.csv) | 23 parameter records for 8 fictional cases | Synthetic educational examples |

## Start here

Read [DATA_USE.md](DATA_USE.md) for interpretation and [SYNTHESIS.md](SYNTHESIS.md) for exact extraction and aggregation steps. The original workbook's Cover sheet and Notes remain authoritative for the published statistics. The CSV summaries are flat UTF-8 tables with one header row. `metadata/dataset_inventory.csv` records their origins and `metadata/derived_data_dictionary.csv` defines each field. File hashes and validation results are supplied in `metadata/`.

“Derived” means selected, converted or aggregated public statistics. “Synthetic” means fictional illustrative parameters. Neither label represents a future hydrogen-demand estimate. The annual industrial/commercial measure includes other sectors and must not be described as industrial process heat alone.

## Scope

The collection supports independent exploration of historical energy use and understanding of possible process-data structures. It excludes the paper's constructed sector allocations, calibrated inputs, actual site parameter sets, adoption trajectories, models, code, partner outputs and analytical results. It cannot reproduce the paper's numerical findings. The downloaded DESNZ edition has not been reconciled against the paper's frozen inputs.

The fictional examples use arbitrary example scales and scenario labels. They are not observations, forecasts, validated engineering designs or evidence about named sites. No probabilities or random draws are implied.

## Source and reuse

The original workbook was published by DESNZ on 30 July 2026 and retrieved on 20 October 2026. [Original publication](https://www.gov.uk/government/statistics/total-final-energy-consumption-at-regional-and-local-authority-level-2005-to-2024).

Contains public sector information licensed under the [Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/). Retain DESNZ attribution for the workbook and its derivatives. See [DATA_LICENCE.md](DATA_LICENCE.md) for the separate terms for author-created material.

Updated 20 October 2026. No DOI or archived release has been assigned. This is a selected supporting-data collection, not a complete replication archive.
