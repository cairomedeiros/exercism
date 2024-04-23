# Welcome To Tech Palace
<a href="https://exercism.org/tracks/go/exercises/welcome-to-tech-palace">Click here to go to the exercise with instructions</a>

## Annotations
#### Strings
- A string in go is a immutable sequence of bytes
- A string literal is defined between double quotes
- Strings can be concatened vi the + operator
- \t can be used for a tab and \n for a new line in strings

## My solution

````
package techpalace
import "strings"
// WelcomeMessage returns a welcome message for the customer.
func WelcomeMessage(customer string) string {
	return "Welcome to the Tech Palace, " + strings.ToUpper(customer)
}
// AddBorder adds a border to a welcome message.
func AddBorder(welcomeMsg string, numStarsPerLine int) string {
    var stars string = ""
	for i := 0; i < numStarsPerLine; i++{
        stars += "*"
    }
	return stars + "\n" + welcomeMsg + "\n" + stars
}
// CleanupMessage cleans up an old marketing message.
func CleanupMessage(oldMsg string) string {
	var msgFormatted string = strings.ReplaceAll(oldMsg, "*", "")
    return strings.TrimSpace(msgFormatted)
}
````
