# python-api-challenge

## Background
The goal of this project is to utilize Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?" We already have a sense that temperature will have a tendency to increase, but how can we use data to prove this or gather additional insights alongside this?

### Part 1: WeatherPy

In this section, I created a Python script to visualize the weather of 500+ cities of varying distance from the equator. To do so, I used a simple Python library, the OpenWeatherMap API, to create a representative model of weather across cities.
The first thing to do was to create a series of scatter plots to showcase the following relationships as areas of interest:

    Temperature (F) vs. Latitude
    Humidity (%) vs. Latitude
    Cloudiness (%) vs. Latitude
    Wind Speed (mph) vs. Latitude

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

After each pair of plots, explained what the linear regression is modeling. For example, described any relationships that I noticed and any other findings.

#### Deliverables
Notebook that includes:

  - Randomly selected at least 500 unique (non-repeated) cities based on latitude and longitude.
  - Performed a weather check on each of the cities using a series of successive API calls.
  - Included a print log of each city as it's being processed, with the city number and city name.
  - Saved a CSV of all retrieved data and a PNG image for each scatter plot.



## Background
The goal of this project is to utilize Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?" We already have a sense that temperature will have a tendency to increase, but how can we use data to prove this or gather additional insights alongside this?















This repository contains the Module 6 API challenge Notebooks and image files.
1) WeatherPy
2) VacationPy
