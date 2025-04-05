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

## Напиши функцию, которая принимает возраст (int) и возвращает строку:

"Совершеннолетний", если возраст 18 и выше

"Несовершеннолетний" — если меньше

```
package main

import (
	"bufio"
	"fmt"
	"os"
	"strconv"
)

func main() {
	scanner := bufio.NewScanner(os.Stdin)
	fmt.Printf("Введите свой возраст: ")
	scanner.Scan()
	age, _ := strconv.Atoi(scanner.Text())
	if age < 18 {
		fmt.Println("Несовершеннолетний\n")
	} else {
		fmt.Println("Совершеннолетний\n")
	}
}

```

## Чётное или нечётное
Напиши функцию, которая принимает число и возвращает true, если оно чётное, и false, если нечётное.

```
package main

import (
	"bufio"
	"fmt"
	"os"
	"strconv"
)

func main() {
	scanner := bufio.NewScanner(os.Stdin)
	fmt.Printf("ВВедите число ")
	scanner.Scan()
	number, _ := strconv.Atoi(scanner.Text())
	if number%2 == 0 {
		fmt.Println("Число чётное")
	} else {
		fmt.Println("Число нечётное")
	}
}

```
