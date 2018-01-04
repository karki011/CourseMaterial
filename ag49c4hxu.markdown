# C# Core

## Introduction

We're going to go over the fundamentals of programming with C#. Let's go over all the basics you'll need to get started.

As we go into details on C# (or any programming language), you'll find that documentation is your best friend for learning and improving your language skill set:

* [Microsoft's C# Documentation](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/)

### Source Code Comments

A comment is a programmer-readable explanation or annotation in the source code of a computer program. Anything within comments will be ignored by the compiler and are just there to help us programmers understand the code better.

* A single line comment is prepended with: `//`
* A multi-line comment is surrounded with: `/* */`

```cs
/* You'll use comments for documentation and explanation of your code.
 * Anytime you see comments, just know it's there for clarity.
 */

// This is a C# variable
var myVariable = "This will be compiled";
```

## Variables

### How They Work

Variables are a core concept of programming. Similar to variables in math, you use variables in programming to store values. This allows you to reference them later.

In C#, variables have a few different parts:

* Type: the variable's [type](#types)
* Name: a descriptive variable name
* Value: the variable's value

Below is a variable:

```cs
string myName = "Cody Winton";
```

* Type: `string`
* Name: `myName`
* Value: `"Cody Winton"`

Finally, the line of code is terminated with a semicolon: `;`.

### Strong and Static Typing

C# is a strongly, statically typed language, meaning that every variable has a type at compile time and you can't a variable's type after it has been set, though you can change its value.

#### Explicit Typing

C# allows for explicit typing of any variable. Let's see this in action as we define a few [String](#string) variables:

```cs
string aString = "This is a String";
string aVal = "Can be 123 or @ or # or any other characters!";
string line = Console.ReadLine(); // Returns a string typed by the user. More on this later.

aVal = "Modified string"; // The value of a variable can be changed

// This below would fail. 123 is not a string, since it is not surrounded by quotes
aVal = 123; // fails

// You can also set the value after creating the variable
string newVal;
newVal = "Testing new val";
```

#### Type Inference

C# also supports type inference, which means that you don't always have to explicitly specify a type. You can let the compiler try and understand the type of variable automatically.

The keyword `var` allows the compiler to infer type at compile time based on the provided value.

Let's see this in action as we define a few [String](#string) variables:




```cs
var aString = "This is a String";
var aVal = "Can be 123 or @ or # or any other characters!";

aVal = "Modified string"; // The value of a variable can be changed

// This below would fail. 123 is not a string, since it is not surrounded by quotes
aVal = 123; // fails
```

You **cannot** use the keyword `var` if you're not immediately setting the value of the variable:

```cs
var newVal; // This fails, since it cannot infer type. There is no provided value.
newVal = "Testing new val"; // You'll never reach this line of code
```

In C#, type inference is not required, but is considered "best practice".

## Types

### Value Types

A value type is set based on the provided value. Assigning one value type variable to another copies the contained value. This differs from the assignment of reference type variables, which copies a reference to the object but not the object itself.

#### Boolean

The Boolean type is defined with the keyword: `bool`. You can set the value be `true` or `false`:

```cs
bool isBoolean = true;
isBoolean = false;
```

#### Character

The Character type is defined with the keyword: `char`. You can set the value to any unicode character, surrounded by single quotes:

```cs
char myCharacter = 'a';
myCharacter = '@';
```

#### Integer

The Integer type is defined with the keyword: `int`. You can set the value to be any integer between `-2,147,483,648` to `2,147,483,647`:

```cs
int myInteger = 123;
myInteger = -456;
```

#### Decimal

The Decimal type is defined with the keyword: `decimal`. You can set the value to be any decimal within the range of `(-7.9 x 1028 to 7.9 x 1028) / 100 to 28` and followed by an `m`;

```cs
decimal myDecimal = 1234567890.234m;
myDecimal = -1234567890.234m;
```

#### Enum

An Enum type is a distinct type used when you want to limit the value set to a fixed amount of options. This allows for very readable code and a delightful autocomplete experience within Visual Studio.

```cs
// This enum defines every week day
enum Day { Sun, Mon, Tue, Wed, Thu, Fri, Sat };

// Can only be set to a day of the week
var dayOfWeek = Day.Tue;
dayOfWeek = Day.Wed;
```

#### Other Value Types

Although you won't run into these types quite as often as the four above, we wanted to list them:

* `byte`: an integer between `0` to `255`
* `double`: a decimal within the range of `(+/-)5.0 x 10-324to(+/-)1.7 x 10308`
* `float`: a decimal between `-3.4 x 1038` to `+3.4 x 1038`
* `long`: an integer between `-9,223,372,036,854,775,808` to `9,223,372,036,854,775,807`
* `sbyte`: an integer between `-128` to `127`
* `short`: an integer between `-32,768` to `32,767`
* `uint`: an integer between `0` to `4,294,967,295`
* `ulong`: an integer between `0` to `18,446,744,073,709,551,615`
* `ushort`: an integer between `0` to `65,535`

### Null and Nullables

In C#, the keyword `null` represents the absence of value.

While [reference types](#reference-types) automacially support being set to `null`, value types require an actual value. When you need to assign `null` to a value type, you employ the "nullable" of that type. A value type, followed by a `?` is shorthand syntax for nullable:

```cs
// Here's a nullable boolean value
bool? isBoolean = true;
isBoolean = null;

// You can do the same for other value types
int? myInteger = null;
myInteger = 0;

// Reference types support null automatically
string myString = "Hello World";
myString = null;
```

As a note around numbers: `0` is not the same as `null`:

* `0` is a legitimate number value, stored in memory or to disk as `0`
* `null` represents the absence of value: nothing is stored in memory or to disk

### Reference Types

A reference type is set by storing the actual data (object) in memory and storing a reference to the object within the variable. Reference types in C# automatically support being set null.

#### String

A String is a sequence of zero or more unicode characters, surrounded by double quotes

You can concatenate strings with the `+` symbol:

```cs
var message = "What's " + "up?";
```