# Java Methods

A method is a block of code that contains a collection of code to execute. You can execute this code by calling the method. In Java, a method consists of a few things:

* Modifiers: an optional list of keywords that give certain qualities to the method
* Return Type: the [type](types.markdown) returned by the method, or `void` when not returning anything
* Name: a descriptive method name
* Parameters: an optional list of parameters to be passed into the method

## Modifiers and Return Types

Here's a `public` method with a `void` return type.

The modifier is `public`, meaning any place in the code can call your method. It's not `private` or `protected`.

The return type is `void`. You can think of `void` as similar to `null`. It's a keyword that represents the absence of a return type.

```java
public void MyMethod()
{
    // Code to execute goes here when MyMethod() is called
    // Return type is void, so no need to return anything
}
```

Here's a `public` method with a `String` return type:

```java
public String MyMessage()
{
    // Code to execute goes here when MyMessage() is called
    // Return type is string, so we must return a string
    return "This is the message";
}
```

Later in your code, you can call your methods:

```java
MyMethod(); // executes any code in your MyMethod() method

String message = MyMessage(); // executes any code in MyMessage() and returns a String
```
