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