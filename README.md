# python-api-challenge

This repository contains my solution of thePython API Homework - What's the Weather Like? which was processed in 2 parts using jupyter notebook:
[Part I- WeatherPy](https://github.com/NazihZaz/python-api-challenge/blob/main/WeatherPy/WeatherPy.ipynb)
[Part II - VacationPy](https://github.com/NazihZaz/python-api-challenge/blob/main/VacationPy/VacationPy.ipynb)

## The three observable trends  that can be made from the this analysis are:

1. The closer the city is from the equator the higher the temperature is and per consequence the farther the city is from the equator the lower the temperature is. This is mainly because of the angle of influence of solar rays and the round form of the earth.
2. The city latitude impact mostly the temperature and not much of the other parameters we have analyzed such as cloudiness, humidity or wind speed. Other factors may have influence and some of the parameters we analyzed like "Season vs. Wind Speed" as usually spring tends to be the windiest season of the year, but further analysis needs to be conducted to confirm this theory.
3. There is no visible association between latitude and humidity, however, looking at the heatmap from Part II - VacationPy, we can notice that humidty level tends to be higher in coastal cities. Further analysis needs to be conducted to confirm this theory.

# Outputs generated:

[cities.csv](https://github.com/NazihZaz/python-api-challenge/blob/main/output_data/cities.csv)

![Latitude_vs_Cloudiness.png](https://github.com/NazihZaz/python-api-challenge/blob/main/Images/Latitude_vs_Cloudiness.png)

![Latitude_vs_Humidity.png](https://github.com/NazihZaz/python-api-challenge/blob/main/Images/Latitude_vs_Humidity.png)

![Latitude_vs_Temperature.png](https://github.com/NazihZaz/python-api-challenge/blob/main/Images/Latitude_vs_Temperature.png)

![Latitude_vs_Wind_Speed.png](https://github.com/NazihZaz/python-api-challenge/blob/main/Images/Latitude_vs_Wind_Speed.png)

![heatmap.png](https://github.com/NazihZaz/python-api-challenge/blob/main/Images/heatmap.png)

![hotel_map.png](https://github.com/NazihZaz/python-api-challenge/blob/main/Images/hotel_map.png)

## Background

Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. So let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

Now, we know what you may be thinking: "Duh. It gets hotter..."

But, if pressed, how would you prove it?

## Part I - WeatherPy
Creation of a [python script](https://github.com/NazihZaz/python-api-challenge/blob/main/WeatherPy/WeatherPy.ipynb) to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, I used a simple Python library, the OpenWeatherMap API, and a little common sense to create a representative model of weather across world cities.

The first requirement was to create a series of scatter plots to showcase the following relationships:

- Temperature (F) vs. Latitude
- Humidity (%) vs. Latitude
- Cloudiness (%) vs. Latitude
- Wind Speed (mph) vs. Latitude

After each plot, I added a sentence or two explaining what the code is analyzing.

The second requirement was to run linear regression on each relationship. This time, I separated the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

- Northern Hemisphere - Temperature (F) vs. Latitude
- Southern Hemisphere - Temperature (F) vs. Latitude
- Northern Hemisphere - Humidity (%) vs. Latitude
- Southern Hemisphere - Humidity (%) vs. Latitude
- Northern Hemisphere - Cloudiness (%) vs. Latitude
- Southern Hemisphere - Cloudiness (%) vs. Latitude
- Northern Hemisphere - Wind Speed (mph) vs. Latitude
- Southern Hemisphere - Wind Speed (mph) vs. Latitude

After each pair of plots, I explained what the linear regression is modeling. 

The final notebook:
- Randomly selected at least 500 unique (non-repeat) cities based on latitude and longitude.
- Performed a weather check on each of the cities using a series of successive API calls.
- Included a print log of each city as it was being processed with the city number and city name.
- Saved a CSV of all retrieved data and a PNG image for each scatter plot.


## Part II - VacationPy
Used jupyter-gmaps and the Google Places API for this part of the assignment. [Click here to be redirected to the jupyter notebook](https://github.com/NazihZaz/python-api-challenge/blob/main/VacationPy/VacationPy.ipynb)

To complete this part of the assignment,I needed to do the following:

- Create a heat map that displays the humidity for every city from Part I.

![heatmap.png](https://github.com/NazihZaz/python-api-challenge/blob/main/Images/heatmap.png)

- Narrowed down the DataFrame to find my ideal weather condition. For example:
	+ A max temperature lower than 80 degrees but higher than 70.
	+ Wind speed less than 10 mph.
	+ Zero cloudiness.
	+ Dropped any rows that don't contain all three conditions. I wanted to be sure the weather is ideal.

- Using Google Places API to I found the first hotel for each city located within 5000 meters of my coordinates.

- Plotted the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.

![hotel_map.png](https://github.com/NazihZaz/python-api-challenge/blob/main/Images/hotel_map.png)

[Homework Assignment details](https://gt.bootcampcontent.com/GT-Coding-Boot-Camp/gt-virt-atl-data-pt-09-2021-u-c/-/tree/master/02-Homework/06-Python-APIs/Instructions#part-i-weatherpy)