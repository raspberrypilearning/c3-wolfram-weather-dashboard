## Exploring Weather Data

In this step, you will explore `WeatherData` in Wolfram. 

Wolfram has all kinds current information about the weather. In order to find weather information for a specific place, you  enter a city using Freeform Linguistic Data.

If you are using a desktop application version of Wolfram, then when you start to type the name of a city, a pop up may appear, asking if you want to Convert to Freeform Linguistic Input. You should select this option.

You can also press `[Control] + [=]` to access a Freeform Input box directly within your code. This is the best option if you are using Wolfram in a web browser.

A final option is to put the name of the city in quotes `""`, which will work for the majority of cities.

```
WeatherData["Hanoi", "Temperature"]

WeatherData["Boston", "Humidity"]

WeatherData["Sydney", "WindDirection"]

WeatherData["Cape Town", "WindSpeed"]
```

`IconData` includes some cool weather icons which will be helpful in building this dashboard.

![Icon Data](images/icondata.png)

---task---
Try getting the temperature data and icon for your capital city

```
IconData["AirTemperature", WeatherData["London", "Temperature"]]
```
```
IconData["WindDirection", WeatherData["London", "WindDirection"]]
```
```
IconData["RelativeHumidity", WeatherData["London", "Humidity"]]
```
```
IconData["WindSpeed", WeatherData["London", "WindSpeed"]]
```
---/task---
