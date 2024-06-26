# Annalyn's Infiltration
<a href="https://exercism.org/tracks/go/exercises/annalyns-infiltration">Click to go to the exercise with instructions</a>

## Annotations
#### Booleans
- Booleans are represented by the type bool

#### Logical Operators
- #### ```&&``` is true if both statements are true

- #### ```||``` is true if at least one is true

- #### ```!``` is true only if the statement is false

## My Solution

````
package annalyn
// CanFastAttack can be executed only when the knight is sleeping.
func CanFastAttack(knightIsAwake bool) bool {
    if(knightIsAwake){
        return false
    }else{
    return true
    }
}
// CanSpy can be executed if at least one of the characters is awake.
func CanSpy(knightIsAwake, archerIsAwake, prisonerIsAwake bool) bool {
	if(knightIsAwake || archerIsAwake || prisonerIsAwake){
        return true
    }else{
    return false
    }
}
// CanSignalPrisoner can be executed if the prisoner is awake and the archer is sleeping.
func CanSignalPrisoner(archerIsAwake, prisonerIsAwake bool) bool {
	if(!archerIsAwake && prisonerIsAwake){
        return true
    }else{
    return false
    }
}
// CanFreePrisoner can be executed if the prisoner is awake and the other 2 characters are asleep
// or if Annalyn's pet dog is with her and the archer is sleeping.
func CanFreePrisoner(knightIsAwake, archerIsAwake, prisonerIsAwake, petDogIsPresent bool) bool {
	if(petDogIsPresent && !archerIsAwake){
        return true
    }else{
    	if(!knightIsAwake && !archerIsAwake && prisonerIsAwake){
            return true
        }else{
        return false
        }
    }
}
