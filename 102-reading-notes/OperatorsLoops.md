# Operators and loops

#### Back to README Home Page
* [README](README.md)



Comparison operators: evaluating conditions
- you can evaluate a situation by comparing one value in a script to what you expect it might be. the result is a boolean true or false
- == is equal to 
    - the operator compares two values to see if they are the same 
    - prefereable to use the strict method
- === strict equal to 
     - compares to values in terms of type or value 
     - if they are not the same, the boolean comes back false
- != is not equal to 
    - compares two values to see if they are not the same 
    - if they are not the same the boolean comes back true
- !== strict not equal to
    - compares two values to chekc that both are not the same type and value

- ```>``` greater than
    - checks to see if the number on the left is greater than the number on the right
- ```>=``` greater than or equal to 
- ```<``` less than
- ``` <=``` less than or equal to 

Logical operators 
- comparison operators usually return single values as true or false, logical operators allow you to compare the results of more than one comparison operator
- && logical and 
- || logical or
- ! logical not

Loops
- check a condition
    - if it returns true, a code block will run, 
    - then the condition will be check again and if it is still true then the code block will run again, so on and so forth until the condition comes back false. 
- three common types of loops
    - "for" loops
        - used to run code a specific number of times, 
        - most common type of loop 
        - use a counter to tell the computer how many times to run the loop 
    - "while" loops 
        - if you dont know how many times to run the code
        - condition is something other than a counter
        - code will continue to loop for as long as the condition is true
    - "do while" loops 
        - very similar to the while loop but will always run the statements inside the curly braces at least once even if the condition is false
- loop counters 
    - initialization 
        - creat a variable and set it to "0" 
        - this variable is commonly called "i" 
            - acts as the counter
    - condition 
        - the loop should continue to run until the counter reaches a specified number 
        - the value of "i" was initially set to "0" 
    - update 
        - every time the loop has run the statemetns in the curly braces it adds one to the counter
        