# Blackjack
<a href="https://exercism.org/tracks/go/exercises/blackjack">Click here to go to the exercise with instructions</a>

## My solution

````
package blackjack

// ParseCard returns the integer value of a card following blackjack ruleset.
func ParseCard(card string) int {
    var value int = 0
	switch card {
        case "ace":
    	value = 11
		break

        case "two":
    	value = 2
		break

        case "three":
    	value = 3
		break

        case "four":
    	value = 4
		break

        case "five":
    	value = 5
		break

        case "six":
    	value = 6
		break

        case "seven":
    	value = 7
		break

        case "eight":
    	value = 8
		break

        case "nine":
    	value = 9
		break

        case "ten", "jack", "queen", "king":
    	value = 10
		break
        
        default:
    	value = 0
        break
    }

    return value
}

// FirstTurn returns the decision for the first turn, given two cards of the
// player and one card of the dealer.
func FirstTurn(card1, card2, dealerCard string) string {
	var numberOne int = ParseCard(card1)
    var numberTwo int = ParseCard(card2)
    var numberDealerCard int = ParseCard(dealerCard)
    var response string = ""

	switch {
        case numberOne == 11 && numberTwo == 11 :
    	response = "P"
        break

        case (numberOne + numberTwo == 21) && (numberDealerCard != 11 && numberDealerCard != 10):
    	response = "W"
        break

        case (numberOne + numberTwo == 21) && (numberDealerCard == 11 || numberDealerCard == 10):
    	response = "S"
        break

        case (numberOne + numberTwo >= 17) && (numberOne + numberTwo <= 20):
    	response = "S"
        break

        case ((numberOne + numberTwo >= 12) && (numberOne + numberTwo <= 16)) && numberDealerCard < 7:
    	response = "S"
        break

        case ((numberOne + numberTwo >= 12) && (numberOne + numberTwo <= 16)) && numberDealerCard >= 7:
    	response = "H"
        break

        case numberOne + numberTwo <= 11:
    	response = "H"
        break
    	
    }

    return response

}
````
