# Diagnostics

So, you've found a problem. Now what?

When you run into an issue in a language like C#, assume it's a problem with your code. Could the issue be with Microsoft? Sure, but it's far more likely to be something with your code.

Don't go chasing zebras: If you see hoof prints, you should probably think horse, not zebra.

* [Diagnostic Steps](#diagnostic-steps)
  * [Define the Problem](#define-the-problem)
  * [Reproduce the Issue](#reproduce-the-issue)
  * [Determine the Nature of the Problem](#determine-the-nature-of-the-problem)
  * [Find the Error Message](#find-the-error-message)
  * [Google Like a Pro](#google-like-a-pro)
  * [Confirm the Fix](#confirm-the-fix)
  * [Write a Test](#write-a-test)

## Diagnostic Steps

These diagnostic steps will help you solve any problem in software:

### Define the Problem

Make sure that you understand the problem reported. Communication is really important, and there is nothing more frustrating on the user side than having to go through multiple rounds of testing in order to solve one problem.

So let's make sure we're understanding what they are reporting. An issue reported in a professional software environment will have all of these things:

* URL: In a web application this can tell you quite a bit. When using a framework like ASP.NET MVC, it will help you isolate it down to a controller action and in some cases even give you the parameters that can reproduce the problem.
* Screenshots: Screenshots will show you much more than just the error. They let you know what browser they are using and may give you clues about what data they were submitting.
* Screencasts: Pictures are worth 1,000 words. Videos are worth more. In certain circumstances, you'll have access to a screencast that shows exactly what the user encountered.
* Steps to Reproduce: These are important to expose what data they are entering or the order that they are doing things to help you reproduce the problem. A video is a welcome substitute if your tester is tech savvy.

### Reproduce the Issue

The most important step and the one most frequently skipped. You cannot know that you have definitely addressed the error if you haven't reproduced the behavior reported. Even the simplest problem must be reproduced before fixing.

Remember this is a Science, so we have to prove it to ourselves that we've addressed the issue. We cannot take it on face value.

If you cannot reproduce the issue, here's some things to check:

* Environment: Something due to configuration, anything that is not on source control, or any prerequisites that are required.
* Source Cod: Git is atomic.
* Data:
  * Extremely large strings
  * Improperly encoded values. Use the death string to reproduce:
    * !@#$%^&*(*())_{}:”?><.//f
  * Data previously stored in the database.

### Determine the Nature of the Problem

The nature of the problem is important to know in order to resolve this issue:

* Logic Problems: If the problem is a logic problem, then that means the program was instructed to do the wrong thing, and you simply have some more development to do. Your next steps are likely to refactor and possibly put in some function boundaries that can help reduce state.
* Unexpected Errors: These are typically due to data in some way if the software has passed QA at some point, which means that you need to keep a big eye out for issues like encoding problems.

### Find the Error Message

On a production system, this will have to be via the log. On your local system, this will usually float to the top when you've reproduced the issue.

If you can't find a log:

* Verify where it should be written in the code.
* Ensure that there are no try/catch blocks that don't log anything. Remove these or put in logging statements.
* Ensure that the application has permission to write to the directory it's attempting to log to.
* Debug the code and make sure that you're hitting the lines of code that you think you should be.

This might sound weird, but you can breathe a deep sigh of relief once you have an error message with a Stack Trace; it's typically smooth sailing from there. Carefully and slowly read the message in its entirety before you start pasting to Google. Let's recap the information contained here:

* In debug mode, you literally have the line of code and file where the error occurred along with the 5-8 methods that called that function.
* The error message is as descriptive as the author knew to make it (results may vary).
* If you are debugging on local machine, you can put a breakpoint on that line and start examining variables and parameters.
* If you've done these steps, and it still doesn't make sense, by all means go to Google.

### Google Like a Pro

Googling is great, but make sure you have an understanding of the technology used.

* If you're touching something completely new, make sure you've read its intro page to learn a little about it.
* If your search isn't bearing fruit, use quotes around the error message for exact match: "Error: The thing is wrong".
* Make sure you're not including dynamic data like filepaths on your local system, or string or variable data that may be a part of the message but is not static.

### Confirm the Fix

Great, we think we have the fix. No matter how sure you are, we still need to prove it to ourselves by repeating the steps and making sure that we cannot reproduce with those steps:

* Commit your code after confirming. Reference the issue id in the commit conforming to the format that you see in other commits.
* Push it to your remote.
* Flag the issue to Code Review and move on to the next one.

### Write a Test

In a properly architected system you should be able to write a unit test after manually reproducing the issue that will reproduce the error. This gives you a fast way to replicate the problem as you make your attempts to fix it. It also ensures that the bug will not be reintroduced, since there will be a unit test testing for it in the future.

IF this is not the case, you need to find a way to start working in that direction. To start with, simply getting proper function boundaries in place is a big step. Pulling all the data access to a repository pattern is usually a good start.

Remember: unit tests are not typically used to hit the database, so without the Repository pattern or something similar, you can't write consistent tests that ignore the filesystem.
