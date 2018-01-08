# Java Operators

* [Math Operators](#math-operators)
* [Logic Operators](#logic-operators)

## Math Operators

Programming is heavily based in math. You can easily handle math operations in programming.

Normal add, subtract, multiply, and divide operators are supported:

```java
int a = 8;
int b = 4;

int add = a + b; // Equals 12
int subtract = a - b; // Equals 4
int multiply = a * b; // Equals 32
int divide = a / b; // Equals 2
```

Modulus operator returns the remainder after a division:

```java
int modulus = 4 % 2; // Equals 0
int oddModulus = 3 % 2; // Equals 1
```

Modifying operators:

```java
int a = 8;

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

```java
boolean isTrue = 4 == 4; // true
boolean isFalse = 4 == 8; // false
```

In Java, an exlaimation mark, as known as a bang, generally stands for "Not". Bang + equal sign `!=` is the operator for "Is Not Equal":

```java
boolean isTrue = 4 != 8; // true
boolean isTrue = "hello" != "world"; // also true
boolean isFalse = 4 != 4; // false
```

Other comparisons are available, written as normal in regular mathmatics:

```java
boolean isGreaterThan = 8 > 4; // 8 is greater than 4
boolean isGreaterThanOrEqualTo = 8 >= 4; // 8 is greater than or equal to 4

boolean isLessThan = 4 < 8; // 4 is less than 8
boolean isLessThanOrEqualTo = 4 <= 8; // 4 is less than or equal to 8
```

## Logic Operators

Programming is also based in logic. You can easily handle logic operations in programming. Sometimes we need to use the concepts of "And", "Or", and "Not".

Double ampersand `&&` is the operator for Logical "And". "And" only resolves to `true` if all conditionals being evaluated are true. Otherwise, it resolves to `false`:

```java
boolean aBool = 12 != 6 && 8 == 8; // aBool equals true
boolean bBool = 12 > 8 && 8 > 80; // bBool equals false
```

Double pipes `||` is the operator for Logical "Or". "Or" only resolves to `false` if all conditionals being evaluated are false. Otherwise, it resolves to `true`:

```java
boolean aBool = 8 > 80 || 4 < 8; // aBool equals true
boolean bBool = 6 == 7 || false; // bBool equals false
```

Exclaimation mark `!`, also called bang, is the operator for Logical "Not". "Not" reverses a boolean, so `!true == false`:

```java
boolean aBool = !false; // aBool equals true
boolean bBool = !true; // bBool equals false
```

**Previous:** [Methods](methods.markdown) |
**Next:** [Statements](statements.markdown)
