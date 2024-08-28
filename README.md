# Project Name
> BoomBikes, a leading bike-sharing service in the U.S., has faced significant challenges due to the COVID-19 pandemic, resulting in a steep decline in revenues. As restrictions are expected to lift, BoomBikes is proactively planning to meet the potential surge in demand for bike-sharing services. This project focuses on analyzing factors that influence bike demand and aims to provide insights for optimizing the company's operations in a post-pandemic world.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- BoomBikes faces the challenge of predicting customer demand in an uncertain post-COVID-19 environment. The company needs to identify the key variables that influence bike rentals, such as weather conditions, seasonal trends, and holidays, to optimize their operations and maximize revenue. By understanding these factors, BoomBikes can make data-driven decisions, such as adjusting bike availability, pricing strategies, and marketing efforts, to better cater to customer needs and stand out from competitors in a recovering market.
- The global COVID-19 pandemic has had a profound impact on various industries, including the bike-sharing sector. BoomBikes, a prominent bike-sharing service provider in the United States, has experienced a significant downturn in revenue due to the lockdowns and restrictions imposed during the pandemic. As the situation gradually improves and the economy begins to recover, BoomBikes is keen to understand the factors that will drive the demand for bike-sharing services in a post-pandemic world. This project aims to analyze these factors to help the company adapt to the changing market conditions and strategically plan for future growth.
- BoomBikes wants to understand the key factors affecting the demand for shared bikes in the American market. The goal is to identify which variables are significant in predicting bike demand and how effectively these variables explain the variations in demand. This understanding will help BoomBikes in making informed decisions to capture market share and boost revenues as the economy recovers.
- Dataset Used
=========================================	
day.csv have the following fields:
	
	- instant: record index
	- dteday : date
	- season : season (1:spring, 2:summer, 3:fall, 4:winter)
	- yr : year (0: 2018, 1:2019)
	- mnth : month ( 1 to 12)
	- holiday : weather day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
	- weekday : day of the week
	- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
	+ weathersit : 
		- 1: Clear, Few clouds, Partly cloudy, Partly cloudy
		- 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
		- 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
		- 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
	- temp : temperature in Celsius
	- atemp: feeling temperature in Celsius
	- hum: humidity
	- windspeed: wind speed
	- casual: count of casual users
	- registered: count of registered users
	- cnt: count of total rental bikes including both casual and registered

## Conclusions
Positive Contributors to Bike Demand:
    1. Temperature (temp):
            - Coefficient: +0.5610
            - Inference: Temperature is the most significant positive contributor to bike demand. As the temperature increases, the number of bike rentals rises, indicating that warmer weather encourages more people to use bikes.
    2. Year (yr):
            - Coefficient: +0.2282
            - Inference: The positive coefficient for the year suggests that there is an increasing trend in bike demand over time, potentially due to growing awareness and adoption of bike-sharing services.
    3. Winter Season (season_winter):
            - Coefficient: +0.1227
            - Inference: Surprisingly, the winter season also shows a positive impact on bike demand, which may indicate that, in some areas, bike rentals remain consistent even in colder months, possibly due to less extreme winter conditions or increased indoor biking options.
    4. September (mnth_sept):
            - Coefficient: +0.1123
            - Inference: September shows a significant positive impact on bike demand, likely due to favorable weather conditions and the return of people to regular routines after the summer holidays.
    5. Saturday (weekday_sat):
            - Coefficient: +0.0559
            - Inference: The positive coefficient for Saturday indicates higher bike rentals on weekends, reflecting leisure activities or family outings.
    6. October (mnth_oct):
            - Coefficient: +0.0644
            - Inference: October also contributes positively to bike demand, possibly due to moderate weather conditions ideal for outdoor activities.
    7. Summer Season (season_summer):
            - Coefficient: +0.0857
            - Inference: The summer season, typically associated with higher outdoor activity, positively impacts bike rentals.
    8. Working Day (workingday):
            - Coefficient: +0.0442
            - Inference: There is a slight positive effect of working days on bike demand, possibly indicating usage for commuting purposes.

Negative Contributors to Bike Demand:
	1.  Humidity (hum):
			- Coefficient: -0.1543
			- Inference: High humidity negatively affects bike demand, as uncomfortable weather conditions discourage people from using bikes.
	2.  Windspeed (windspeed):
			- Coefficient: -0.1079
			- Inference: Higher wind speeds reduce bike rentals, likely due to the difficulty and discomfort associated with biking in windy conditions.
	3. 	Bad Weather (weathersit_bad):
			- Coefficient: -0.2173
			- Inference: Bad weather conditions significantly decrease bike demand, as adverse weather such as heavy rain or snow deters outdoor activities.
	4.	Moderate Weather (weathersit_moderate):
			- Coefficient: -0.0474
			- Inference: Even moderate weather conditions have a slight negative impact on bike demand, though to a lesser extent than bad weather.
	5. 	Holiday (holiday):
			- Coefficient: -0.0948
			- Inference: Holidays show a negative impact on bike demand, possibly due to people preferring other modes of transport or staying indoors.


## Technologies Used
- Python - 3.12
- seaborn - 0.12.2
- matplotlib - 3.8.0
- pandas -  2.1.4
- numpy -  1.26.4
- Scikit-Learn - version 1.5.1
- Statsmodels - verion 0.14.2

## Acknowledgements
- This project was done as part during the PG Program in ML and AI from IIIT - B, in association with Upgrad.



## Contact
Created by [@ramyap-learnspace] - feel free to contact me!
