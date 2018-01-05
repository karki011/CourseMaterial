# Java Types

Java Types tend to fall into 2 categories:

* Primitive Types
* Reference Types

## Primitive Types

A primitive type is set based on the provided value. Assigning one primitive type variable to another copies the contained value. This differs from the assignment of reference type variables, which copies a reference to the object but not the object itself.

In Java, there are 8 primitive types:

### Boolean

The Boolean type is defined with the keyword: `boolean`. You can set the value be `true` or `false`:

```java
boolean isBool = true;
isBool = false;
```

### Character

The Character type is defined with the keyword: `char`. You can set the value to any unicode character, surrounded by single quotes:

```java
char myChar = 'a';
myChar = '@';
```

### Byte

The Byte type is defined with the keyword: `byte`. You can set the value to be any integer between `-128` to `127`:

```java
byte myByte = 123;
myByte = -37;
```

### Short

The Short type is defined with the keyword: `short`. You can set the value to be any integer between `-32768` to `32767`:

```java
short myShort = 1423;
myShort = -3787;
```

### Integer

The Integer type is defined with the keyword: `int`. You can set the value to be any integer between `-2,147,483,648` to `2,147,483,647`:

```java
int myInteger = 123;
myInteger = -456;
```

### Long

The Long type is defined with the keyword: `long`. You can set the value to be any integer between `-9,223,372,036,854,775,808` to `9,223,372,036,854,775,807` and appended with an `L`:

```java
long myLong = 9223372036854775807L;
myLong = -223372036854777L;
```

### Float

The Float type is defined with the keyword: `float`. You can set the value to be a decimal number with around 7-digits of precision and appended with an `f`:

```java
float myFloat = 123.23f;
myFloat = -45.24743f;
```

### Double

The Double type is defined with the keyword: `double`. You can set the value to be a decimal number with around 15-digits of precision:

```java
double myDouble = 123.223;
myDouble = -45.24743245909;
```

## Null and Nullables

In Java, the keyword `null` represents the absence of value.

While [reference types](#reference-types) automacially support being set to `null`, primitive types require an actual value. When you need to assign `null` to a primitive type, you employ a reference "wrapper" class for that type:

```java
// Here's a reference wrapper class for the boolean type
Boolean isBoolean = true;
isBoolean = null;

// You can do the same for other primitive types
Integer myInteger = null;
myInteger = 0;

// Reference types support null automatically
String myString = "Hello World";
myString = null;
```

As a note about `null`: `0` is not the same as `null`:

* `0` is an actual number value, stored in memory or to disk as `0`
* `null` represents the absence of value: nothing is stored in memory or to disk

## Reference Types

A reference type is set by storing the actual data (object) in memory and storing a reference to the object within the variable. Reference types in Java automatically support being set `null`.

### String

A String is a sequence of zero or more unicode characters, surrounded by double quotes.

```java
String myString = "Hello World!";
```

You can concatenate strings with the `+` symbol:

```java
String message = "What's " + "up?"; // message == "What's up?"
```

You can split a single string into an [array](#array) of strings:

```java
String aString = "1,2,3"; // the string to split
String separator = ","; // ","

// This splits `aString` using a separator `String` value
String[] numbers = aString.Split(separator); // numbers == { "1", "2", "3" };
```

### Array

Arrays allow you to combine multiple variables of the same type in a single variable. You declare an array type by specifying the type, followed by double square brackets `type[]`.

```java
// We've created an array that can hold up to 5 ints
int[] ints = new int[5];

// You can also use type inference when you provide the variables for the array to contain
int[] intsLiteral = new [] { 7, 58, 5 }; // Array with set values using curly bracket notation
```

Arrays are zero-based index, meaning that the first value is stored at index `0`. You can access a value using its index, along with square bracket notation.

```java
int[] intsLiteral = new [] { 7, 58, 5 };

int firstNumber = intsLiteral[0]; // Equals 7
int secondNumber = intsLiteral[1]; // Equals 58

intsLiteral[2] = 10; // Did change 5 to 10
```

You can join an array of [strings](#strings) into a single string:

```java
String[] numbers = new [] { "1", "2", "3" }; // the array to join
String allNums = String.join(",", numbers); // allNums == "1,2,3"
```

### Enum

An Enum type is a distinct type used when you want to limit the value set to a fixed amount of options. This allows for very readable code and a delightful autocomplete experience within Eclipse.

```cs
// This enum defines every week day
public enum Day { SUN, MON, TUE, WED, THU, FRI, SAT }

// Can only be set to a day of the week
Day dayOfWeek = Day.TUE;
dayOfWeek = Day.WED;
```

## Reference Types vs. Primitive Types

With a primitive type, when you copy a variable you create a clone of the actual value.

Let's see how this works with an [int](#integer)

```java
int a = 1; // primitive type int
int b = a; // clone the value of `a`

a = 2; // Change the contained value of `a`

// Now a == 2 && b == 1
```

With a reference type, when you copy a variable you create a clone of the reference to the same actual data value:

Let's see how this works with a [class](classes.markdown#classes) called `Animal`.

```java
Animal c = new Animal("Fido"); // reference type Animal
Animal d = c; // copy of reference to same object

// currently c.Name == "Fido" && d.Name == "Fido", but let's change that:
c.Name = "Fluffy";

// You changed the property of the actual object
// So now c.Name == "Fluffy" && d.Name == "Fluffy"
```

**Previous:** [Variables](variables.markdown)
