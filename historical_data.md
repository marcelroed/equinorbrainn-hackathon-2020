# Historical Wind Farm Data description

File Name: train.&lt;date>.&lt;uuid>.csv

File URL: Released separately

## General notes 
The dataset contians historical readings for some sensors for each turbine from the [wind farm](windfarm.md). Readings are aggregated for each hour, with 4 aggregate functions: Average, Min, Max, End, where "End" means the last value in the aggregation period.

Note that the data set may contain missing data, as "Null" values, as well as completely missing time intervals.

Most of the sensors produce continuous stream of data, but some are discrete, producing values from time to time. For such sensors, value is considered unchanged until the next real reading arrives.

Note that the dataset contains sensor data for __Power__ ( P ) for __each turbine__, measured in KW (Kilowatts), while you will have to predict __Energy__ ( E ), measured in KWh (Kilowatt-hours), for the __whole park__. In a time period with constant power, Energy can be calculated by the formula:

E = P * t, 
where P is Power in KW, t is time in hours. 

One should summarize  all turbines to get the overall energy.

All dates in the dataset are in UTC format.


## Description of Fields
| Field  | Type |Aggregates | Description  |
|---|---|---|---| 
| turbine | string | | ID of Turbine |
| timestamp | datetime | |UTC time for sensor reading |
| ActivePower | number | Average, Min, Max, End | Measured Active Power, KW |
| ActivePowerLimit | number | Field without aggregate suffix is most relevant.  Average, Min, Max, End aggregates are added for reference. End is forward filled, other aggregates are discrete| Power Limit, KW. |
| WindDirection | number | Average, Min, Max, End | Measured wind direction, &deg; |
| AmbientTemp | number | Average, Min, Max, End | Measured outside temperature, &deg;C|
| BladeAngleA | number | Average, Min, Max, End | Pitch angle for blade A, &deg; |
| BladeAngleB | number | Average, Min, Max, End | Pitch angle for blade B, &deg; |
| BladeAngleC | number | Average, Min, Max, End | Pitch angle for blade C, &deg; |
| BladeAngleRef | number | Average, Min, Max, End | Reference pitch angle, &deg;|
| NacelleDirection | number | Average, Min, Max, End | Nacelle direction, &deg; |
| ReactivePower | number | Average, Min, Max, End | Reactive Power, VAR  |
| StateRun | number | Field without aggregate suffix is most relevant.  Average, Min, Max, End aggregates are added for reference. End is forward filled, others aggregates are discrete. | On/Off (0/1) state of the turbine. NB! Can be fractional in the periods with several readings.|
| WindSpeed | number | Average, Min, Max, End | Measured wind speed, m/s |
