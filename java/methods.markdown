# Java Methods

A method, sometimes called a function, is a block of code that contains a collection of code to execute. You can execute this code by calling the method. In Java, a method consists of a few things:

* Modifiers: an optional list of keywords that give certain qualities to the method
* Return Type: the [type](types.markdown) returned by the method, or `void` when not returning anything
* Name: a descriptive method name
* Parameters: an optional list of parameters to be passed into the method

## Modifiers and Return Types

Here's a `public` method with a `void` return type.

The modifier is `public`, meaning any place in the code can call your method. It's not `private` or `protected`.

The return type is `void`. You can think of `void` as similar to `null`. It's a keyword that represents the absence of a return type.

```java
public void myMethod()
{
    // Code to execute goes here when myMethod() is called
    // Return type is void, so no need to return anything
}
```

Here's a `public` method with a `String` return type:

```java
public String myMessage()
{
    // Code to execute goes here when myMessage() is called
    // Return type is string, so we must return a string
    return "This is the message";
}
```

Later in your code, you can call your methods:

```java
myMethod(); // executes any code in your myMethod() method

String message = myMessage(); // executes any code in myMessage() and returns a String
```

## Parameters

Below, we have a method called `SendEmail`. The return type is `boolean`, in this case, if the email sent with success. The method has one parameter: `String emailAddress`.

```java
public boolean sendEmail(String emailAddress)
{
    if (emailAddress.equals("cwinton@truecoders.io"))
    {
        // Send the email and return true, for success
        return true;
    }
    else
    {
        // Don't send the email and return false, for failure
        return false;
    }
}
```

Later in your code, you can call your methods:

```java
boolean didSendFirst = sendEmail("cwinton@truecoders.io"); // This call will return true

boolean didSendSecond = sendEmail("dwalsh@truecoders.io"); // This call will return false
```

**Previous:** [Types](types.markdown) |
**Next:** [Operators](operators.markdown)
