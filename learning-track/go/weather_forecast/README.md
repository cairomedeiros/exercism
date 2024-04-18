# Weather Forecast
<a href="https://exercism.org/tracks/go/exercises/weather-forecast">Click here to go to the exercise with instructions</a>

## Annotations

#### Comments
- We should write comments very clear starting with the name of the thing just like "// Package x " and finish with a period.

## My Solution
```
// Package weather package that can forecast the current weather condition.
package weather

// CurrentCondition can store the current weather condition.
var CurrentCondition string
/* CurrentLocation can store the current location that the program is calculating the weather. */
var CurrentLocation string

// Forecast returns the current weather with his location.
func Forecast(city, condition string) string {
	CurrentLocation, CurrentCondition = city, condition
	return CurrentLocation + " - current weather condition: " + CurrentCondition
}
```
