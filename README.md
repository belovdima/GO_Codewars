
# 💻 GO Codewars

---

## ✅ 1. Boolean to Word

**Описание:**  
Заверши метод, который принимает значение `bool` и возвращает строку `"Yes"` для `true` и `"No"` для `false`.

```go
package kata

func BoolToWord(word bool) string {
	if word == true {
		return "Yes"
	} else {
		return "No"
	}
}
```

---

## 🔢 2. Convert a String to a Number

**Описание:**  
Функция принимает строку и возвращает соответствующее число.

```go
package kata

import "strconv"

func StringToNumber(str string) int {
	output, _ := strconv.Atoi(str)
	return output
}
```

---

## 👶 3. Совершеннолетие

**Описание:**  
Напиши функцию, которая принимает возраст (`int`) и возвращает:
- `"Совершеннолетний"`, если возраст 18 и выше  
- `"Несовершеннолетний"` — если меньше

```go
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
		fmt.Println("Несовершеннолетний")
	} else {
		fmt.Println("Совершеннолетний")
	}
}
```

---

## ⚖️ 4. Чётное или нечётное

**Описание:**  
Функция принимает число и возвращает `true`, если оно чётное, и `false`, если нечётное.

```go
package main

import (
	"bufio"
	"fmt"
	"os"
	"strconv"
)

func main() {
	scanner := bufio.NewScanner(os.Stdin)
	fmt.Printf("Введите число: ")
	scanner.Scan()
	number, _ := strconv.Atoi(scanner.Text())
	if number%2 == 0 {
		fmt.Println("Число чётное")
	} else {
		fmt.Println("Число нечётное")
	}
}
```

---

## ➕ 5. Сумма чисел от 1 до N

**Описание:**  
Функция принимает число `n` и возвращает сумму от `1` до `n` включительно.

```go
package main

import (
	"bufio"
	"fmt"
	"os"
	"strconv"
)

func main() {
	scanner := bufio.NewScanner(os.Stdin)
	fmt.Printf("Введите число: ")
	scanner.Scan()
	number, _ := strconv.Atoi(scanner.Text())

	sum := 0
	for i := 1; i <= number; i++ {
		sum += i
	}
	fmt.Printf("Сумма от 1 до %d: %d\n", number, sum)
}
```

---

## 📅 6. День недели по числу

**Описание:**  
Функция принимает число от `1` до `7` и возвращает день недели.

```go
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
```

---

## 🔁 7. Проверка на палиндром

**Описание:**  
Функция проверяет, является ли слово палиндромом (читается одинаково в обе стороны).

```go
package main

import (
	"bufio"
	"fmt"
	"os"
)

func main() {
	scanner := bufio.NewScanner(os.Stdin)
	fmt.Print("Введите слово: ")
	scanner.Scan()
	word := scanner.Text()

	runes := []rune(word)
	isPalindrome := true

	for i := 0; i < len(runes)/2; i++ {
		if runes[i] != runes[len(runes)-1-i] {
			isPalindrome = false
			break
		}
	}

	if isPalindrome {
		fmt.Println("Это палиндром!")
	} else {
		fmt.Println("Это не палиндром.")
	}
}
```
