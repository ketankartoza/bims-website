---
title: BIMS Documentation
summary: Central documentation site for BIMS projects
    - Tim Sutton
    - Helen Dallas
    - Jeremy Prior
date: 26-09-2023
some_url: https://github.com/kartoza/bims-website
copyright: Copyright 2023, Kartoza
contact: 
license: This program is free software; you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation; either version 3 of the License, or (at your option) any later version.
#context_id: 1234
---

# Water temperature time series dashboard

This dashboard includes some of the components in the biodiversity dashboards such as map, site photograph and overview, which provides geocontext data for the site, and metadata.  The water temperature data is shown for one year at a time, so the user need to first select the day, month and year for the start and end of the data series. Note: it is not possible to select data for longer than 1 year, and the start and end year need to be the same.

![Water Temperature 1](img/water-temperature-1.png)

A thermograph is provided for the site based on the one year of water temperature data time series specified. Sub-daily data are transformed into daily data and plotted as smoothed daily temperature means based on a seven-day moving average, and smoothed daily range using daily minima and maxima. For Reference thermograph the reference condition thermal envelope plus one and two standard deviations are shown. Further manipulation of the time series is possible using the All dropdown (view 1 month, 3 months, 6 months etc) and the graph may be downloaded in different formats.

![Water Temperature 2](img/water-temperature-2.png)

Tables of thermal metrics and monthly magnitudes (mean, minimum, maximum and range) are provided. The user is referred to Dallas and Rivers-Moore (2019, 2022) for more details. Thermal metrics describe an annual thermal regime using broad descriptive statistics, such as mean annual temperature, annual coefficient of variability, predictability and maximum daily range, as well as water temperature events in terms of their magnitude, frequency, duration of extreme events (Rivers-Moore et al. 2013).

**Water temperature dashboard – Part 1.**

![Water Temperature 3](img/water-temperature-3.png)

**Water temperature dashboard – Part 2.**

![Water Temperature 4](img/water-temperature-4.png)
