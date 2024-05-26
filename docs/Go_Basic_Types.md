
# Go Basic Types

## Numeric Types

### 1. Integer Types
**Signed Integers:**
- `int`: The default integer type, which is either 32 or 64 bits depending on the platform.
- `int8`: 8-bit signed integer (range: -128 to 127)
- `int16`: 16-bit signed integer (range: -32768 to 32767)
- `int32`: 32-bit signed integer (range: -2147483648 to 2147483647)
- `int64`: 64-bit signed integer (range: -9223372036854775808 to 9223372036854775807)

**Unsigned Integers:**
- `uint`: The default unsigned integer type, which is either 32 or 64 bits depending on the platform.
- `uint8`: 8-bit unsigned integer (range: 0 to 255, same as `byte`)
- `uint16`: 16-bit unsigned integer (range: 0 to 65535)
- `uint32`: 32-bit unsigned integer (range: 0 to 4294967295)
- `uint64`: 64-bit unsigned integer (range: 0 to 18446744073709551615)

**Special Unsigned Integers:**
- `uintptr`: An unsigned integer large enough to store the uninterpreted bits of a pointer value.

### 2. Floating-Point Types
- `float32`: 32-bit IEEE-754 floating-point number
- `float64`: 64-bit IEEE-754 floating-point number (the default floating-point type)

### 3. Complex Types
- `complex64`: Complex numbers with float32 real and imaginary parts
- `complex128`: Complex numbers with float64 real and imaginary parts (the default complex type)

## String Type
- `string`: A string is a sequence of bytes. Strings are immutable in Go, meaning once created, they cannot be changed. Strings are enclosed in double quotes (`"`).

## Boolean Type
- `bool`: Represents a boolean value, which can be either `true` or `false`.

## Rune Type
- `rune`: An alias for `int32`, represents a Unicode code point. Useful when dealing with individual characters.

## Byte Type
- `byte`: An alias for `uint8`, typically used to emphasize that the value is a raw byte of data.

## Zero Values
Each type has a zero value that is assigned when variables are declared without an explicit initialization. Here are the zero values for basic types:
- Numeric types: `0`
- Boolean type: `false`
- String type: `""` (empty string)

## Examples

Here are some examples of using these types in Go:

\`\`\`go
package main

import "fmt"

func main() {
    // Integer types
    var i int = 42
    var ui uint = 42
    var i8 int8 = 127
    var ui8 uint8 = 255

    // Floating-point types
    var f32 float32 = 3.14
    var f64 float64 = 3.141592653589793

    // Complex types
    var c64 complex64 = 1 + 2i
    var c128 complex128 = 1 + 2i

    // String type
    var s string = "Hello, Go!"

    // Boolean type
    var b bool = true

    // Rune type
    var r rune = 'a' // Unicode code point for 'a'

    // Byte type
    var by byte = 255

    fmt.Println(i, ui, i8, ui8)
    fmt.Println(f32, f64)
    fmt.Println(c64, c128)
    fmt.Println(s)
    fmt.Println(b)
    fmt.Println(r)
    fmt.Println(by)
}
\`\`\`

## Type Conversion
Go is strongly typed, so you often need to explicitly convert between types. Here’s an example:

\`\`\`go
package main

import "fmt"

func main() {
    var x int = 42
    var y float64 = float64(x) // convert int to float64
    var z uint = uint(y)       // convert float64 to uint

    fmt.Println(x, y, z)
}
\`\`\`

Understanding these basic types is essential as they form the foundation for more complex data structures and algorithms in Go. If you have any questions or need further details on any specific type, feel free to ask!
