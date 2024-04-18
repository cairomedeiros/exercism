# Weather Forecast

## Annotations

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
