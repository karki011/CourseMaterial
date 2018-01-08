# TrueCoders Course Materials

* [Course Languages](#course-languages)
* [Documentation & Resources](#documentation-resources)
  * [C# Resources](#c-resources)
  * [Java Resources](#java-resources)
  * [Additional Resources](#additional-resources)
* [Source Code Comments](#source-code-comments)
  * [Line Comment](#line-comment)
  * [Block Comment](#block-comment)
* [Output](#output)
  * [C# Output](#c-output)
  * [Java Output](#java-output)
* [Tools](#tools)
* [Acronyms](#acronyms)
* [CRUD Definitions](#crud-definitions)

## Course Languages

* [C# Material Start](cs/variables.markdown)
* [Java Material Start](java/variables.markdown)

We're going to go over the fundamentals of programming. But, before you dive in, let's go over all the basics you'll need to get started.

## Documentation & Resources

As we go into details of any programming language, you'll find that documentation is your best friend for learning and improving your language skill set:

### C# Resources

* [C# Microsoft Walkthrough](https://msdn.microsoft.com/en-us/library/jj153219.aspx)
* [C# Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/csharp/)

### Java Resources

* [Java Oracle Docs](https://docs.oracle.com/javase/9/)

### Additional Resources

* [Git Docs](https://git-scm.com/doc)
* [Linus Torvalds on Git](https://youtu.be/4XpnKHJAok8)
* [Markdown Docs](https://daringfireball.net/projects/markdown/syntax/)
* [Semantic Versioning](http://semver.org)

## Source Code Comments

A comment is a programmer-readable explanation or annotation in the source code of a computer program. Anything within comments will be ignored by a compiler and are just there to help us programmers understand the code better.

You'll use comments for documentation and explanation of your code. Anytime you see comments, just know it's there for clarity.

### Line Comment

Also known as single-line comment, line comment syntax for C# and Java is prepended with `//`

```cs
// Example line comment
```

### Block Comment

Also known as multi-line comment, block comment syntax for C# and Java is surrounded with `/* */`. Also, though not required, this block comment syntax usually contains a `*` at the beginning of each new line.

```cs
/* Example
 * block
 * comment
 */
```

## Output

When working with programming languages, at times you'll want to output something for your user or yourself. Also, at times, you'll want to read user input. In most languages, this is made available. Don't worry if this doesn't make total sense yet. We'll get there.

### C# Output

```cs
// Write a message to the console
Console.WriteLine("Message to write out");
```

Output:

```
Message to write out
```

### Java Output

```java
// Write a message to the console
System.out.println("Message to write out");
```

Output:

```
Message to write out
```

## Tools

| Name                                                                                | Install | Notes                                                 |
| ----------------------------------------------------------------------------------- | ------- | ----------------------------------------------------- |
| VirtualBox                                                                          | Mac     |                                                       |
| [Git](https://git-scm.com)                                                          | Windows |                                                       |
| Visual Studio Community Edition                                                     | Windows | Install with .NET Desktop, .NET Core, and ASP.NET MVC |
| ReSharper                                                                           | Windows |                                                       |
| Git Extensions                                                                      | Windows |                                                       |
| SourceTree                                                                          | Windows |                                                       |
| Visual Studio Code                                                                  | Windows | Lightweight Code Editor                               |
| Atom                                                                                | Windows | Lightweight Code Editor                               |
| [SSMS SQL Server Management Server](https://go.microsoft.com/fwlink/?linkid=858904) | Windows |                                                       |
| [MS Report Builder](https://www.microsoft.com/en-us/download/details.aspx?id=53613) | Windows |                                                       |

## Acronyms

| Term   | Topic          | Definition                                                   |
| ------ | -------------- | ------------------------------------------------------------ |
| GUI    | General        | Graphical User Interface                                     |
| NAS    | General        | Network Attached Storage                                     |
| OS     | General        | Operating System                                             |
| RDP    | General        | Remote Desktop Protocol                                      |
| VM     | General        | Virtual Machine                                              |
| VPN    | General        | Virtual Private Network                                      |
| WPF    | OS             | Windows Presentation Foundation                              |
| OOP    | Programming    | Object Oriented Programming                                  |
| OOPL   | Programming    | Object Oriented Programming Language                         |
| ANSI   | Programming    | American National Standards Institute                        |
| API    | Programming    | Application Programming Interface                            |
| IDE    | Programming    | Integrated Development Environment                           |
| LOC    | Programming    | Lines of Code                                                |
| MVC    | Programming    | Model View Controller                                        |
| RTFM   | Programming    | Read the F**king Manual                                      |
| SCM    | Programming    | Source Control Management                                    |
| SLOC   | Programming    | Source Lines of Code                                         |
| SQL    | Programming    | Structured Query Language                                    |
| SSH    | Programming    | Secure Shell                                                 |
| TDD    | Programming    | Test Driven Development                                      |
| UI     | Programming    | User Interface: The space where humans and machines interact |
| JSON   | Programming    | JavaScript Object Notation                                   |
| DRY    | Programming    | Don’t Repeat Yourself                                        |
| CRUD   | Programming    | Create Read Update Delete                                    |
| GET    | REST           | Read a file                                                  |
| POST   | REST           | Create a file                                                |
| PUT    | REST           | Update a file                                                |
| DELETE | REST           | Delete a file                                                |
| DVCS   | Source Control | Distributed Version Control System                           |

## CRUD Definitions

| CRUD     | Create | Read   | Update | Delete |
| -------- | ------ | ------ | ------ | ------ |
| REST API | POST   | GET    | PUT    | DELETE |
| SQL      | INSERT | SELECT | UPDATE | DELETE |
