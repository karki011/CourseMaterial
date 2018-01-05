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