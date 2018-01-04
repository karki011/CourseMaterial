# C# Operators

Operators are all about handling and manipulating data.

## Math Operators

Programming is heavily based in math. You can easily handle math operations in programming.

Normal add, subtract, multiply, and divide operators are supported:

```cs
var a = 8;
var b = 4;

var add = a + b; // Equals 12
var subtract = a - b; // Equals 4
var multiply = a * b; // Equals 32
var divide = a / b; // Equals 2
```

Modulus operator returns the remainder after a division:

```cs
var modulus = 4 % 2; // Equals 0
var oddModulus = 3 % 2; // Equals 1
```

Modifying operators:

```cs
var a = 8;

a += 4; // same as a = a + 4;
a -= 4; // same as a = a - 4;
a *= 4; // same as a = a * 4;
a /= 4; // same as a = a / 4;

// Increment and Decrement
a++; // same as a = a + 1;
a--; // same as a = a - 1;
```

Comparison operators are available for comparing values.

Double equal signs `==` is the operator for "Is Equal":

```cs
var isTrue = 4 == 4; // true
var isFalse = 4 == 8; // false
```

In C#, an exlaimation mark, as known as a bang, generally stands for "Not". Bang + equal sign `!=` is the operator for "Is Not Equal":

```cs
var isTrue = 4 != 8; // true
var isFalse = 4 != 4; // false
```

Other comparisons are available, written as normal in regular mathmatics:

```cs
var isGreaterThan = 8 > 4; // 8 is greater than 4
var isGreaterThanOrEqualTo = 8 >= 4; // 8 is greater than or equal to 4

var isLessThan = 4 < 8; // 4 is less than 8
var isLessThanOrEqualTo = 4 <= 8; // 4 is less than or equal to 8
```

## Logic Operators

Programming is also based in logic. You can easily handle logic operations in programming. Sometimes we need to use the concepts of "And", "Or", and "Not".

`&&`: Logical "And":

```cs
var aBool = true && 8 == 8; // aBool == true
var bBool = 12 > 8 && 8 > 80; // bBool == false
```

`||`: Logical "Or":

```cs
var aBool = 8 > 80 || 4 < 8; // aBool == true
var bBool = 6 == 7 || false; // bBool == false
```

`!`: Logical "Not":

```cs
var aBool = !false; // aBool == true
var bBool = !true; // bBool == false
```

**Previous:** [Methods](methods.markdown) |
**Next:** [Statements](statements.markdown)