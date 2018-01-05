# Java Interfaces

An Interface is like a blueprint. It defines some data and functionality that should exist within a type that implements the interface. An interface does not care about the implementation. It merely requires that it is implemented.

## Interfaces

Here's an example interface:

```java
public interface SampleInterface
{
    void sampleMethod();
}

interface OtherInterface
{
    String otherMethod();
}
```

Unlike inheritance, a class can conform to multiple interfaces:

```java
class SampleClass : SampleInterface, OtherInterface
{
    // SampleInterface member implementation
    void sampleMethod()
    {
        // Method implementation
    }

    // OtherInterface member implementation
    String otherMethod()
    {
        // Other implementation
        return "Message";
    }
}
```

Later in code, you can create an instance of the `SampleClass` as an instance of the `SampleInterface`:

```java
SampleInterface sample = new SampleClass();
sample.sampleMethod();
```

You can also have an interface inherit from another interface.

Let's create a Hawk class and a Penguin class. Both are animals. Both are birds, even. But, only one can fly.

Using Interfaces, we can accomplish this functionality is a clear, concise, and readable way:

```java
class Animal {}

public interface Bird // For all birds
{
    void cleanFeathers();
}

public interface FlyingBird extends Bird // For all flying birds
{
    void fly();
}

class Hawk extends Animal, FlyingBird
{
    public void cleanFeathers() {}
    public void fly() {}
}

class Penguin extends Animal, Bird
{
    public void cleanFeathers() {}
}
```

Let's look at an example that shows the benefit of interchangeable code using Interfaces. We'll use the `Bird` interface with a method:

```java
public void cleanBird(Bird bird)
{
    bird.cleanFeathers();
}
```

Later, we can create an instance of the `Hawk` class and the `Penguin` class. Both of these instances are different types, but both implement the `Bird` interface:

```java
Hawk hawk = new Hawk();
cleanBird(hawk); // this works

Penguin penguin = new Penguin();
cleanBird(penguin); // this also works
```

We've created a method that accepts any bird in a type-safe fashion.

**Previous:** [Classes](classes.markdown) |
**Next:** [Syntax](syntax.markdown)
