# Assessing the Effects of Climate Change in VA Reservoirs

![](path_to_related_image.gif)

A project focused on the application of Median-Based Linear Models (MBLM), using `mblm` package in R, to understand water surface temperature warming rates over time in reservoirs across the state of Virginia.

# Summary

The analysis uses long-term monitoring data from the Virginia Department of Environmental Quality to examine trends across 41 monitoring stations in reservoirs throughout the state of Virginia during the months of May-October. Median-based linear modelling is thought to be more robust to the presence of outlier data points than ordinary least squares linear regression.
Lake stations were selected that had at least 100 depth profiles recorded over the last 40+ years, with the earliest observations in the dataset coming from 1968.

After subsetting data for the 41 selected lake stations from the larger DEQ dataset, mean, minimum, maximum, and the number of observations for maximum temperature (`TMax`) are derived for each station-month (41 sites x 6 months = 246 station-months), aggregating across all available years.

A "temperature anomaly" field (`TAnomaly`) is derived by subtracting the long-term monthly average maximum temperature from each observed `TMax` value. To analyze trends over time, a MBLM for each station-month is fitted using the formula `TAnomaly ~ Year`. In the file `TempDO_climateChange_analysis.Rmd`, model slope (i.e., change in temperature (degrees C) per year) is used to create a series of data visualizations in an effort to identify potential causes of variability in lake warming rates.

## Files

This repository includes the following files and directories:

| File Name                          | Description                                       |
|------------------------------------|---------------------------------------------------|
| ecoregions_shp                     | shapefile of Virginia Level III ecoregions (source: EPA)|
| TempDO_climateChange_analysis.Rmd  | R Markdown file for data preparation in climate change analysis, includes fix for TAnomaly calculation.|
| TempDO_climateChange_viz.Rmd  | R Markdown file for data analysis and viz|
| VADEQ_stationInfo.csv              | VA DEQ (Department of Environmental Quality) station information |
| data_original.xlsx                 | source data|
| reservoir-temp-DO.Rproj            | R Project file |
| .gitignore                        |                                                                            |
