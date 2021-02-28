# Class 10

## References

Call stack
https://developer.mozilla.org/en-US/docs/Glossary/Call_stack


The JavaScript Call Stack - What It Is and Why It's Necessary
https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/


JavaScript error messages && debugging
https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c



### Call stack

"A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc."

- functions get added to the stack, as they are called and then the interpreter carrys out the function
- any functions that are part of the first function are then called and stacked on top and carried out too 
- when the function is finished it is removed from the stack


### The JavaScript Call Stack - What It Is and Why It's Necessary

by Charles Freeborn 
Jan 11, 2018

"The JavaScript engine (which is found in a hosting environment like the browser), is a single-threaded interpreter comprising of a heap and a single call stack. The browser provides web APIs like the DOM, AJAX, and Timers."

"The call stack is primarily used for function invocation (call). Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous."

"At the most basic level, a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call)."

"LIFO: When we say that the call stack, operates by the data structure principle of Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns."

"Temporarily store: When a function is invoked (called), the function, its parameters, and variables are pushed into the call stack to form a stack frame. This stack frame is a memory location in the stack. The memory is cleared when the function returns as it is pop out of the stack."

"Manage function invocation (call): The call stack maintains a record of the position of each stack frame. It knows the next function to be executed (and will remove it after execution). This is what makes code execution in JavaScript synchronous."

#### How does the call stack handle function calls?

When a function calls another function, the first function is added to the stack, and then the second one is added to the stack, and since the first one has to wait till the second one is complete it stays at the bottom of the stack. Once the second funciton is complete js can then complete the first function. Once a funcion is invoked it is "Popped on" the stack. Once the function is complete it "pops off" the stack. 


### JavaScript error messages && debugging

by Diogo Spinola Jul 17, 2017

"Most of your time as a developer is spent reading code followed by debugging that same code, most likely to be able to read it or solve an “unexpected feature” (which, joking aside, is more correctly known as a “bug”)."

#### Types of error messages

- Reference errors
    -  using a variable that is not yet declared.

- Syntax errors
    - something that cannot be parsed in terms of syntax

- Range errors
    - invalid length of object, arrays  or elements

- Type errors
    - types (number, string, etc.) you are trying to use are incompatible

#### Debugging

- console.log() the variables you want to check
- use developer tools
- putting a debugger statement in your code in the line you want to break
    - "add conditional breakpoints by right-clicking a previous set breakpoint, which will make your program stop at that point only if a condition is met"

