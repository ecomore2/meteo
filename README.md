
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Meteorological data

<!-- badges: start -->

<!-- badges: end -->

Source: [TuTiempo.net](https://en.tutiempo.net), daily data.

Station: 489400 (VLVT) | Latitude: 17.95 | Longitude: 102.56 | Altitude:
171

[cleaning
pipeline](https://ecomore2.github.io/meteo/make_data.html)

[CSV](https://raw.githubusercontent.com/ecomore2/meteo/master/data/meteo.csv)

From
R:

``` r
if (! "readr" %in% rownames(installed.packages())) install.packages("readr")
pacs <- readr::read_csv("https://raw.githubusercontent.com/ecomore2/meteo/master/data/meteo.csv",
                        col_types = "Dddddidddddllll")
```

Dictionary:

  - **day**: date of data colletion
  - **ta**: average temperature (°C)
  - **tx**: maximum temperature (°C)
  - **tn**: minimum temperature (°C)
  - **slp**: atmospheric pressure at sea level (hPa)
  - **h**: average relative humidity (%)
  - **pp**: total rainfall and / or snowmelt (mm)
  - **vv**: average visibility (km)
  - **v**: average wind speed (km / h)
  - **vm**: maximum sustained wind speed (km / h)
  - **vg**: maximum speed of wind (km / h)
  - **ra**: boolean indicating whether there was rain or drizzle
  - **sn**: boolean indicating whether it snowed
  - **ts**: boolean indicating whether there were storm
  - **fg**: boolean indicating whether there was flood
