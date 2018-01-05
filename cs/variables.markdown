# C# Variables

Variables, sometimes called properties, are a core concept of programming. Similar to variables in math, you use variables in programming to store values. This allows you to reference them later.

In C#, variables have a few different parts:

* Type: the variable's [type](types.markdown)
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

## Strong and Static Typing

C# is a strongly, statically typed language, meaning that every variable has a type at compile time and you can't a variable's type after it has been set, though you can change its value.

### Explicit Typing

C# allows for explicit typing of any variable. Let's see this in action as we define a few [String](types.markdown#string) variables:

```cs
string aString = "This is a String";
string aVal = "Can be 123 or @ or # or any other characters!";

aVal = "Modified string"; // The value of a variable can be changed

// This below would fail. 123 is not a string, since it is not surrounded by quotes
aVal = 123; // fails

// You can also set the value after creating the variable
string newVal;
newVal = "Testing new val";
```

### Type Inference

C# also supports type inference, which means that you don't always have to explicitly specify a type. You can let the compiler try and understand the type of variable automatically.

The keyword `var` allows the compiler to infer type at compile time based on the provided value:

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

**Next:** [Types](types.markdown)
