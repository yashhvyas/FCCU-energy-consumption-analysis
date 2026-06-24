# FCCU Energy Consumption Analysis

Practice project analyzing energy consumption (steam, power, fuel gas) across FCCU plant equipment. Raw data → cleaning → analysis → visualization.

**Status: Dataset upgrade in progress.** Initial analysis was done on a self-generated practice dataset to learn the full data analytics pipeline. Now replacing it with a real plant-knowledge-based dataset for accurate, meaningful analysis.

## What This Project Covers

- 6 months of daily energy consumption readings (Jan - Jun 2025)
- 9 FCCU equipment units: Reactor, Regenerator, Air Blower, CO Boiler, Wet Gas Compressor, etc.
- 3 energy types: Steam, Power (Electrical), Fuel Gas
- Columns: `Date`, `Plant_Area`, `Equipment_Name`, `Energy_Type`, `Consumption`, `Unit`, `Shift`, `Remarks`

## Project Progress

### Phase 1 — Learning Pipeline (Completed)

Built and ran the full data analytics pipeline on a self-generated practice dataset:

- Explored raw data using `shape`, `info()`, `describe()`, `isnull().sum()`, `unique()`
- Cleaned mixed date formats, inconsistent casing/spacing, duplicate category labels
- Handled missing values and outlier readings (negative/zero consumption)
- Imputed missing values using per-equipment average
- Removed duplicate rows
- Ran groupby analysis — equipment-wise, energy-type-wise, monthly trend, shift comparison
- Built 4 visualizations using Matplotlib

### Phase 2 — Real Data (In Progress)

During analysis review, identified that energy type assignments in the practice dataset didn't match actual FCCU plant setup — for example, Wet Gas Compressor runs on a steam turbine drive, not electrical power. This kind of error significantly skews analysis results.

Upgrading to a real plant-knowledge-based dataset with correct energy types and realistic consumption ranges based on actual field experience. Full analysis and visualizations will be re-run on this corrected data.

This is a good example of why domain knowledge matters in data analytics — the numbers alone wouldn't catch this kind of error.

## Tools

Python, Pandas, NumPy, Matplotlib

