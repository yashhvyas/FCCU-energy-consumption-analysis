# FCCU Energy Consumption Analysis

Practice project analyzing energy consumption (steam, power, fuel gas) across FCCU plant equipment. Raw data → cleaning → analysis → visualization.

**Status: Real dataset collection in progress.** Practice pipeline is fully complete. Now collecting actual equipment-wise energy consumption data from plant knowledge to rebuild the dataset accurately before final analysis.

## What This Project Covers

- 6 months of daily energy consumption readings (Jan - Jun 2025)
- 9 FCCU equipment units: Reactor, Regenerator, Air Blower, CO Boiler, Wet Gas Compressor, Feed Preheater, Flue Gas Cooler, Slurry Pump, Main Fractionator
- 3 energy types: Steam, Power (Electrical), Fuel Gas
- Columns: `Date`, `Plant_Area`, `Equipment_Name`, `Energy_Type`, `Consumption`, `Unit`, `Shift`, `Remarks`

## Project Progress

### Phase 1 — Learning Pipeline (Completed)

Built and ran the full data analytics pipeline end to end on a practice dataset:

- Explored raw data — shape, dtypes, nulls, unique values, descriptive stats
- Cleaned mixed date formats, inconsistent casing/spacing, duplicate category labels
- Handled missing values and bad sensor readings (negative/zero consumption)
- Imputed missing values using per-equipment average
- Removed duplicate rows
- Ran groupby analysis — equipment-wise, energy-type-wise, monthly trend, shift-wise comparison
- Built 4 visualizations using Matplotlib (bar charts + line chart)

### Phase 2 — Real Data Collection (In Progress)

During analysis review, identified that energy type assignments in the practice dataset did not match actual FCCU plant setup. For example, the Wet Gas Compressor runs on a steam turbine drive — not electrical power. This kind of domain error significantly affects analysis results and conclusions.

Currently collecting accurate equipment-wise energy type and daily consumption data based on actual field experience. Dataset will be rebuilt and full analysis re-run once this is confirmed.

This is a good example of why domain knowledge matters in data analytics — the numbers alone would not have caught this error.

### Phase 3 — Final Analysis & Visualization (Planned)

Once real dataset is ready:
- Re-run full cleaning pipeline
- Re-run all groupby analysis
- Regenerate all 4 charts
- Add summary of key findings

## Tools

Python, Pandas, NumPy, Matplotlib

