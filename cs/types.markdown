# C# Types

C# Types tend to fall into 2 categories:

* Value Types
* Reference Types

## Value Types

A value type is set based on the provided value. Assigning one value type variable to another copies the contained value. This differs from the assignment of reference type variables, which copies a reference to the object but not the object itself.

### Boolean

The Boolean type is defined with the keyword: `bool`. You can set the value be `true` or `false`:

```cs
bool isBoolean = true;
isBoolean = false;
```

### Character

The Character type is defined with the keyword: `char`. You can set the value to any unicode character, surrounded by single quotes:

```cs
char myCharacter = 'a';
myCharacter = '@';
```

### Integer

The Integer type is defined with the keyword: `int`. You can set the value to be any integer between `-2,147,483,648` to `2,147,483,647`:

```cs
int myInteger = 123;
myInteger = -456;
```

### Decimal

The Decimal type is defined with the keyword: `decimal`. You can set the value to be any decimal within the range of `(-7.9 x 1028 to 7.9 x 1028) / 100 to 28` and followed by an `m`;

```cs
decimal myDecimal = 1234567890.234m;
myDecimal = -1234567890.234m;
```

### Enum

An Enum type is a distinct type used when you want to limit the value set to a fixed amount of options. This allows for very readable code and a delightful autocomplete experience within Visual Studio.

```cs
// This enum defines every week day
enum Day { Sun, Mon, Tue, Wed, Thu, Fri, Sat };

// Can only be set to a day of the week
var dayOfWeek = Day.Tue;
dayOfWeek = Day.Wed;
```

### Other Value Types

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

## Null and Nullables

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

## Reference Types

A reference type is set by storing the actual data (object) in memory and storing a reference to the object within the variable. Reference types in C# automatically support being set `null`.

### String

A String is a sequence of zero or more unicode characters, surrounded by double quotes.

```cs
var myString = "Hello World!";

// You can concatenate strings with the `+` symbol
var message = "What's " + "up?"; // message == "What's up?"
```

### Arrays

Arrays allow you to combine multiple variables of the same type in a single variable. You declare an array type by specifying the type, followed by double square brackets `type[]`.

```cs
// We've created an array that can hold up to 5 ints
int[] ints = new int[5];

// You can also use type inference when you provide the variables for the array to contain
var intsLiteral = new [] { 7, 58, 5 }; // Array with set values using curly bracket notation
```

Arrays are zero-based index, meaning that the first value is stored at index `0`. You can access a value using its index, along with square bracket notation.

```cs
var intsLiteral = new [] { 7, 58, 5 };

int firstNumber = intsLiteral[0]; // Equals 7
int secondNumber = intsLiteral[1]; // Equals 58

intsLiteral[2] = 10; // Did change 5 to 10
```

**Previous:** [Variables](variables.markdown) |
**Next:** [Methods](methods.markdown)