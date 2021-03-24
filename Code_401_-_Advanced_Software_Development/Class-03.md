# Class 03 Reading Notes 

## references
https://www.baeldung.com/java-primitives-vs-objects

https://docs.oracle.com/javase/tutorial/essential/exceptions/summary.html

https://docs.oracle.com/javase/tutorial/essential/io/scanning.html

## Java Primitives versus Objects

This article basically described the size difference between the Objects, such as Boolean, Integer, Short etc. and their primitive counterparts(boolean, int, short etc.);

The primitive variables are much smaller in size, as an example, a Boolean takes up 128 bits, where as a boolean takes up only 1 bit of memory. This difference in size makes primitives much faster to work with and manipulate. 

That being said, there are a few programs and APIs that do not allow the primitives to be used, but in most cases they are the prefered option. 

## Exceptions 

Definition: An exception is an event, which occurs during the execution of a program, that disrupts the normal flow of the program's instructions.

Valid Java programming language code must honor the Catch or Specify Requirement

"A program can use exceptions to indicate that an error occurred. To throw an exception, use the throw statement and provide it with an exception object — a descendant of Throwable — to provide information about the specific error that occurred. A method that throws an uncaught, checked exception must include a throws clause in its declaration.

A program can catch exceptions by using a combination of the try, catch, and finally blocks.

The try block identifies a block of code in which an exception can occur.
The catch block identifies a block of code, known as an exception handler, that can handle a particular type of exception.
The finally block identifies a block of code that is guaranteed to execute, and is the right place to close files, recover resources, and otherwise clean up after the code enclosed in the try block.
The try statement should contain at least one catch block or a finally block and may have multiple catch blocks.

The class of the exception object indicates the type of exception thrown. The exception object can contain further information about the error, including an error message. With exception chaining, an exception can point to the exception that caused it, which can in turn point to the exception that caused it, and so on."

## Scanning 

"Objects of type Scanner are useful for breaking down formatted input into tokens and translating individual tokens according to their data type."
"By default, a scanner uses white space to separate tokens"

Scanner uses a similar syntax to regex to determine which character it will be looking for in a file. 