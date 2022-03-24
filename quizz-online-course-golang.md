# Quizz Golang

## Online Course Golang (Basic)

1. What does the following code print to the console?

    ```go
    package main

    import "fmt"

    func main() {
        fmt.Println("Welcome to CAMP2022")
    }

    ```
    **A.** "Welcome to CAMP2022" is printed to the console.
    
    B. "welcome to CAMP2021" is printed to the console.
    
    C. "welcomE to CAMP2022" is printed to the console.
    
    D. "welcom3 to CAMP2022" is printed to the console.

2. What does the following code print to the console?
    ```go
    package main

    import "fmt"

    func main() {
        fmt.Println(3134 != 2123)
    }
    ```
    A. `false`

    B. `int32`

    **C.** `true`

    D. `int64`

3. What does the following code print to the console?
    ```go
        fmt.Println("gina" == "bimo" || 1992 != 1996)
    ```
    A. `false` is printed.

    **B.** `true` is printed.

    C. `float32` is printed.

    D. `floar64` is printed.

4. What does the following code print to the console?
    ```go
    name := "juno"
    if name == "gina" {
        fmt.Println("jepang")
    } else if name == "steven" {
        fmt.Println("cina")
    } else {
        fmt.Println("indonesia")
    }
    ```

    A. "juno" is printed.

    B. "jepang" is printed.

    C. "cina" is printed.

    **D**. "indonesia" is printed.
    
5. The code below will generate?

   ![](https://mahabib.files.wordpress.com/2014/09/c552e-2-1.png?w=665)
   
   **A**. Primes

   B. Integers

   C. Odd numbers

   D. Even number

6. What does the following code print to the console?
    ```go
    hairColor := "blue"
    if 3 > 2 {
        if hairColor == "black" {
            fmt.Println("You rock!")
        } else {
            fmt.Println("Boring")
        }
    }
    ```
    A. "You rock!" is printed.

    B. "black" is printed.

    **C**. "Boring" is printed.

    D. "blue" is printed.

7. What does the following code print to the console?
    ```go
    i := 2
    switch i {
    case 0:
        fmt.Println("Zero")
    case 1:
        fmt.Println("One")
    case 2:
        fmt.Println("Two")
    case 3:
        fmt.Println("Three")
    default:
        fmt.Println("Whatever")
    }
    ```
    **A**. Two is printed to the console.

    B. Three is printed to the console.

    C. Zero is printed to the console.

    D. Whatever is printed to the console.

8. What does the following code print to the console?
    ```go
    colors := [2]string{"cianjur", "bandung", "jakarta"}
    fmt.Println(colors[1])
    ```
    A. "bandung" is printed to the console.

    **B**. This code returns the following error: array index 2 out of bounds [0:2].

    C. This code returns the following complete: array index 1[0:1] is `true`

    D. "jakarta" is printed to the console.

9. What does the following code print to the console?
    ```go
    animals := [4]string{"bird", "fish"}
    fmt.Println(len(animals))
    ```

    A. 2 is printed.

    B. This code returns the following error: array index 4 out of bounds [0:4].

    C. 1 is printed.

    **D**. 4 is printed.

10. What does the following code print?
    ```go
    var letters = []string{"a", "b", "c"}
    var someLetters = make([]string, 2)
    copy(someLetters, letters)
    fmt.Println(someLetters)
    ```
    A. [c b] is printed.

    B. [a c] is printed.

    **C**. [a b] is printed.

    D. [c a] is printed.

11. What does the following code print?
    ```go
    var odds = []int{1, 3}
    var evens = []int{8, 10}
    fmt.Println(append(odds, evens...))
    ```
    **A**. [1 3 8 10] is printed.

    B. [8 10 1 3] is printed.

    C. [1 3 10 8] is printed.

    D. [1 8 3 10] is printed.

12. What does the following code print?
    ```go
    places := make(map[string]int)
    fmt.Println(places["diamond"])
    ```
    A. 1 is printed.

    B. 5 is printed.

    **C**. 0 is printed.

    D. 2 is printed.

13. What does the following code print?
    ```go
    countryCodes := map[string]string{
        "93":  "Afghanistan",
        "374": "Armenia",
        "61":  "Australia",
    }
    country, ok := countryCodes["999"]
    fmt.Println(country == "", ok == false)
    ```
    A. `false` `false` is printed.

    B. `false` `true` is printed.

    C. `true` `false` is printed.

    **D**. `true` `true` is printed.
    

14. What does the following code print?
    ```go
    countryCodes := map[string]string{
        "93":  "Rusia",
        "374": "Amerika",
        "61":  "Spanyol",
        "94":  "Indonesia",
    }
    if country, ok := countryCodes["93"]; ok {
        fmt.Println(country, "is a beautiful place")
    } else {
        fmt.Println("I don't know that country")
    }
    ```
    **A**. Rusia is a beautiful place is printed.

    B. Amerika is a beautiful place is printed.

    C. Indonesia is a beautiful place is printed.

    D. Spanyol is a beautiful place is printed.

15. What does the following code print?
    ```go
    meaning := map[string]map[string]string{
        "red": map[string]string{
            "element": "fire",
            "feeling": "hot",
        },
        "blue": map[string]string{
            "element": "water",
            "feeling": "cold",
        },
    }
    fmt.Println(meaning["blue"]["feeling"])
    ```
    A. "water" is printed.

    **B**. "cold" is printed.

    C. "fire" is printed.

    D. "hot" is printed.

16. What does the following code print?
    ```go
    var a = [...]int{5, 6, 7}
	var b = [...]int{3, 6, 10}

	arr := []int{0, 0}
	for i := range a {
		if a[i] > b[i] {
			arr[0] = arr[0] + 1
		} else if a[i] < b[i] {
			arr[1] = arr[1] + 1
		}
	}
	fmt.Println(arr)
    ```
    A. [2 0]

    B. [0 1]

    **C**. [1 1]

    D. [0 0]
    

17. What does the following code print?
    ```go
    var i, j, k int
    for i = 11; i > 0; i-- {
        for j = 1; j <= i; j++ {
            fmt.Printf(" ")
        }
        for k = 11; k > i; k-- {
            fmt.Printf("#")
        }
        fmt.Printf("\n")
    }
    ```

    A.
```
          *
         **
        ***
       ****
      *****
     ******
    *******
   ********
  *********
 **********
```

**B.**
```
          #
         ##
        ###
       ####
      #####
     ######
    #######
   ########
  #########
 ##########
```

C. 
```
*
**
***
****
*****
******
*******
********
*********
```

D. 
```
#
##
###
####
#####
######
#######
########
#########
```

18. What does the following code print?
    ```go
    var i, j, k, l int
	for i = 11; i > 0; i-- {
		for j = 1; j <= i; j++ {
			fmt.Printf(" ")
		}
		for k = 10; k > i; k-- {
			fmt.Printf("*")
		}
		for l = 11; l > i; l-- {
			fmt.Printf("*")
		}
		fmt.Printf("\n")
	}
    ```
A. 
```
*********************
 *******************
  *****************
   ***************
    *************
     ***********
      *********
       *******
        *****
         ***
          *
```

B. 
```
          #
         *##
        **###
       ***####
      ****#####
     *****######
    ******#######
   *******########
  ********#########
 *********##########
```

C. 
```
  *****************
 *******************
*********************
 *******************
  *****************
   ***************
    *************
     ***********
      *********
       *******
        *****
         ***
          *
```

**D.** 
```
          *
         ***
        *****
       *******
      *********
     ***********
    *************
   ***************
  *****************
 *******************
```

19. What does the following code print?
    ```go
    func average(nums []float64) float64 {
        total := 0.0
        for _, v := range nums {
            total += v
        }
        return total / float64(len(nums))
    }

    func main() {
        scores := []float64{10, 11, 12, 13}
        fmt.Println(average(scores))
    }
    ```
    A. 21.5 is printed.

    **B**. 11.5 is printed.
    
    C. 12.5 is printed.

    D. 31.5 is printed.

20. What does the following code print?
    ```go
    func addAll(nums ...int) int {
        total := 0
        for _, v := range nums {
            total += v
        }
        return total
    }

    func main() {
        points := []int{5, 10, 15}
        fmt.Println(addAll(points...))
    ```
    A. 10 is printed.

    B. 40 is printed.

    C. 20 is printed.

    **D**. 30 is printed.

---



## Online Course Golang (Intermediate)
1. Select the code that gives the print output:
```
          *
         ***
        *****
       *******
      *********
     ***********
    *************
   ***************
  *****************
```

**A.**  
    
```go
    var i, j, k, l int
	for i = 11; i > 0; i-- {
		for j = 1; j <= i; j++ {
			fmt.Printf(" ")
		}
		for k = 10; k > i; k-- {
			fmt.Printf("*")
		}
		for l = 11; l > i; l-- {
			fmt.Printf("*")
		}
		fmt.Printf("\n")
	}
```

B.
```go
    var i, j, k int
    for i = 11; i > 0; i-- {
        for j = 1; j <= i; j++ {
            fmt.Printf(" ")
        }
        for k = 11; k > i; k-- {
            fmt.Printf("#")
        }
        fmt.Printf("\n")
    }
```

C. 
```go
    for i := range a {
        if a[i] > b[i] {
            arr[0] = arr[0] + 1
        } else if a[i] < b[i] {
            arr[1] = arr[1] + 1
        }
    }
```

D. 
```go
    var i, j int
	for i = 0; i < 10; i++ {
		for j = 0; j < i; j++ {
			fmt.Printf("i: %v j: %v * ", i, j)
		}
		fmt.Printf("\n")
	}
```

2. Choose golang code implementation to generate circle area value: 

A. 
```go 
	var side, res float32
    side = 5
	res = side * side
    fmt.Printf("%f", res)
```

B. 
```go
    var a, t, res float32
    a = 5
    t = 7
    res = 0.5 * a * t
    fmt.Printf("%f", res)
```

**C.** 
```go
    var r, res float64
	const pi float64 = 3.14
    r := 5 
	res = pi * (math.Pow(r, 2))
	fmt.Printf("%f", res)
```

D. 
```go
    var r, h, res float32
    const pi = 3.14
    r = 5
    h = 10
    volume = res * r * r * height
```

3. What does the following code print?
```go
    i := 2 
    s := "1000"
    if len(s) > 1 {
        i, _ := strconv.Atoi(s)
        i = i + 5
    }
    fmt.Println(i)
```

A. 5  

B. 1005  

C. compilation error 

**D**. 2

4. What does the following code print?
```go
func hello(num ...int) {  
    num[0] = 22
}

func main() {  
    i := []int{5, 6, 7}
    hello(i...)
    fmt.Println(i[0])
}
``` 

A. 18  

B. 5

**C.** 22

D. Compilation error


6. What does the following code print?
```go
type rect struct {  
    len, wid int
}

func (r rect) area() {  
    fmt.Println(r.len * r.wid)
}

func main() {  
    r := &rect{len: 5, wid: 6}
    r.area()
}
```
A. compilation error  

**B**. 30

C. 200

D. 5


7. What does the following code print?
```go
    s := make(map[string]int)
    delete(s, "h")
    fmt.Println(s["h"])
```

A. runtime panic 

**B**. 0

C. compilation error

D. 5 

8. Choose solution for Problem Hackerrank: //www.hackerrank.com/challenges/counter-game?

**A**. 
```go
    powerOfTwos := make([]int64, 0)
	for i := int64(1); i <= n; i *= 2 {
		powerOfTwos = append(powerOfTwos, i)
	}

	turn := 0
	for n > 1 {
		turn += 1
		if contains(powerOfTwos, n) {
			n /= 2
			continue
		}

		prevPowerOfTwo := int64(1)
		for i := len(powerOfTwos) - 1; i >= 0; i-- {
			if n > powerOfTwos[i] {
				prevPowerOfTwo = powerOfTwos[i]
				break
			}
		}
		n -= prevPowerOfTwo
	}

	if turn == 0 {
		return "Louise"
	} else {
		if turn%2 == 1 {
			return "Louise"
		} else {
			return "Richard"
		}
	}
```

B. 
```go
    count := make(map[rune]int)
	for _, c := range s {
		count[c]++
	}

	uniqCounts := make(map[int]int)
	for _, v := range count {
		uniqCounts[v] += 1
	}

	if len(uniqCounts) == 1 {
		return "YES"
	} else if len(uniqCounts) == 2 {
		keys := []int{}
		values := []int{}
		for k, v := range uniqCounts {
			keys = append(keys, k)
			values = append(values, v)
		}

		for i := 0; i < 2; i++ {
			if keys[i] == 1 && values[i] == 1 {
				//since the count is 1, we can just remove it
				return "YES"
			}
			//need to reduce by one
			if keys[i]-keys[1-i] == 1 {
				//only one item can be reduced
				if values[i] == 1 {
					return "YES"
				}
			}
		}
	}
	return "NO"
```
C. 
```go
   positions := make(map[int]int)
	for i := 0; i < len(arr); i++ {
		positions[arr[i]] = i
	}
	sorted := make([]int, len(arr))
	copy(sorted, arr)
	sort.Slice(sorted, func(i, j int) bool {
		return sorted[i] > sorted[j]
	})

	turn := 0
	for len(arr) > 0 {
		turn += 1

		max := -1
		for {
			max = sorted[0]
			sorted = sorted[1:]
			if positions[max] < len(arr) {
				break
			}
		}

		deleteFrom := positions[max]
		arr = arr[:deleteFrom]
	}
	if turn%2 == 0 {
		return "ANDY"
	}
	return "BOB"
```
D. 
```go
	sumDigit := func(n string) int64 {
		sum := int64(0)
		for _, c := range n {
			digit := int64(c) - '0'
			sum += digit
		}
		return sum
	}

	if len(n) == 1 && k == 1 {
		res, _ := strconv.Atoi(n)
		return int32(res)
	} else {
		return superDigit(fmt.Sprint(sumDigit(n)*int64(k)), 1)
	}
```

9. Choose solution for Problem Hackerrank: https://www.hackerrank.com/challenges/sherlock-and-valid-string/problem
A. 
```go
    powerOfTwos := make([]int64, 0)
	for i := int64(1); i <= n; i *= 2 {
		powerOfTwos = append(powerOfTwos, i)
	}

	turn := 0
	for n > 1 {
		turn += 1
		if contains(powerOfTwos, n) {
			n /= 2
			continue
		}

		prevPowerOfTwo := int64(1)
		for i := len(powerOfTwos) - 1; i >= 0; i-- {
			if n > powerOfTwos[i] {
				prevPowerOfTwo = powerOfTwos[i]
				break
			}
		}
		n -= prevPowerOfTwo
	}

	if turn == 0 {
		return "Louise"
	} else {
		if turn%2 == 1 {
			return "Louise"
		} else {
			return "Richard"
		}
	}
```

**B**. 
```go
    count := make(map[rune]int)
	for _, c := range s {
		count[c]++
	}

	uniqCounts := make(map[int]int)
	for _, v := range count {
		uniqCounts[v] += 1
	}

	if len(uniqCounts) == 1 {
		return "YES"
	} else if len(uniqCounts) == 2 {
		keys := []int{}
		values := []int{}
		for k, v := range uniqCounts {
			keys = append(keys, k)
			values = append(values, v)
		}

		for i := 0; i < 2; i++ {
			if keys[i] == 1 && values[i] == 1 {
				//since the count is 1, we can just remove it
				return "YES"
			}
			//need to reduce by one
			if keys[i]-keys[1-i] == 1 {
				//only one item can be reduced
				if values[i] == 1 {
					return "YES"
				}
			}
		}
	}
	return "NO"
```
C. 
```go
    positions := make(map[int]int)
	for i := 0; i < len(arr); i++ {
		positions[arr[i]] = i
	}
	sorted := make([]int, len(arr))
	copy(sorted, arr)
	sort.Slice(sorted, func(i, j int) bool {
		return sorted[i] > sorted[j]
	})

	turn := 0
	for len(arr) > 0 {
		turn += 1

		max := -1
		for {
			max = sorted[0]
			sorted = sorted[1:]
			if positions[max] < len(arr) {
				break
			}
		}

		deleteFrom := positions[max]
		arr = arr[:deleteFrom]
	}
	if turn%2 == 0 {
		return "ANDY"
	}
	return "BOB"
```
D. 
```go
	sumDigit := func(n string) int64 {
		sum := int64(0)
		for _, c := range n {
			digit := int64(c) - '0'
			sum += digit
		}
		return sum
	}

	if len(n) == 1 && k == 1 {
		res, _ := strconv.Atoi(n)
		return int32(res)
	} else {
		return superDigit(fmt.Sprint(sumDigit(n)*int64(k)), 1)
	}
```

10. Choose solution for Problem Hackerrank: https://www.hackerrank.com/challenges/an-interesting-game-1/problem
A. 
```go
    powerOfTwos := make([]int64, 0)
	for i := int64(1); i <= n; i *= 2 {
		powerOfTwos = append(powerOfTwos, i)
	}

	turn := 0
	for n > 1 {
		turn += 1
		if contains(powerOfTwos, n) {
			n /= 2
			continue
		}

		prevPowerOfTwo := int64(1)
		for i := len(powerOfTwos) - 1; i >= 0; i-- {
			if n > powerOfTwos[i] {
				prevPowerOfTwo = powerOfTwos[i]
				break
			}
		}
		n -= prevPowerOfTwo
	}

	if turn == 0 {
		return "Louise"
	} else {
		if turn%2 == 1 {
			return "Louise"
		} else {
			return "Richard"
		}
	}
```

B. 
```go
    count := make(map[rune]int)
	for _, c := range s {
		count[c]++
	}

	uniqCounts := make(map[int]int)
	for _, v := range count {
		uniqCounts[v] += 1
	}

	if len(uniqCounts) == 1 {
		return "YES"
	} else if len(uniqCounts) == 2 {
		keys := []int{}
		values := []int{}
		for k, v := range uniqCounts {
			keys = append(keys, k)
			values = append(values, v)
		}

		for i := 0; i < 2; i++ {
			if keys[i] == 1 && values[i] == 1 {
				//since the count is 1, we can just remove it
				return "YES"
			}
			//need to reduce by one
			if keys[i]-keys[1-i] == 1 {
				//only one item can be reduced
				if values[i] == 1 {
					return "YES"
				}
			}
		}
	}
	return "NO"
```
**C**. 
```go
    positions := make(map[int]int)
	for i := 0; i < len(arr); i++ {
		positions[arr[i]] = i
	}
	sorted := make([]int, len(arr))
	copy(sorted, arr)
	sort.Slice(sorted, func(i, j int) bool {
		return sorted[i] > sorted[j]
	})

	turn := 0
	for len(arr) > 0 {
		turn += 1

		max := -1
		for {
			max = sorted[0]
			sorted = sorted[1:]
			if positions[max] < len(arr) {
				break
			}
		}

		deleteFrom := positions[max]
		arr = arr[:deleteFrom]
	}
	if turn%2 == 0 {
		return "ANDY"
	}
	return "BOB"
```
D. 
```go
	sumDigit := func(n string) int64 {
		sum := int64(0)
		for _, c := range n {
			digit := int64(c) - '0'
			sum += digit
		}
		return sum
	}

	if len(n) == 1 && k == 1 {
		res, _ := strconv.Atoi(n)
		return int32(res)
	} else {
		return superDigit(fmt.Sprint(sumDigit(n)*int64(k)), 1)
	}
```
