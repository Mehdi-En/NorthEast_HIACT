# How the supporting tables were assembled

## Geographic membership

`study_geography.csv` carries the 16 local authority codes, names and study-area assignments from the existing research geography register. Internal electricity-system region assignments and notes were omitted. It defines the study boundary; it is not an official DESNZ regional classification. North East comprises 12 authorities. Humber comprises Hull, East Riding of Yorkshire, North East Lincolnshire and North Lincolnshire. All 16 codes match records in every deposited year sheet.

## Historical energy tables

The sole numerical source is the original DESNZ workbook stored in `data/raw/`. Its year sheets use April 2025 local authority boundaries. These supporting summaries were assembled on 20 October 2026; they are separate from the paper's calibrated working datasets.

1. For each year 2005–2024, use the year-named worksheet. Headers are in row 6. Match column A (Code) to the geography list. Keep one record per authority. Published names come from column C and row notes from column D.
2. For `local_authority_energy_2005_2024.csv`, extract E (all fuels, domestic), F (transport), G (industrial, commercial and other) and H (total). Reshape into one record per authority, year and measure. Retain the sheet, cell and row-note references.
3. For `study_area_energy_2005_2024.csv`, sum each of those measures over the listed 12 or 4 authorities within each year. Exclude regional, national and unallocated rows. Do not sum the three component measures and the total together. These are study-boundary aggregates, not copied official regional totals.
4. For `local_authority_fuel_totals_2024.csv`, extract the 2024 totals in O (coal), R (manufactured fuels), Z (petroleum), AC (gas), AF (electricity) and AJ (bioenergy and wastes). These totals include all sectors, not industrial use alone.
5. Preserve the published numbers as `energy_ktoe`. Compute `energy_gwh = energy_ktoe × 11.63`, following the source workbook. No rounding is deliberately applied to the stored values. Floating-point representations may differ in their last decimal places.

No sector disaggregation, imputation, efficiency correction, emissions conversion, future interpolation or hydrogen substitution is applied. Missing or non-numeric selected energy cells cause validation failure rather than silently becoming zero. The source's Notes still apply to all extracts.

## Fictional process examples

The eight cases were adapted from existing project test fixtures: ammonia, direct-reduced iron, refinery feedstock, fuel switching, company replacement, hydrogen production, storage and power demand. They were already fictional; their values were retained without fitting them to named sites. Only the long-format examples were included. Wide-format variants were omitted to avoid mixing alternative representations.

The adaptation retains parameter names, values, units, energy basis, illustrative scenario/year and source-example filename. It renames `site` to `example_id`, adds `data_kind=fictional_example`, and removes internal model buses, geography, workflow status, approval fields and fixture paths. These removals prevent test-workflow labels from being mistaken for real evidence approval. `source_example` identifies an originating fixture name, not a file delivered in this repository.

The examples are independent descriptions, not a connected scenario or a complete parameterisation. For example, storage working capacity is a stock in MWh and production is an annual flow in MWh/year. Do not add those quantities. Sample intensities and loss factors must not be treated as recommended engineering assumptions. The example scenario label `central` has no connection to the paper's central scenario.

## Validation

All years contain exactly the 16 unique authority codes. The tables have 1,280 authority-measure records, 160 area-measure records and 96 fuel records. All selected values are finite and non-negative. For each 2024 authority, the six fuel totals reconcile to column H within 0.00001 ktoe. The maximum observed residual is recorded in `metadata/validation_summary.json`. The source workbook's SHA-256 is unchanged.

These checks establish extraction consistency. They do not validate the paper's model or the realism of fictional process parameters.
