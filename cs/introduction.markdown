# C# Introduction

We're going to go over the fundamentals of programming with C#. Let's go over all the basics you'll need to get started.

As we go into details on C# (or any programming language), you'll find that documentation is your best friend for learning and improving your language skill set:

* [Microsoft's C# Documentation](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/)

## Source Code Comments

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

## Output

When working with C#, at times you'll want to "output" something to for your user or yourself. You can accomplish this with:

```cs
// Write a message to the console
Console.WriteLine("Message to write out");
```

Also, at times, you'll want to read something the user typed in. You can accomplish this with:

```cs
// This is a message typed by the user
var message = Console.ReadLine();
```

Don't worry if this doesn't make total sense yet. We'll get there.

**Next:** [Variables](variables.markdown)