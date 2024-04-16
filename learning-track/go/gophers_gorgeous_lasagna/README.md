# Gopher's Gorgeous lasagna
<a href="https://exercism.org/tracks/go/exercises/lasagna">Click to go to exercise with instrunctions</a>

## Annotations

#### Packages
- Applications in go are oranizeds in packages
- When a package is imported, only entitys(functions, types, variables and constants) with capital letter can be used/acessed
- The style of naming in go is using camelCase except for those meant to be accessible across packages, that should be PascalCase

#### Variables
- Variables can be defined specifying a type
- If you use a initializer, will be assigned the type of the initializer to the variable
- Once the type is declared, the variable type does not change

#### Constants
- Your value does not change during the program execution

#### Functions
- Accept one or more parameters
- Does not accept type inference in parameters

## My solution

```
package lasagna

// TODO: define the 'OvenTime' constant
const OvenTime = 40
// RemainingOvenTime returns the remaining minutes based on the `actual` minutes already in the oven.
func RemainingOvenTime(actualMinutesInOven int) int {
    return OvenTime - actualMinutesInOven
}

// PreparationTime calculates the time needed to prepare the lasagna based on the amount of layers.
func PreparationTime(numberOfLayers int) int {
    return numberOfLayers * 2
}

// ElapsedTime calculates the time elapsed cooking the lasagna. This time includes the preparation time and the time the lasagna is baking in the oven.
func ElapsedTime(numberOfLayers, actualMinutesInOven int) int {
	return PreparationTime(numberOfLayers) + actualMinutesInOven
    
}
