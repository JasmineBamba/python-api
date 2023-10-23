# python-api


## Table of Contents
- [Application Programing Interface (API)](#application-programing-interface-(API))
- [JSON Traversals](#json-traversals)
- [Project Overview](#project-overview)
- [Part1: WeatherPy](#part1)
- [Part2: VacationPy](#part2)
- [APIs Used & Documentation](#api-documentation)
- [References](#ref)

## Application Programing Interface (API)

![image](https://github.com/JasmineBamba/python-api/assets/135666038/8ae2d3e0-f6e4-452c-8854-2e736bbfaa82)

APIs are a set of rules and protocols that allow different software applications to communicate with each other. APIs provide a way for one software program to request and exchange data with another, facilitating the integration of services and data from various sources. APIs are used to access services, data, or functionality provided by web servers, databases, and other applications.

## JSON Traversals

JSON traversals refer to the process of navigating and extracting data from JSON structures. This typically involves accessing specific keys, values, or elements within a JSON object or array. Traversing JSON data is a fundamental task in working with APIs because API responses are often provided in JSON format. Python provides libraries like json for parsing and manipulating JSON data, making it easy to extract and use data from JSON responses.

![image](https://github.com/JasmineBamba/python-api/assets/135666038/08b9ad45-5c10-44de-9d71-783ecaa30a2a)

## Project Overview

The exploration of weather conditions as we approach the equator is a fundamental scientific inquiry that delves into the intricate dynamics of our planet's climate. While the notion that it gets hotter as we near the equator may seem evident, the goal of this project is to move beyond this basic observation and harness the power of data to provide a definitive answer and deeper insights.

![image](https://github.com/JasmineBamba/python-api/assets/135666038/5e4aec78-a837-49f9-ac85-d8fd8f5edce0)

Data is a powerful tool that empowers us to go beyond general observations and test hypotheses rigorously. By collecting and analyzing weather data from a variety of locations at different latitudes, we can uncover trends, patterns, and correlations that might not be immediately obvious.

## Part1: WeatherPy

**Relationship Between Weather Variables and Latitude**

In the first part of the project, OpenWeatherMap API weere used to retrieve weather data for over 500 cities. Series of scatter plots were created to showcase the relationships between latitude and various weather variables:

- Latitude vs. Temperature: Analyzed how temperature changes with latitude.
- Latitude vs. Humidity: Explored the relationship between latitude and humidity.
- Latitude vs. Cloudiness: Investigated how cloudiness varies with latitude.
- Latitude vs. Wind Speed: Examined how wind speed is related to latitude.

![image](https://github.com/JasmineBamba/python-api/assets/135666038/30e75660-8211-49fd-a28c-40c03f27c95d)

**Linear Regression Analysis**

Linear regressions for each of these relationships were computed, splitting the data into Northern and Southern Hemispheres. Linear regression lines, the model's formula, and the r-values were included in the scatter plots.

The following scatter plots were created:

- Northern Hemisphere: Temperature vs. Latitude
- Southern Hemisphere: Temperature vs. Latitude
- Northern Hemisphere: Humidity vs. Latitude
- Southern Hemisphere: Humidity vs. Latitude
- Northern Hemisphere: Cloudiness vs. Latitude
- Southern Hemisphere: Cloudiness vs. Latitude
- Northern Hemisphere: Wind Speed vs. Latitude
- Southern Hemisphere: Wind Speed vs. Latitude

![image](https://github.com/JasmineBamba/python-api/assets/135666038/1158af92-cf4c-480d-9349-509aefc58dcb)

In each section, we explained what the linear regression was modeling and shared any notable findings or relationships that we observed in the data. This analysis provides valuable insights into how weather variables are affected by a city's proximity to the equator.

## Part2: VacationPy

In the second part of the project, we leveraged our weather data and used the geoViews Python library to plan future vacations. We also incorporated the Geoapify API to create map visualizations.

1. **Humidity Map:** We generated a map displaying points for each city in the city_data_df DataFrame, with the size of the points representing the humidity level in each city.

![image](https://github.com/JasmineBamba/python-api/assets/135666038/a77a4c83-b858-474d-bbff-f7b1216e4eac)

2. **Ideal Weather Conditions:** We narrowed down the city_data_df DataFrame to find our ideal weather conditions, including a specific temperature range, wind speed, and cloudiness criteria.
   
![image](https://github.com/JasmineBamba/python-api/assets/135666038/8f79178c-4757-4203-b3c0-0ad635029296)
![image](https://github.com/JasmineBamba/python-api/assets/135666038/9cdffb2e-90ae-46f1-a805-231764c3fa57)


3. **Hotel Data:** We created a new DataFrame called hotel_df to store information about hotels, including the city, country, coordinates, and humidity.

![image](https://github.com/JasmineBamba/python-api/assets/135666038/641335de-82e0-47d5-a381-65a19a931efb)

4. **Hotel Selection:** For each city, we used the Geoapify API to find the first hotel located within 10,000 meters of the coordinates.
  
![image](https://github.com/JasmineBamba/python-api/assets/135666038/1f009875-373c-407b-9b52-44ae6b9b9b93)

6. **Hover Messages:** We added the hotel name and the country as additional information in the hover message for each city on the map, allowing us to plan future vacations with essential details.

![image](https://github.com/JasmineBamba/python-api/assets/135666038/728c0961-9579-4fa2-8f10-62ad9da7560c)

This part of the project empowers us to make informed decisions about vacation destinations based on weather conditions and provides a visually engaging way to explore potential travel spots.


## APIs Used & Documentation

- OpenWeatherMap API (weather information):
https://openweathermap.org/api/one-call-3

- Geoapify (used to locating points on map by using latitude & longitude):
https://apidocs.geoapify.com/#docs

- Citipy Python Package (to look up city names and corresponding country codes based on latitude and longitude coordinates)
https://pypi.org/project/citipy/

**Protecting API Keys:** To safeguard API keys, it's recommeneded to create a separate file to mention api keys used (in this project they were stored in api_keys.py file) and include this file in .gitignore. This ensures our keys remain confidential and are not shared publicly on GitHub, preventing unauthorized access and potential cost implications.
