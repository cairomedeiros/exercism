# Cars Assemble

<a href="https://exercism.org/tracks/go/exercises/cars-assemble">Click here to go to the exercise with the instructions</a>

## Annotations

- Convertion between types in go is done via function with the name of the type to convert, example:

  `````
  var x int = 42
  f := float64(x) // f has type float64(42.0)
  `````

## My solution

```
package cars
// CalculateWorkingCarsPerHour calculates how many working cars are
// produced by the assembly line every hour.
func CalculateWorkingCarsPerHour(productionRate int, successRate float64) float64 {
    return (float64(productionRate) * successRate)/100
}
// CalculateWorkingCarsPerMinute calculates how many working cars are
// produced by the assembly line every minute.
func CalculateWorkingCarsPerMinute(productionRate int, successRate float64) int {
	var successCarsPerHour float64 = CalculateWorkingCarsPerHour(productionRate, successRate)
    return int(successCarsPerHour)/60
}
// CalculateCost works out the cost of producing the given number of cars.
func CalculateCost(carsCount int) uint {
    var carsCountRest uint = uint(carsCount) % 10
    if(carsCountRest == 0){
        return (uint(carsCount) / 10) * 95000
    }else{
    	if(carsCountRest < 1){
            //se e menor que 1 então é as unidades inferiores a 10
            return carsCountRest * 10000
        }else{
        	var carsCountDozens uint = uint(carsCount) - carsCountRest
        	return carsCountRest * 10000 + ((carsCountDozens/10) * 95000)
        }
    }
}
```
