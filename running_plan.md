# Description of Running Plan dataset

File Name: running_plan.&lt;date>.&lt;uuid>.csv

File URL: Released separately

## General notes 
The dataset contians schedule for future turbine on/off periods and/or power limits.

## Description of Fields
| Field  | Type | Description  |
|---|---|---| 
| turbine | string  | ID of Turbine|
| timestamp | datetime | UTC schedule time |
| ActivePowerLimit | number | Planned Power Limit, KW. |
| StateRun | number | Planned On/Off state |

