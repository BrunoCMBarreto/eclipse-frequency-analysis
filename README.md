# NASA Solar Eclipse Frequency Analysis

## Purpose

This repository contains a brief analysis into the distribution and frequency of solar eclipses around the world, with a focus on identifying the ideal place for passively viewing solar eclipses.

In particular, this analysis aims to determine if any trends exist in eclipse frequency by region or by eclipse type, and from this, determine which location most frequently has _visible_ solar eclipses when considering both historical eclipse data and historical cloud cover data.  

The purpose of this analysis is to identify optimal geographic locations for viewing solar eclipses based on historical data of eclipse frequency and weather conditions. Specifically, the analysis aims to:

## Data Sources

The solar eclipse data used in this notebook's analysis comes from [the NASA Eclipse dataset on Kaggle](https://www.kaggle.com/datasets/nasa/solar-eclipses/data). This data is included in this repository's data folder for convenience.

The weather data used in this notebook's analysis comes from [the Meteostat Global Daily Weather dataset on Kaggle](https://www.kaggle.com/datasets/guillemservera/global-daily-climate-data). Due to its size, the bulk of this dataset is not included in this repository.

Both datasets are also available directly from their sources at NASA and Meteostat respectively.

## Methods

The analysis within this repository is performed in four parts.

1. Frequency of Solar Eclipses
* Analyzed the number of solar eclipses (total, annular, partial, hybrid) across latitudes and longitudes.
* Visualized the spread of different eclipse types with line plots showing their distribution by latitude.
* Compared the proportion of total eclipses to all eclipse types at each latitude.
2. Cloud Cover and Sunshine Analysis
* Used daily sunshine minutes from the weather dataset as a proxy for cloud cover.
* Calculated low-visibility minutes (1440 - sunshine minutes per day).
* Created heatmaps to visualize the distribution of:
* Sunshine minutes (clear sky potential).
* Low-visibility minutes (cloud cover intensity).
3. Regional Grouping and Statistical Testing
* Rounded latitude and longitude to group eclipses into larger geographic bins.
* Performed ANOVA tests to assess variation in eclipse counts:
* Across latitudes (significant variation found).
* Across longitudes (no significant variation found).
4. Eclipse Viewing Optimization
* Combined eclipse frequency with cloud cover data to calculate the eclipse viewing ratio (total eclipses per daily low-visibility minutes).
* Generated heatmaps to identify regions with the highest viewing potential.
* Highlighted top geographic locations with optimal viewing conditions based on this ratio.
* These methods integrated weather and astronomical data to assess and optimize solar eclipse visibility by location.

## Findings

Ultimately, this analysis concluded that total, annular, and hybrid eclipses are most common at 0 latitude and become progressively less common, following a logarithmic decay curve, as latitude devites from 0. By contrast, partial eclipses are staggeringly more common from 60 to 70 degrees latitude and from -60 to -70 degrees latitude, due to the angle that the sun and moon must have with a given region on the Earth to result in a partial eclipse in that area.

From these frequencies and the data of regional cloud cover, it was concluded that western Somalia at a Latitude of 3 degrees and a Longitude of 42 degrees had the highest incidence of visible total solar eclipses.
