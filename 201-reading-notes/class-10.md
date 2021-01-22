# Class 10 
## [Home Page](../README.md)

#### References:

JS book by Duckett
- Chapter 10 



## Error handling and debugging

- The JavaScript interpreter uses the concept of execution contexts

- there is one global execution context, plus each function creates a new execution context. They correspond to variable scope. 

- Execution context 
    - global context
    - function context
    - eval context

- variable scope
    - global scope
    - function-level scope


The stack
- js processes one line of code at a time
- Stacking processes on top of each other as the functions return specific values. 

Execution context and hoisting

- two phases of activity for a new execution context
    - prepare
        - the new scope is created
        - variables are created
        - values are determined

    - execute
        - assign values to variables
        - reference functions
        - execute statements


Understanding Scope
- in the interpreter, each execution context has its own variables object
- it holds the variables, function, and parameters available within it. 
- Each execution context can also access its parents variables object

Understanding Errors
- if a js statement generates an error, then it throws an exception. 
- the interpreter then stops and looks for exception-handling code. 

error objects
- can help you find where your mistakes are and browsers have tools to help you read them

error -  generic error
sytaxError - syntax has not been followed
ReferenceError -  tried to reference a variable that is not declared
TypeError -  an unexpected data type that cannot be coerced
RangeError - Numbers not in acceptable range
URIError - encodeURI(), decodeURI() used incorrectly
EvalError- eval() used incorrectly

How to deal with errors

1. Debug the script to fix errors
2. handle errors gracefully

A Debugging Workflow
Find where the problem is 
- use tools that write script to tell you how far the code has gone

- use breakpoints where things are going wrong. 
- They let you pause execution and inspect the values that area stored

What exactly the problem is 
- if youve set breakpoints see if the variables around them have the right values
- breakdown parts of the code to test smaller pieces. 
- Check the number of parameters for a function or the number of items in an array

Browser Dev Tools and Javascript console

- the console will tell you when there is a problem with a script
Grouping Messages
- console.group(); method to group messages togerther you can then expand and contract the results
- it has one parameter the name that you want to use fo rthe goroup. 

- console.groupEnd()

Writing tabular data
- console.table()
lets you output a table showing:
- objects
- arrays contain other objects or arrays

writing on a condition
console.assert()
you can test if a condition is met, and write to the console only if the expression evaluates a false 

Breakpoints
you can pause the execution of a script on any line using breakpoints. 
chrome - 
- sources option
    - select the script you are working with from the left hand pane, 
    - find the line number you want to stop on and click it
    - when you run the script, it will stop on this line. 

Stepping through the code
- if you set multiple breakpoints you can step through them one by one to see hwere values change and problem might occur

Conditional breakpoints
-  you can indicate that a breakpoint should be triggered only if a condition that you specify is met. 

Debugger keyword
- you can create a breakpoint in your code using just the debugger keyword
- when the developer tools are open, this will automatically create a breakpoint
- you can also place the debugger keyword within a conditional statement so that it only triggers the berakpoint if the condition is met. 

Handling Exceptions
if you know your code might fail, 
- use try, catch, and finally



Throwing errors
- if you know something might cause a problem for your script, you can generate your own errors before the interpreter creates them 


