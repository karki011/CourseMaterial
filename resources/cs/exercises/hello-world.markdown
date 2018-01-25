# C# Exercise: Hello World

* [Introduction](#introduction)
* [Create a Project](#create-a-project)
* [Build and Run](#build-and-run)
  * [C# Compiler](#c-compiler)
  * [MSBuild](#msbuild)
  * [Visual Studio IDE](#visual-studio-ide)

## Introduction

Welcome to your first introduction to programming in this course! We're excited you're here.

Throughout this course, we hope to challenge you to think outside the box, to learn quickly, and to collaborate well with others.

Programming is an amazing skill, and, by the end of this course, we hope to see you equipped with all the skills necessary to be a TrueCoder.

We're going to be teaching you to learn C# and .NET within this course. So, first things first. Let's get our **Hello World** app up and running... Because we might get struck by lightning if we did anything else.

## Create a Project

Create the Hello World application using Visual Studio. Select **"Create new project"** and you'll see the New Project options:

* Select the **"Console App (.NET Framework)"** from the Visual C# project templates
* Set the Name: **"HelloWorld"**
* Select: **"Create new Git repository"** (also might be **"Add to Source Control"**)
* Leave everything else the same and select **OK**

In the created project, you'll see code that looks like this:

```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace HelloWorld
{
    class Program
    {
        static void Main(string[] args)
        {
        }
    }
}
```

We're going to add some code to our `Main` method:

```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace HelloWorld
{
    class Program
    {
        static void Main(string[] args)
        {
            // Add code here:
            Console.WriteLine("Hello World");
            Console.ReadLine();
        }
    }
}
```

## Build and Run

There are several ways to build and run your application. We're going to go over the different ways to do so:

### C# Compiler

Your app, at its core, will be built with the C# Compiler (`csc`), and we'll show you how to access it directly.

* Minimize Visual Studio and open the Developer Command Prompt for Visual Studio
* `cd` into the directory of your project
* Run: `csc HelloWorld/Program.cs` in the Command Prompt
* Double click the `Program.exe` file

You'll see `Hello World` print out on your screen

### MSBuild

The Microsoft Build Engine (`MSBuild`) is the build platform for .NET and Visual Studio. `MSBuild` is the build platform for .NET and Visual Studio:

* Run in the Command Prompt: `msbuild HelloWorld.sln`
* Find the location of the `.exe` file in the build results
* Open the `Program.exe` file

You'll see `Hello World` print out on your screen

### Visual Studio IDE

Our C# Editor & Integrated Development Environment (IDE) of Choice

We're glad that you now know how to run your app with just the Command Prompt. However, Visual Studio makes everything a whole lot easier:

* Click Run
* That's it

You'll see `Hello World` print out on your screen
