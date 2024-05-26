
# Go Syntax and Declarations

## 1. Packages and Imports
Every Go program starts with a package declaration, followed by necessary imports.

```go
package main

import "fmt"
```
- `package main`: Declares the package. A Go program must have a `main` package to be executable.
- `import "fmt"`: Imports the `fmt` package, which contains functions for formatting text, including printing to the console.

## 2. Functions
Functions are declared with the `func` keyword.

```go
func main() {
    fmt.Println("Hello, World!")
}
```
- `func main() { ... }`: Declares the main function, which is the entry point of a Go program.

## 3. Variables
Variables can be declared in several ways.

### Short Variable Declaration
```go
x := 42
```
- `x := 42`: Declares and initializes a variable `x` with the value `42`. The type of `x` is inferred.

### Standard Variable Declaration
```go
var y int
y = 42
```
- `var y int`: Declares a variable `y` of type `int`.
- `y = 42`: Assigns the value `42` to `y`.

### Multiple Variable Declaration
```go
var a, b, c int = 1, 2, 3
```
- `var a, b, c int = 1, 2, 3`: Declares three variables `a`, `b`, and `c` of type `int` and initializes them with values `1`, `2`, and `3`, respectively.

## 4. Constants
Constants are declared using the `const` keyword.

```go
const Pi = 3.14
```
- `const Pi = 3.14`: Declares a constant `Pi` with the value `3.14`.

## 5. Types
Go is a statically typed language, meaning each variable has a type, which is checked at compile time.

### Basic Types
```go
var i int
var f float64
var s string
var b bool
```
- `int`, `float64`, `string`, `bool` are basic types in Go.

## 6. Composite Types
Go has composite types such as arrays, slices, maps, and structs.

### Arrays
```go
var arr [5]int
```
- `var arr [5]int`: Declares an array of 5 integers.

### Slices
```go
var slc []int
slc = append(slc, 1, 2, 3)
```
- `var slc []int`: Declares a slice of integers.
- `slc = append(slc, 1, 2, 3)`: Appends values to the slice.

### Maps
```go
var m map[string]int
m = make(map[string]int)
m["one"] = 1
```
- `var m map[string]int`: Declares a map with string keys and integer values.
- `m = make(map[string]int)`: Initializes the map.
- `m["one"] = 1`: Assigns a value to a key in the map.

### Structs
```go
type Person struct {
    Name string
    Age  int
}

var p Person
p = Person{Name: "Alice", Age: 30}
```
- `type Person struct { ... }`: Defines a struct type `Person`.
- `var p Person`: Declares a variable `p` of type `Person`.
- `p = Person{Name: "Alice", Age: 30}`: Initializes the struct.

## 7. Control Structures
Go has standard control structures such as `if`, `for`, and `switch`.

### If Statements
```go
if x > 0 {
    fmt.Println("x is positive")
}
```

### For Loops
```go
for i := 0; i < 10; i++ {
    fmt.Println(i)
}
```

### Switch Statements
```go
switch x {
case 1:
    fmt.Println("one")
case 2:
    fmt.Println("two")
default:
    fmt.Println("other")
}
```

## 8. Pointers
Go supports pointers, which hold the memory address of a value.

```go
var p *int
i := 42
p = &i
fmt.Println(*p) // Prints 42
```
- `var p *int`: Declares a pointer to an integer.
- `p = &i`: Assigns the address of `i` to `p`.
- `*p`: Dereferences the pointer to get the value it points to.

These are the basic syntax and declarations in Go. Practice writing small programs to get comfortable with these concepts. Let me know if you need further clarification on any topic!
