# FCCU Energy Consumption - Raw Data

This is raw data I'm using for a data analytics practice project, based on energy consumption (steam, power, fuel gas) in an FCCU plant setup.

## About the data

- 6 months of daily readings (Jan 2025 - Jun 2025)
- Covers 9 equipment units like Reactor, Regenerator, Air Blower, CO Boiler, Wet Gas Compressor etc.
- Columns: Date, Plant_Area, Equipment_Name, Energy_Type, Consumption, Unit, Shift, Remarks

## Current status

This is the **raw, unprocessed** version of the data. I've started exploring it using pandas (`head()`, `info()`, `describe()`, checking nulls and unique values).

While exploring, I found a bunch of issues that real-world data usually has:
- Dates written in different formats
- Equipment names with inconsistent spelling/casing
- Same unit written in different ways (e.g. Ton, ton, Tons)
- Some missing values
- A few outlier/odd readings
- Some duplicate rows

## What's next

Next step is cleaning this data and standardizing everything, then moving on to actual analysis (which equipment consumes the most energy, any trends over time, etc.)

This repo will be updated as I progress through the project.
