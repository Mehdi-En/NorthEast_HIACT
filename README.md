# Northeast_HIACT

Selected public source data and usage documentation for regional hydrogen research in North East England and Yorkshire and the Humber.

## What is included

The original DESNZ **Subnational total final energy consumption, 2005–2024** workbook, released 30 July 2026. It contains national, regional and local authority energy consumption by fuel and sector. The publisher's workbook is preserved unchanged, including its Cover sheet and Notes.

This is a selected source-evidence collection. It excludes the research project's constructed demand datasets, site assumptions, adoption trajectories, model files, code, partner outputs and paper results. It cannot reproduce the paper's numerical findings. Inclusion here does not certify that this downloaded edition exactly matches the frozen inputs used in the paper.

## Start here

1. Open `data/raw/Subnational_total_final_consumption_2005_2024.xlsx` and read **Cover sheet** and **Notes**.
2. Select a year sheet (2005–2024). The workbook uses April 2025 local authority boundaries.
3. Identify regional or local authority records using their codes and names. Do not add a region total to its constituent local authorities.
4. Consult `DATA_USE.md` for interpretation, limitations and a worked units example.
5. Use `metadata/dataset_inventory.csv`, `metadata/data_dictionary.csv` and `metadata/checksums.sha256` for provenance and verification.

The dataset supports independent exploration of historical energy consumption. It does not directly measure hydrogen demand or establish future site conversion.

## Source and reuse

Source: Department for Energy Security and Net Zero, [original publication](https://www.gov.uk/government/statistics/total-final-energy-consumption-at-regional-and-local-authority-level-2005-to-2024).

Contains public sector information licensed under the [Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/). Retain the publisher attribution when reusing the data. See `DATA_LICENCE.md`.

## Availability

Prepared 20 October 2026. No archived release or DOI has yet been assigned. Repository documentation is separate from the paper's data-availability statement; this collection should be described as selected source data rather than a replication archive.
