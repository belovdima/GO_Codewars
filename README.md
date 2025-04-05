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
## Сумма чисел от 1 до N

Напиши функцию, которая принимает число n и возвращает сумму чисел от 1 до n включительно (через цикл for).

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
	sum := 0
	number, _ := strconv.Atoi(scanner.Text())
	for i := 0; i <= number; i++ {
		sum = sum + i
		fmt.Println(sum)
	}

}

```

## Определить день недели по числу

package main

import (
	"bufio"
	"fmt"
	"os"
)

func main() {
	scanner := bufio.NewScanner(os.Stdin)
	fmt.Print("Введите число от 1 до 7: ")
	scanner.Scan()
	day := scanner.Text()

	switch day {
	case "1":
		fmt.Println("Понедельник")
	case "2":
		fmt.Println("Вторник")
	case "3":
		fmt.Println("Среда")
	case "4":
		fmt.Println("Четверг")
	case "5":
		fmt.Println("Пятница")
	case "6":
		fmt.Println("Суббота")
	case "7":
		fmt.Println("Воскресенье")
	default:
		fmt.Println("Нет такого дня недели")
	}
}
