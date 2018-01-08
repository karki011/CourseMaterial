# C# Statements

* [Scope](#scope)
* [Selection](#selection)
  * [If](#if)
  * [Else](#else)
* [Iteration](#iteration)
  * [While](#while)
  * [Do](#do)
  * [For](#for)
  * [Foreach](#foreach)

## Scope

Scope, also called a block, is defined with curly braces. This restricts the code to be visible only within the scope. You can think of scope as a parent-child relationship:

```cs
var hello = "Hello";

{
    // Child scope can access parent scope variables
    var message = hello + " World"; // This works
}

// You can access your `hello` variable, since you're in the same scope
Console.WriteLine(hello); // This works

// You cannot access the `message` variable, since it's in a child scope
Console.WriteLine(message); // This fails.
```

## Selection

Selection statements are all about choosing what to execute.

### If

The if statement evaluates a conditional, which must resolve to either `true` or `false`. Then, you provide the scope of your if statement, which executes if the conditional evaluates to `true`:

```cs
if (8 > 4) // 8 > 4 is your condition, which is true
{
    // your scope is executed when the conditional is true
}

if (4 > 8) // this resolves to false
{
    // so your scope is skipped over
}
```

### Else

The else statement is used in tandem with an if statement, providing scope for an if statement that resolves to `false`:

```cs
if (4 == 5) // your conditional is "if 4 equals 5", which is false
{
    // so your if scope is skipped over
}
else
{
    // your else scope will be executed
}
```

You can also chain if-else statements together:

```cs
var a = 4;
var b = 5;

if (a == b) // checked first
{
    // executes if a equals b
}
else if (a > b) // checked if the first conditional isn't true
{
    // executes if the a > b
}
else
{
    // executes if all if conditionals above are false
}
```

## Iteration

Iteration statements are all about executing something multiple times

### While

The while statement executes everything within scope until a condition is `false`. Use a while loop if you need to execute some code until something happens:

```cs
while (true)
{
    // do something here until condition is false
}
```

One thing to notice: the above code will execute indefinitely, since `true` will never be `false`. Let's look at a while loop that would be more beneficial. This while loop would execute the scope of the while loop 10 times:

```cs
var i = 0;

while (i < 10) { // Will execute as long as i < 10
    // Increment i each execution
    i++;
}
```

This loop will never execute, since `1` is not less than `1`:

```cs
var i = 1;

while (i < 1) { // Will execute as long as i < 1
    i++;
}
```

### Do

The do statement can be used in tandem with a while statement. Use a do-while loop if you need to execute some code at least once, then continue execution until something happens. This do-while loop would execute the scope of the loop 10 times:

```cs
var i = 0;
do
{
    // Increment i each execution
    i++;
} while (i < 10);
```

You can use a do-while loop to ensure that the scope is executed at least once. This do-while loop would execute the scope of the loop 1 time, then exit:

```cs
var i = 1;
do
{
    i++;
} while (i < 1);
```

### For

The for statement has lots of uses, but primarily it's somewhat of a bounded while statement. Use a for loop if you need to execute some code a specific number of times.

There are 3 parts to a for loop

* Initializer: runs once at the beginning
* Conditional: evaluates before each iteration
* Increment: increment code to execute during the loop
  * `++i` increments before each conditional check and scope execution
  * `i++` increments after each conditional check and scope execution

Below if a for loop that demonstrates the 3 parts:

* Initializer: `var i = 0`
* Conditional: `i < 10`
* Increment: `i++`

These parameters will execute the scope of the for loop 10 times:

```cs
for (var i = 0; i < 10; i++)
{
    // Execute some code
}
```

### Foreach

The foreach loop is used for iterating over a collection. The foreach loop is similar to a for loop. The syntax is easier to read and so is preferable in many scenarios when you have a collection. Use a foreach loop if you need to execute some code on each element in a collection of elements.

Below is a foreach loop that iterates of an array of 2 email addresses. These parameters execute the scope of the foreach loop 2 times, once for each email address:

```cs
var emails = new [] { "a@me.com", "b@me.com" };

foreach (var email in emails)
{
    //do something with the `email`, like send a marketing message
}
```

If we added a 3rd email address to the `emails` array, the foreach loop scope would execute 3 times.

**Previous:** [Operators](operators.markdown) |
**Next:** [Classes](classes.markdown)
