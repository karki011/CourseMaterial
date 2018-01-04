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

### Reference Types

A reference type is set by storing the actual data (object) in memory and storing a reference to the object within the variable. Reference types in C# automatically support being set null.

#### String

A String is a sequence of zero or more unicode characters, surrounded by double quotes

You can concatenate strings with the `+` symbol:

```cs
var message = "What's " + "up?";
```