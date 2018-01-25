# Logging

You don't always have access to the debugger. When you're in production, you still need to know what's going on with your app. That's where logging comes in.

* [Log Levels](#log-levels)
  * [Fatal: The Most Severe Log](#fatal-the-most-severe-log)
  * [Error: Something Bad Happened](#error-something-bad-happened)
  * [Warning: Something Unusual Happened](#warning-something-unusual-happened)
  * [Info: Just Thought You Should Know](#info-just-thought-you-should-know)
  * [Debug/Trace: Extremely Verbose](#debugtrace-extremely-verbose)
* [Rolling Logs](#rolling-logs)

## Log Levels

Sometimes we just want the CliffsNotes, while other times we want everything. So, to handle this, we have multiple log levels:

### Fatal: The Most Severe Log

* Causes the application to crash
* Failing in a way that is unrecoverable

### Error: Something Bad Happened

* Typically causes whatever operation/action you're doing to fail

### Warning: Something Unusual Happened

* A condition that we might want to be aware of happened, but is not indicative of a failure
* Warning would not indicate that something did not work, but it could be an interesting clue
* Less severe than Error

### Info: Just Thought You Should Know

* An object was successfully saved
* User logged in
* User logged out
* Informational about the activity that was happening

### Debug/Trace: Extremely Verbose

* Informational only -- not indicative of anything bad happening
* Informational to help you figure things out
* Should be used in any part of the application that is rapidly repeatable

## Rolling Logs

Usually, you and your team don't need an endless history of logs. The logs from 5 years ago would be pretty irrelevant to your team. So, usually logs are rolled, which means that only a specific set of logs over a given time period are kept. Many people use a 5-7 day rolling log:

* Log.0.txt (Sunday)
* Log.1.txt
* Log.2.txt
* Log.3.txt
* Log.4.txt
* Log.5.txt
* Log.6.txt (Saturday)

Once you get back to Sunday, you start writing over your previous Sunday log.
