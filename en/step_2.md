## Exploring Weather Data

--- task ---
If you have never used the Wolfram Language before, follow [this guide](https://projects.raspberrypi.org/en/projects/getting-started-with-mathematica). You will need to look at 'Starting Mathematica' and 'Programming in Mathematica'.
--- /task ---

In this step, you will explore `WeatherData` in Wolfram. 

Wolfram has all kinds of current information about the weather. In order to find weather information for a specific city, you can enter the name of the city using Freeform Linguistic Data.

If you are using a desktop application version of Wolfram, when you start to type the name of a city, a pop-up may appear, asking if you want to 'Convert to Freeform Linguistic Input'. You should select this option.

You can also press `[Control] + [=]` to access a Freeform Input box directly within your code.

Otherwise, you can put the name of the city in quotes `""`. This will work for most cities.

```
WeatherData["Hanoi", "Temperature"]

WeatherData["Boston", "Humidity"]

WeatherData["Sydney", "WindDirection"]

WeatherData["Cape Town", "WindSpeed"]
```

`IconData` includes some cool weather icons which will be helpful in building this dashboard.

![Icon Data](images/icondata.png)

---task---
Use the following code to get the temperature data and icon for London. If you like, you can change it to another capital city.

```
IconData["AirTemperature", WeatherData["London", "Temperature"]]
```
---/task---

--- task ---
Now follow the examples above to use `WeatherData` to find out the humidity, wind direction, and wind speed in the capital city you have chosen.

--- hints ---
--- hint ---
This code will find the weather information for London. If you like, you can find the weather information for another capital city.

```
IconData["WindDirection", WeatherData["London", "WindDirection"]]
```
```
IconData["RelativeHumidity", WeatherData["London", "Humidity"]]
```
```
IconData["WindSpeed", WeatherData["London", "WindSpeed"]]
```
--- /hint ---
--- /hints ---
--- /task ---
