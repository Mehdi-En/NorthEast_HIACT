# How to use the data

## Role in regional hydrogen research

Historical fuel consumption provides context for the scale and geography of regional energy use. It can inform the evidence base from which an industrial energy baseline is constructed. Translating that evidence into future hydrogen demand requires separate choices about eligible processes, efficiencies, adoption, named-site demand and overlap. Those choices and their numerical implementation are outside this repository.

The deposited workbook was retrieved from DESNZ on 20 October 2026. Its identity has not been reconciled against the paper's frozen working input files. Treat it as an independently usable public source edition, not a certified reconstruction of those inputs.

## Reading the workbook

- `Cover sheet`: publication details, scope, units, boundaries and revision information.
- `Notes`: qualifications referenced by numbered notes in the tables.
- `2005` through `2024`: annual tables; column headers are in row 6 and records start in row 7.
- Columns A–D identify geography and notes; E–AJ contain energy consumption measures.

Select North East and Yorkshire and The Humber records as appropriate for your own geographic question. Yorkshire and The Humber is broader than the Humber subregion. A regional total therefore must not be labelled a Humber-only total. The supplied `data/derived/study_geography.csv` defines the 16-authority study boundary used in the supporting CSV summaries.

## Units example

Energy figures are in thousands of tonnes of oil equivalent (ktoe). Following the workbook's conversion factor:

- GWh = ktoe × 11.63.
- TWh = ktoe × 0.01163.
- An illustrative 100 ktoe is 1,163 GWh, or 1.163 TWh.

This is a unit conversion, not a conversion of fuel demand into hydrogen demand. No paper result is represented by the illustrative value.

## Interpretation limits

Gas and electricity include an “Industrial, Commercial and other” grouping; this must not be treated as a pure industrial process-heat measurement. Coal and petroleum industrial categories also have specific coverage defined in the publisher's notes. National, regional, local authority and unallocated rows have different meanings. Keep them separate to avoid double counting.

Read the original Notes for missing or qualified entries; do not replace blanks or text markers with zero without justification. Annual revisions can change historical values. The April 2025 geography and release date matter when comparing with other editions.

## What users can do

Inspect historical fuel mix, compare regional trends, explore local authority energy consumption, and construct their own explicitly documented analyses. This repository supplies no future hydrogen scenario, site commissioning schedule, economic threshold or model implementation.

## Using the added summaries

Use the local authority series for comparisons over time, and the area series for the sum over each fixed study boundary. `all_fuels_total` includes domestic, transport and industrial/commercial/other use. The 2024 fuel table also covers all sectors. These measures cannot be substituted for industrial hydrogen demand. See `SYNTHESIS.md` for source columns and aggregation rules.

## Using fictional examples

Use `data/synthetic/illustrative_process_parameters.csv` to inspect how a process parameter can be recorded with a unit, time, pathway and energy basis. Every record is fictional. Source-example filenames indicate provenance from example fixtures, not external evidence. Several cases are intentionally incomplete and cannot be used to reconstruct a complete model.
