# Java Classes

* [Fundamentals](#fundamentals)
* [Instances](#instances)
* [Class Methods and Variables](#class-methods-and-variables)
* [Inheritance](#inheritance)
* [Constructor](#constructor)

## Fundamentals

A class is a construct that enables the creation of custom types by grouping together variables of other types, as well as custom methods and/or events. A class is like a blueprint or a cookie cutter. It defines the data and behavior of a type.

Like variables and methods, classes have a few basic parts:

* Modifiers: an optional list of keywords that give certain qualities to the class
* Keyword `class`: required to define a class
* Name: a descriptive class name
* Scope: the scope of the class definition
  * Variables: class or instance variables associated with the class
  * Methods: class or instance methods associated with the class

Here, we have defined a class called `Animal`:

```java
public class Animal
{
    // We'll define a variable of type string called `name`
    public String name;

    // We'll define a method called `sayName`
    public void sayName()
    {
        // Use `this` to reference the current Animal instance
        System.out.println("My name is " + this.name);

        // The code can also infer that you're accessing `this`
        System.out.println("My name is " + name);
    }
}
```

## Instances

If a class is like a cookie cutter, an "instance" of that class is like an actual cut-out cookie. The below code creates a new instance of the `Animal` class:

```java
Animal animal = new Animal();
animal.name = "Fido"; // animal.name equals "Fido"
String name = animal.name; // `name` equals "Fido"

// Calling the sayName method will execute the sayName code
animal.sayName(); // Writes "My name is Fido" to the console
```

## Class Methods and Variables

Within the class scope, a class can contain variables and methods that have the `static` modifier, meaning that the variable or method is associated with the class itself, not an instance of the class.

If we think of a class as a cookie cutter, and an instance of the class as a cookie, a `static` method is a method that belongs to the cookie cutter, not the cookie.

```java
public class Animal
{
    public static int numberOfAnimals;
    public String name;

    public static void listAllAnimals()
    {
        System.out.println(numberOfAnimals + " animals");
    }

    public void sayName()
    {
        System.out.println("My name is " + name);
    }
}
```

Later in code, you can call your class variables and methods on the `Animal` class:

```java
int animalCount = Animal.numberOfAnimals;
Animal.listAllAnimals();
```

## Inheritance

A class can also be a subclass of another class and "inherit" some of the parent class's functionality. In Object Oriented Programming (OOP), we call this Inheritance. A class can only inherit from one parent class:

```java
public class Animal
{
    public String name;

    public void sayName()
    {
        System.out.println("My name is " + name);
    }
}

// The Dog class is a child class of the parent Animal class
public class Dog extends Animal
{

}
```

This instance of the Dog class has all the functionality of an instance of the Animal class:

```java
Dog dog = new Dog();
dog.name = "Fido";
dog.sayName();
```

## Constructor

A constructor allows you to assign property values when you create the instance of a class. This makes code cleaner and allows us to ensure that every value is properly set at the time of initialization.

In addition, you can also execute other necessary "setup" code at the time of constructing an instance:

```java
public class Animal
{
    public String name;

    // Default, standard constructor
    public Animal()
    {
        // Handle some default execution
        this("Fido") // call the constructor below
    }

    // Specific constructor, called above as well
    public Animal(string name)
    {
        this.name = name;
    }
}
```

Later in your code:

```java
Animal aAnimal = new Animal(); // created with name equal to the default "Fido"
Animal bAnimal = new Animal("Fluffy"); // created with name equal to "Fluffy"
```

**Previous:** [Statements](statements.markdown) |
**Next:** [Interfaces](interfaces.markdown)
