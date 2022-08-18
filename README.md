# weather-api-data-analysis-viz

## Background
The goal of this project is to utilize Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?" We already have a sense that temperature will have a tendency to increase, but how can we use data to prove this or gather additional insights alongside this?

### Part 1: WeatherPy

In this section, I created a Python script to visualize the weather of 500+ cities of varying distance from the equator. To do so, I used a simple Python library, the OpenWeatherMap API, to create a representative model of weather across cities.
The first thing to do was to create a series of scatter plots to showcase the following relationships as areas of interest:

    Temperature (F) vs. Latitude
    Humidity (%) vs. Latitude
    Cloudiness (%) vs. Latitude
    Wind Speed (mph) vs. Latitude
<img width="423" alt="Screen Shot 2022-08-17 at 8 42 32 PM" src="https://user-images.githubusercontent.com/91276925/185267814-03efc850-b6d7-4a86-86d9-126d434ec09f.png">

After each plot, added a sentence or two explaining what the code is analyzing.
The second thing to do was to compute the linear regression for each relationship to determine potential correlation. I separated the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

    Northern Hemisphere - Temperature (F) vs. Latitude
    Southern Hemisphere - Temperature (F) vs. Latitude
    Northern Hemisphere - Humidity (%) vs. Latitude
    Southern Hemisphere - Humidity (%) vs. Latitude
    Northern Hemisphere - Cloudiness (%) vs. Latitude
    Southern Hemisphere - Cloudiness (%) vs. Latitude
    Northern Hemisphere - Wind Speed (mph) vs. Latitude
    Southern Hemisphere - Wind Speed (mph) vs. Latitude
<img width="423" alt="Screen Shot 2022-08-17 at 8 42 57 PM" src="https://user-images.githubusercontent.com/91276925/185267836-b778e463-0c38-44c9-92a6-0aaa8bf6db36.png">

After each pair of plots, explained what the linear regression is modeling. For example, described any relationships that I noticed and any other findings.

#### Deliverables
Notebook that includes:

  - Randomly selected at least 500 unique (non-repeated) cities based on latitude and longitude.
  - Performed a weather check on each of the cities using a series of successive API calls.
  - Included a print log of each city as it's being processed, with the city number and city name.
  - Saved a CSV of all retrieved data and a PNG image for each scatter plot.

### Part 2: VacationPy

In this Section, I used Jupyter-gmaps and the Google Places API in order to create a heat map that displays the humidity for every city from Part 1. I then narrowed down the DataFrame to find your ideal weather condition. 
![image](https://user-images.githubusercontent.com/91276925/185267991-c0d70d29-0cde-46a7-86f7-6de246aecaf7.png)

I defined this as:

    - A max temperature lower than 80 degrees but higher than 70.
    - Wind speed less than 10 mph.
    - Zero cloudiness.
    
I then dropped any rows that don't satisfy all three conditions and used the Google Places API to find the first hotel for each city located within 5,000 meters of the coordinates. Lastly, I plotted the hotels on top of the humidity heatmap, with each pin containing the Hotel Name, City, and Country.
















