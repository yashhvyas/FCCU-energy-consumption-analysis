# FCCU Energy Consumption - Raw Data

This is raw data I'm using for a data analytics practice project, based on energy consumption (steam, power, fuel gas) in an FCCU plant setup.

## About the data

- 6 months of daily readings (Jan 2025 - Jun 2025)
- Covers 9 equipment units like Reactor, Regenerator, Air Blower, CO Boiler, Wet Gas Compressor etc.
- Columns: Date, Plant_Area, Equipment_Name, Energy_Type, Consumption, Unit, Shift, Remarks

## Current status

This is the raw, unprocessed version of the data. I've started exploring it using pandas (`head()`, `info()`, `describe()`, checking nulls and unique values).

While exploring, I found a bunch of issues that real-world data usually has:

- Dates written in different formats
- Equipment names with inconsistent spelling/casing
- Same unit written in different ways (e.g. Ton, ton, Tons)
- Some missing values
- A few outlier/odd readings
- Some duplicate rows

## Cleaning done so far

- Converted the Date column into a proper date format (it had mixed formats like `2025-01-05`, `25/01/2025`, `14-03-2025`)
- Cleaned up Equipment_Name, Energy_Type and Shift columns - fixed spacing and casing issues so the same equipment/shift wasn't being counted as different categories
- Fixed Shift labels (`A` and `A Shift` were meant to be the same thing)
- Caught a tricky one - after cleaning, `Fuel Gas` and `Fuelgas` were still showing up as two different categories because of how the original text was written. Fixed that too.
- Treated negative and zero consumption values as bad sensor readings, and filled them along with the actual missing values using the average consumption for that specific equipment (not the overall average, since each equipment has very different normal usage)
- Marked which rows had their values filled in (vs original readings) in the Remarks column, so that's still traceable
- Removed duplicate rows

## What's next

Next step is actual analysis - figuring out which equipment consumes the most energy, whether there's any month-wise trend, and comparing energy usage across shifts. Charts and visuals will follow after that.

This repo will be updated as I progress through the project.
