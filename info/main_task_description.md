# Task description

You are an operator of a [wind farm](windfarm.md), and you find yourself on a certain date. You want to sell electrical energy on a spot market; to do that you need to provide expected production from your wind farm for 48 hours in advance, for each hour, starting at upcoming midnight.


You are provided with the following data sets:
- [Historical data set](historical_data.md) with actual production values, as well as some measurements;
- [Weather data set](weather_data.md), containing historical weather forecasts;
- [Running plan](running_plan.md), containing on/off and power limit schedule for today and next three days.

URLs for the data sets will be distributed via [Slack](https://equinorbrainn-hy21669.slack.com/).

Predictions should be made as precise as possible, since:
- In the case of overestimate (i.e. predicting more than actually producing), you will need to purchase additional energy to fulfill the commitment.
- In the case of underestimate (predicting less than actually producing), you will be forced to curtail the turbines, and therefore you would not be able to sell more than predicted. In addition, there would be a cost associated with curtailment.

After each round earnings will be calculated according to the actual and predicted production. Earnings will be then summarized and presented at the [scoreboard](https://equibrainhackahton2020.azurewebsites.net/scoreboard).

Note that overall production, as well as energy price, may change from round to round.

General information about wind farm can be found [here](windfarm.md)

# Delivery
## Requirements
You are required to deliver the following:
- CSV file with predictions, according to the specifications below. 
- Source code for prediction/description on how to reproduce prediction (Code files and/or notes in text, word or pdf)

## Delivery location

Prediction files: Upload your predictions [here](https://equibrainhackahton2020.azurewebsites.net). Choose "upload results" option.

Source code files: create a subfolder with your name and upload your code [here](https://equibrainhackahton2020.azurewebsites.net/sourcecode). 

## Specifications for the prediction file
Name: ```submission_<number_of_the_round>_<team-name>.csv.``` 

Example: ```submission_1_teamname.csv```

NB! Only one prediction will be considered. If you want to change your prediction within the timeline, replace your current file.

Content: semicolon-separated values, with header. Decimal separator: point; no thousand separators.

| Field name | Description |
|---|---|
| timestamp | UTC timestamp, in time-zone aware ISO format (YYYY-MM-DD hh:mm:ss+00:00), eg. 2020-02-29 00:00:00+00:00 |
| energy | Predicted Energy in KWh |

The file shall contain predictions for each hour, total 49 lines including header and 48 predictions. 

Example:
```
timestamp;energy
2020-02-29 00:00:00+00:00;70000
2020-02-29 01:00:00+00:00;10000
2020-02-29 02:00:00+00:00;100000
```
An example file can also be found [here](submission_1_teamname.csv)

## Specifications for the source code file
'txt', 'csv', 'py', 'zip', 'ipynb'

Name: ```sourcecode_<number_of_the_round>_<team-name>.<extension>.```

Example: ```sourcecode_1_teamname.zip```

## Deadline
Deadlines for each round are described [here](game_schedule.md)
