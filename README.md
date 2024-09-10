# Assessing the Effects of Climate Change in VA Reservoirs

<p align="center">
  <img src="img/publication_images/reservoirAnalysis_publicationPlot.jpg" width="233">
  <img src="img/publication_images/resevoirAnalysis_publicationMap.jpg" width="300">
</p>


A project focused on the application of Median-Based Linear Models (MBLM), using `mblm` package in R, to assess trends in water temperature and dissolved oxygen levels over time in reservoirs across the state of Virginia. The work was completed in collaboration with [Dr. Paul Bukaveckas](https://blogs.vcu.edu/pabukaveckas/) of VCU's Center for Environmental Sudies.

# Summary

The study focused on reservoirs in Virginia. Monitoring data were provided by the Virginia Department of Environmental Quality (DEQ). 

The dataset contained approximately 182,000 individual measurements of temperature and DO from over 500 lake stations, from the 1970s to the 2023. For this analysis, 41 stations were selected based on the availability of at least 100 profile dates between May and October. These stations included shallow sites (less than 3 meters in depth) and deep sites, and provided a total of 6,184 profiles. The data span approximately 40 years, with some stations monitored as early as the 1970s.

Trend Analysis

Station-specific trends were derived on a monthly basis (May-October) for temperature and DO, considering surface, bottom, mean, and range values. Temperature values were converted to anomalies by subtracting the long-term monthly average from observed values. Trends were then analyzed using the `mblm` package to derive Thiel-Sen slopes. MBLM being less sensitive to outliers than ordinary least squares. This approach allowed for the identification of long-term trends in temperature and DO.

Additionally, monthly average air temperature data from 1970 to 2021 were retrieved from NOAA’s National Centers for Environmental Information. These data was analyzed for four climate regions within Virginia that encompass most of the reservoirs in the analysis. Air temperature trends were derived using the same methods as for the water temperature data, allowing for the examination of correlations between atmospheric and reservoir trends.


