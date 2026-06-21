# FCCU Energy Consumption Analysis

Practice project analyzing energy consumption (steam, power, fuel gas) across FCCU plant equipment. Raw data → cleaning → analysis → visualization.

**Status: Work in progress.** Cleaning is complete, analysis is underway. This README will be updated as the project moves forward.

## Dataset

- 6 months of daily readings (Jan - Jun 2025)
- 9 equipment units: Reactor, Regenerator, Air Blower, CO Boiler, Wet Gas Compressor, etc.
- Columns: `Date`, `Plant_Area`, `Equipment_Name`, `Energy_Type`, `Consumption`, `Unit`, `Shift`, `Remarks`

## Data Quality Issues Found

- Date column with mixed formats (`2025-01-05`, `25/01/2025`, `14-03-2025`)
- Inconsistent spelling/casing in Equipment_Name and Energy_Type
- Same unit written differently (`Ton`, `ton`, `Tons`)
- Missing values and outlier readings (negative/zero consumption)
- Duplicate rows

## Cleaning Steps

- Standardized Date column to a single format
- Fixed casing/spacing in Equipment_Name, Energy_Type, Shift
- Merged duplicate category labels (e.g. `A` / `A Shift`, `Fuel Gas` / `Fuelgas`)
- Treated negative/zero consumption as bad sensor readings, imputed using per-equipment average (not overall average, since usage ranges differ significantly across equipment)
- Flagged imputed rows in Remarks for traceability
- Removed duplicate rows

## Analysis

Completed:
- Total and average consumption by equipment
- Total consumption by energy type

In progress:
- Month-wise consumption trends
- Shift-wise comparison

## Planned

- Visualizations (matplotlib)
- Summary of key findings

## Tools

Python, Pandas, NumPy, Matplotlib
