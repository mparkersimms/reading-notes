# Class 06 
## [Home Page](../README.md)

#### References:

JS book by Duckett
- Chapter 3: “Object Literals” (pp.100-105)
- Chapter 5: “Document Object Model” (pp.183-242)

## What is an object
- Objects group together a set of variables and functions to create a model of a something you would recognize from the real world. In an object, variables and functions take on new names.
- IN AN OBJECT: VARIABLES BECOME KNOWN AS PROPERTIES
- IN AN OBJECT: FUNCTIONS BECOME KNOWN AS METHODS
- `var hotel = {`
    `name: 'Quay',`
    `rooms: 40,`
    `booked: 25,`
    `gym: true,`
    `roomTypes: ['twin','double'],`
    `checkAvailability: function(){`
       ` return this.rooms - this.booked;`
    `}`
`};`

## Document Object Model

-  The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window.
    - The DOM is neither part of HTML, nor part of JavaScript; it is a separate set of rules. It is implemented by all major browser makers, and covers two primary areas
        - MAKING A MODEL OF THE HTML PAGE
        - ACCESSING AND CHANGING THE HTML PAGE

-  THE DOM TREE IS A MODEL OF A WEB PAGE
    - four main types of nodes
        - THE DOCUMENT NOD
            - represents the entire page
            - the starting point for all visits to the DOM tree 
        - ELEMENT NODES
            - 
        - ATTRIBUTE NODES
            - opening tags of HTML elements can carry attributes and these are represented by attribute nodes in the DOM tree
            - part of the element that contains them
        - TEXT NODES
            - Text nodes cannot have children

- Accessing and updating the DOM tree involves two steps
    - STEP 1: ACCESS THE ELEMENTS
        - SELECT AN INDIVIDUAL ELEMENT NODE
            - `getEl ement Byld ()`
            - `querySe1ector ()`
        - SELECT MULTIPLE ELEMENTS (NODELISTS)
            - `getElementsByClassName()`
            - `getElementsByTagName()`
            - `querySelectorAll()`
        - TRAVERSING BETWEEN ELEMENT NODES
            - `parentNode`
            - `previousSibl ing / nextSibl ing`
            - `firstChild / lastChild`
    - STEP 2: WORK W ITH THOSE ELEMENTS
        - ACCESS/ UPDATE TEXT NODES
            - `nodeValue` - lets you access or update the contents of a text node
        - WORK W ITH HTML CONTENT
            - `innerHTML`
            - `textContent`
            - `createElement()`
            - `createTextNode()`
            - `appendChild() / removeChild()`
        - ACCESS OR UPDATE ATTRIBUTE VALUES
            - `className / id`
            - `hasAttribute() `
            - `getAttribute()`
            - `setAttribute()`
            - `removeAttribute()`
    -  METHODS THAT RETURN A SINGLE ELEMENT NODE:
        - `getElementByld('id')`
        - `querySelector('css selector')`
    - METHODS THAT RETURN ONE OR MORE ELEMENTS (AS A NODELIST):
        - `getElementsByClassName('class')
        - `getElementsByTagName('tag name')`
        - `querySelctorAll('css selector')`
- SELECTING AN ELEMENT FROM A NODELIST
    - THE item() METHOD
        - `var elements = document.getElementsByClassName('hot')` 
            `if (elements.length>= 1) {`
            `var firstltem = elements.item(O); }`
    - Array Syntax
        - `var elements = document.getElementsByClassName('hot');`
            `if (elements.length >= 1) {`
                `var firstItem = elements[0];`
            `}`
-  SELECTING ELEMENTS USING CLASS ATTRIBUTES
    - ``` 
        var elements = document.getElementsByClassName('hot');                 // find hot items
        if (elements.length >2){       // if 3 or more are found
            var el = elements[2];    // select the third one from the NodeList
            el.className = 'cool';     // change the value of its class attribute
        }
        ```

- SELECTING ELEMENTS BY TAG NAME 
 ``` var elements = document.getElementByTagName('li); 
    if (eliements.length >0) {
        var el = elements [0];
        el.className = 'cool'
    }
```
- Repeating actions for an entire nodelist
    - looping througha nodelist
    - ```
        var hotItems = document.querySelectorAll('li.hot');  // sotre nodelist in array
        if (hotItems.length > 0 ){      //if it contains items
        for(var i = 0; i<hotItems.length; i++){
            hotItems[i].classname = 'cool'
        }
        }
        ```

- Traversing the DOM
    - When you have an element node, you can select another element in relation to it using these five properties:
        - parentNode
            - finds the element node fot the containing element in the HTML
        - previousSibling
        - nextSibling
            - find the previous or next sibling of a node if there are siblings
        - firstChild
        - lastChild
            - find the first or last child of the current element. 

    - White space nodes
        - most browsers treat whitespace as a text node
- How to get/Update element content
    - `nodeValue`  --> accesses text from node
    - `innerHTML` --> gets/sets text and markup
    - `textContent` --> gets/sets text only
    - `innerText` --> gets/sets text only

    - accessing and changing a text node
    - ```
        var itemTwo = document.getElementById('two');
        var elText = itemTwo.firstChild.nodeValue;
        elText = elText.replace('pine nuts', 'kale');
        itemTwo.firstChild.nodeValue = elText;
        ```

- Adding or removing HTML content
    - innerHTML and DOM manipulation
        - `innerHTML` 
            - used on any element node
            - used to retrieve and replace
            - to add new content
                - store new content as a string in a variable
                - select the element you want to replace
                - set the elements `innerHTML` property to be the new string
            - to remove content
                - set `innerHTML` to an empty string
        - DOM manipulation methods
            - allows you to create or remove content from a DOM tree
            - create content one node at a time
            - `createElement ()`
            - `createTextNode()`
            - `appendChild()`
        - `document.write()`
            - simple way to add content to a page
- XSS 
    - cross-site scripting (XSS) attacks
        - an attacker could gain access to your users' accounts
- attribute nodes
    - `getAttribute()`--> gets the value of an attribute
    - `hasAttribute()`--> checks if element node has a specified attribute
    - `setAttribute()`--> sets the value of an attribute
    - `removeAttribute()`--> removes an attribute from an element node


