# angular-weather-app

Create an Angular web application that displays weather data for a user-defined location.

![](docs/weather-app-angular_small.png)

👉 ``Fork`` the repository and solve the tasks in a ``solution branch`` 👈


# REST API
The weather data should be accessed via the following service: https://www.weatherapi.com

The service provides an explorer through which the API can be tested: https://www.weatherapi.com/api-explorer.aspx

The API key is sent via email.

# Technical requirements
1. The user should be able to enter a location
2. The user should be able to enter a specific date in the format `dd.MM.yyyy`
3. The user should see the weather data for “Today”, “Tomorrow” and “Today + 2 days”.

## Weather data
The term “weather data” means the following values:
- Name of the place
- Name of the region
- Name of the country
- Time zone
- Temperature in C°
- Felt temperature in C°
- Wind speed in km/h
- Wind direction
- Cloud probability in %
- Chance of rain in %

### Weather data - Today
The user should be shown the current weather data and forecast data for the current day.
The forecast data results from the weather data, which are aggregated over time as follows:
- Morning (average values from 6 a.m. to 12 p.m.)
- Midday (average from 12 p.m. to 6 p.m.)
- Evening (average from 6 p.m. to 10 p.m.)
- At night (average values from 10 p.m. to 6 a.m.)

### Weather data - Tomorrow | Today + 2 days
For these two variants, the forecast data should be displayed as in the previous variant.
The current weather data is no longer displayed.

## Depiction
There are no requirements for the display of weather data. You can decide for yourself how the data should be displayed to the user.

# Technical requirements
- The Angular Framework should be used to implement the web application.
- Functions should be tested via unit tests.
- Dependencies may be installed and used at your own discretion.

# Documentation
No independent documentation is required for implementation. However, the code should be provided with comments at your own discretion.

# Questions & Problems

If questions arise or problems arise, try to accept/solve them as best you can and document what decisions and requirements you have made.

# Internal note
*can be ignored*

## Build build
````shell
docker build -t noderunner .
````

## Run app in container
````shell
docker run -v .:/app -p 4200:4200 -it noderunner bash
````

### in container start
````shell
npm install
ng serve
````
