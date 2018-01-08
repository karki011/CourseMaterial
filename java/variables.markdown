# Java Variables

* [Fundamentals](#fundamentals)
* [Strong and Static Typing](#strong-and-static-typing)

## Fundamentals

Variables, sometimes called properties, are a core concept of programming. Similar to variables in math, you use variables in programming to store values. This allows you to reference them later.

In Java, variables have a few different parts:

* Type: the variable's [type](types.markdown)
* Name: a descriptive variable name
* Value: the variable's value

Below is a variable:

```java
String myName = "Cody Winton";
```

* Type: `String`
* Name: `myName`
* Value: `"Cody Winton"`

Finally, the line of code is terminated with a semicolon: `;`.

## Strong and Static Typing

Java is a strongly, statically typed language, meaning that every variable has a type at compile time and you can't a variable's type after it has been set, though you can change its value.

Java requires explicit typing for any variable. Let's see this in action as we define a few [String](types.markdown#string) variables:

```java
String aString = "This is a String";
String aVal = "Can be 123 or @ or # or any other characters!";

aVal = "Modified string"; // The value of a variable can be changed

// This below would fail. 123 is not a string, since it is not surrounded by quotes
aVal = 123; // fails

// You can also set the value after creating the variable
String newVal;
newVal = "Testing new val";
```

**Next:** [Types](types.markdown)
