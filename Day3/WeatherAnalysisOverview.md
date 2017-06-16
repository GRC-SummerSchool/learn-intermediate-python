[< Previous (Git - Saving your work)](GitChanges.md) | [Day3](../README.md)| [Next (Functions: Temperature Conversion) >](TemperatureConversion.md) |
|----|----|----|

# Weather Analysis

## Overview

For this exercise, we will create a program that will do the following:

- Read in weather data from a CSV file.
- Perform analysis on the data.
- Display both data and results as visually appealing plots.

Along the way, we will leverage the python concepets you have learned so far and introduce some new ones:
- Functions for temperature conversion
- Importing modules for plotting charts
- Reading data from CSV files

## Weather Data

The weather data we will use for this exercise has been obtained
[NOAA's National Centers for Environmental Information](https://www.ncdc.noaa.gov/)

Our data file contains [divisional](https://www7.ncdc.noaa.gov/CDO/CDODivisionalSelect.jsp#) data for the state of New York from January 2001 through April 2017.

The CSV file contains the following columns with a header:

| Header|Description|
|-------|-----------|
|StateCode|State code|
|Division|Division or station code (1-10)|
|YearMonth|Year month timestamp e.g., 201001|
|PCP | Precipitation Index|
|TAVG | Temperature Index|
|TMIN | Minimum Temperature Index|
|TMAX | Maximum Temperature Index|
|PDSI | Palmer Drought Severity Index|
|PHDI | Palmer Hydrological Drought Index|
|ZNDX | Palmer Z-Index|
|PMDI | Modified Palmer Drought Severity Index|
|CDD | Cooling Degree Days|
|HDD | Heating Degree Days|
|SPnn | Standard Precipitation Index|

[< Previous (Git - Saving your work)](GitChanges.md) | [Day3](../README.md)| [Next (Functions: Temperature Conversion) >](TemperatureConversion.md) |
|----|----|----|