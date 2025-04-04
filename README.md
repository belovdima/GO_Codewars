# GO_Codewars

## Complete the method that takes a boolean value and return a "Yes" string for true, or a "No" string for false.

```
package kata

func BoolToWord(word bool) string {
	if word == true {
		return "Yes"
	} else {
		return "No"
	}
}

```

## Convert a String to a Number!

```
package kata

import "strconv"

func StringToNumber(str string) int {
	output, _ := strconv.Atoi(str)
	return output
}

```
