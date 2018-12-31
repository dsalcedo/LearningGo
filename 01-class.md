# Estructura Básica

```Go
package main

import (
	"fmt" // alias of `format`, this prints in console.
)

func main () {
  // main siempre es escutado en primer lugar
}
```

# Variables

```Go
package main

import (
	"fmt" // alias of `format`, this prints in console.
)

func main () {
  var a int;
  a = 10
  
  b := 10 // automatic Type casting to int
  b := "abcd" // Error: Cannot use "abcd" (type string) as type int in assignment.
  
  e := "Hello world" // automatic Type casting to string
  e = "Overwritten Hello World"
  e := "Overwritten Hello World. This method not works, you need use `e = 'new string :0'`"
  
  // Declaring Multiples Variables at Once
  
  var f, g, h int; // Allow integers only
	f = 1
	g = 2
	h = 3
  
  var i, j, k int = 4, 5, 6; // Allow integers only
  var l, m, n = "This content", 3, "mixed types values"
  o, p := 7, 8
  q, r, s, t, u := 9, 10, "SS", "TT", 11
  
  var v [2]string
	v[0] = "Hello"
	v[1] = "World"
	
	fmt.Println(a[0], a[1])
	fmt.Println(a)
}
```

# Array Variables

```Go
package main

import (
	"fmt"
)

func main() {
	var a [4]int
	fmt.Println(a)

	b := [5]int{1, 2, 3, 4, 5}
	fmt.Println("dcl:", b)
	
	a[2] = 100 // index in position 2
	fmt.Println(a)
}
```

__Output__

```log
[0 0 0 0]

dcl: [1 2 3 4 5]

[0 0 100 0]
```



# Imprimiendo variables

```Go

package main

import (
	"fmt" // alias of `format`, this prints in console.
)

func main () {
  var a int;
  a = 10
  b := "Hello world" // automatic Type casting to string
  var c string;
  c = "custom_name_example"
  var d, e, f int; // Allow integers only
	d = 1
	e = 2
	f = 3
  var g, h, i int = 4, 5, 6; // Allow integers only
  var j, k, l = "This content", 3, "mixed types values"
  m , n, o, p := 7, 8, 9, 10
  q, r, s, t, u := 11, 12, "SS", "TT", 13

// Prints all vars value
	fmt.Println(a, b, c, d, e, f, g, h, i, j, k, l, m, n, o, p, q, r, s, t, u)
// Prints vars with custom format
  fmt.Printf("Hola %v! Cuenta del $%v al %v \n", c, d, f)
// Prints the var Type.  
  fmt.Printf("%T", b)
}
```

# Funciones

```Go
package main

import (
	"fmt" // alias of `format`, this prints in console.
)

func getAgeFrom(yearOfBirth int) int {
	return 2019 - yearOfBirth
}

func name(alias string) string {
	return fmt.Sprintf("%v's", alias)
}

func main () {
  name, yearOfBirth := "Daniel", 1989
  new_name, age := setName(name), getAgeFrom(yearOfBirth)
  fmt.Printf("Hi %v, you have %v years", new_name, age)
}
```

__Output__

> Hi Daniel, you have 30 years

> Program exited.

# Var Types personalizados & avanzados

```Go
package main

import (
	"fmt"
)

// Custom types
type dinero int

type point struct {
    x, y int
}


func main() {
	var d dinero
	d = 1500.00
	fmt.Printf("Hola! Tienes $%v MXN\n", d)
	fmt.Printf("%T", d)
	
	p := point{100, 5}
	fmt.Println(p, p.x, p.y)
}
```
__Output__
```log
> Hola! Tienes $1500 MXN
> main.dinero
> {1 2} 1 2
```

