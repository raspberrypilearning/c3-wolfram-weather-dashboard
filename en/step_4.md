## Create a function

Now that you have a nice dashboard, you can build a more general function to find out the weather information for any city, without having to change the code.

In Wolfram, you can use `:=` to define a function. A function means that you can write code that puts the parameter `location` in place of the name of the city you want to see in the weather dashboard. Then, you run the `weatherDashboard` function using the actual name of the city (for example, `weatherDashboard["London"]`), and the function will replace the parameter `location` with the name of the city throughout the code.

--- task ---
Make a function called `weatherDashboard` with a parameter `location`.

Use `CommonName[location]` to so that the code will put the name of the city into the title automatically.

```
weatherDashboard[location_] :=
 Framed[
  Grid[{
  {Text[Style[CommonName[location], Large, Gray]], SpanFromLeft},
  {Show[IconData["AirTemperature", WeatherData[location, "Temperature"]], ImageSize -> 150],
  Show[IconData["WindDirection", WeatherData[location, "WindDirection"]], ImageSize -> 170]},
  {Show[IconData["RelativeHumidity", WeatherData[location, "Humidity"]], ImageSize -> 150],
  Show[IconData["WindSpeed", WeatherData[location, "WindSpeed"]], ImageSize -> 170]}
  }],
  RoundingRadius -> 40, FrameMargins -> 20, FrameStyle -> {Thick, Gray}]
  ```

--- /task ---
  
Now, you can run `weatherDashboard` with any city simply by running the function above, and then running the function with a specific location. You will need to use the Freeform Entry box as described in the 'Explore weather data' step.

![Final Interface](images/SF.png)
  
--- task ---
Run the `weatherDashboard` function with a few different cities.

You can also use `$GeoLocationCity` to set the location of your own computer as the city.
  
```
weatherDashboard[$GeoLocationCity]
```
--- /task ---

Congratulations, you have created a functioning weather dashboard! You can run it for any city you like, or for your geolocation.
