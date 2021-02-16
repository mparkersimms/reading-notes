# Class 2

## [Home Page](../README.md)

#### References:

JavaScript and jQuery book by Jon Duckett pages 293-301, 306-331 and 354-357

https://www.codefellows.org/blog/6-reasons-for-pair-programming/


## jQuery

jQuery offers a simple way to achieve a variety of common JavaScript tasks quickly and consistently, across all major browsers and without any fallback code needed

- Select elements
- perform tasks
- handle events

jQuery() allows you to find one or more elements in the page 
- can also be written like $();

jQuery object has many methods that you can use to work witht the elements you select. 
- do something with the elements using jquery

to get jQuery to work, you have to include the jquery script on the html page just like js. 

Why use jQuery 
1. simple selectors
2. common tasks in less code
3. cross-browser compatibility



### matched set/ jquery selection
When you select one or more elements, a jquery object is returned. it is known as a matched set or jquety selection

Single element -  if a selector returns only one element, the jquery object contains a reference to just one element node 

multiple elements - if a selector returns several elements the jquery object contains reference to each element

### jquery methods that get and set data
some jquery methods retrieve information from and update contents of elements.but they do not always apply to all elements. 

get information
- if multiple elements 
    - will only hold reference and get information from the first element
    - will set information to all elements 

When you create a selection with jquery, it stores a reference to the corresponding nodes in the dom tree, not a copy of them

a jQuery object stores reference to elements. 
Caching a jquery object stores a reference to it in a variable.  

looping - 

-  with jquery when the selector returns multiple elements, you can update all of them using one method. theres no need to use a loop 

chaining - 
- if you want to use more than one jquery method on the same selection of elemnts, you can list several methods at a time using dot notation to seperate each one. 

Checking a page is ready to work with 

- .ready() method checks that the page is ready for your code to work with

Getting element content

- the .html() and .text() methods both retrieve and update the content of elements. 

updating elements

- four methods that update the content of all elements in a jquery selection
    - .html()
    - .text()
    - .replaceWith()
    - .remove()

inserting elements
- inserting elements involves two steps 
    - create the new element
    - use a method to insert the content on the page
        - .before()
        - .after()
        - .prepend()
        - .append()
    
getting a setting attributes

- .attr()
- .removeAttr()
- .addClass()
- .removeClass()

getting and setting css properties
the .css() method lets you retrieve and set the values of css properties

working with each element in a selection 
- .each() 
    - allows you to perform one or more statements on each of the items in the selection of elements that is returned by a selector
- this or $(this)
    - access current element as it goes through the .each()



## traversing the DOM

when you have made a jQuery selection, you can use the methosds to access other element nodes relative to the intitial selection. 

examples 
1. the .find() and .closest() methods both require a CSS-style selector as an argument. 

2. .parent(), .parents(), .children() etc. CSS selector is optional 


## Pair programming 

How does pair programming work?
While there are many different styles, pair programming commonly involves two roles: the Driver and the Navigator. The Driver is the programmer who is typing and the only one whose hands are on the keyboard. Handling the “mechanics” of coding, the Driver manages the text editor, switching files, version control, and—of course writing—code. The Navigator uses their words to guide the Driver but does not provide any direct input to the computer. The Navigator thinks about the big picture, what comes next, how an algorithm might be converted in to code, while scanning for typos or bugs. The Navigator might also utilize their computer as a second screen to look up solutions and documentation, but should not be writing any code.

- from 6 Reasons for Pair Programming by Allie Grampa

1. Greater efficiency
2. Engaged collaboration
3. Learning from fellow students
4. Social skills
5. Job interview readiness
6. Work environment readiness