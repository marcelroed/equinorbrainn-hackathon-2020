# Historical Weather Forecast Dataset description

File Name: weather_data_utc.csv

File URL: Released separately

## General notes
The dataset contains historical weather forecasts for the wind park, from TODO (obfuscate): 01.11.2017 to 30.11.2018. 

The forecasts are made for 4 geographical zones within the wind park (codes 'NE | 'NW | 'SE | 'SW'), as well as for the whole park (code 'WP')

The forecasts are issued each hour, for 156 hours in advance. Time resoultion for a forecast is 1 hour. Each forecast is represented by a time series with 156 data points.

The dataset contains a 156-hour forecast series for each hour/wind park zone in the mentioned period. 

All dates in the dataset are in UTC format.

## Description of Fields
| Field  | Description  |
|---|---|
| windpark_zone | Geographical zone for the forecast. One of 'NE | 'NW | 'SE | 'SW' or 'WP' |
| datetime_forecast_utc | Date and time at which the forecast series have been made |
| datetime_start_utc | Start timestamp of a forecast data point | 
| datetime_end_utc | End timestamp of a forecast data point | 
| SUB_WIND_SPEED_10 | Wind speed at 10m height, m/s |
| SUB_WIND_SPEED_40 | Wind speed at 40m height, m/s |
| SUB_WIND_SPEED_110 | Wind speed at 110m height, m/s | 
| SUB_WIND_GUST_10 | Wind gusts at 10m height, m/s | 
| SUB_WIND_GUST_40m| Wind speed at 40m height, m/s | 
| SUB_WIND_GUST_110m | Wind speed at 110m height, m/s |
| SUB_WIND_DIR_10 | Wind direction at 10m height, &deg; |
| SUB_WIND_DIR_40| Wind direction at 40m height, &deg; |
| SUB_WIND_DIR_110 | Wind direction at 110m height, &deg; | 
| SUB_AIR_TEMP_2 | Air temperature, &deg;C | 
| SUB_AIR_PRESSURE| Air pressure, hPa |
| SUB_AIR_HUMIDITY | Air humidity, % |
| SUB_WIND_CHILL_TEMP | Air temperature wind chill factor, &deg;C |
| SUB_WATER_TEMP| Water temperature, &deg;C |
| SUB_HOR_VISIBILITY | Horisontal visibility, m |
| SUB_CLOUD_COVER | Cloud cover, % |
| SUB_PRECIPITATION| Precipitation, mm |
| SUB_RISK_LIGHTENING | Risk of lightning, % |
| SUB_RISK_FOG| Risk of fog, % |
