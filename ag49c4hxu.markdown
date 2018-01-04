# C# Core

## Introduction

We're going to go over the fundamentals of programming with C#. Let's go over all the basics you'll need to get started.

As we go into details on C# (or any programming language), you'll find that documentation is your best friend for learning and improving your language skill set:

* Microsoft's [C# Documentation](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/)

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

## Types and Variables

### Variables

Variables are a core concept of programming. Similar to variables in math, you use variables in programming to store values. This allows you to reference them later.

In C#, variables have a few different parts:

* Type: the variable’s type
* Name: a descriptive variable name
* Value: the variable’s value

Below is a variable:

* Type: `string`
* Name: `myName`
* Value: `"Cody Winton"`

Finally, the line of code is terminated with a `;`.

```cs
string myName = "Cody Winton";
```