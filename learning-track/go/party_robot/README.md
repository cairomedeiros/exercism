# Party Robot
<a href="https://exercism.org/tracks/go/exercises/party-robot">Click here to go to the exercise with instrunctions</a>

## Annotations
- Sprintf uses verbs like %s to interpolate values
- %03d has the result in a number with 3 digits, if the number is 3 the output will be 003

## My solution

```
package partyrobot
import "fmt"
// Welcome greets a person by name.
func Welcome(name string) string {
	return fmt.Sprintf("Welcome to my party, %s!", name)
}

// HappyBirthday wishes happy birthday to the birthday person and exclaims their age.
func HappyBirthday(name string, age int) string {
	return fmt.Sprintf("Happy birthday %s! You are now %d years old!", name, age)
}

// AssignTable assigns a table to each guest.
func AssignTable(name string, table int, neighbor, direction string, distance float64) string {
	return fmt.Sprintf(Welcome(name) + "\n" + "You have been assigned to table %03d. Your table is %s, exactly %.1f meters from here.\nYou will be sitting next to %s.", table, direction, distance, neighbor) 
}
```
