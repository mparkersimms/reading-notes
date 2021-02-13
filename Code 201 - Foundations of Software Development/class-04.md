# Class 04 
## [Home Page](../README.md)

#### References:

HTML book by Duckett
- Chapter 4: “Links” (pp.74-93)
- Chapter 15: “Layout” (pp.358-404)
    - pp.358-364

JavaScript book by Duckett
- Chapter 3 (first part): “Functions, Methods, and Objects” (pp.86-99 ONLY)
- Article: “6 Reasons for Pair Programming”

## Links 

### Writing Links

- Links are created using the `<a>` element. Users can click on anything between the opening `<a>` tag and the closing `</a>` tag. You specify which page you want to link to using the href attribute.
- example : `<a href="http://www.imdb.com">IMDB</a>`
- linking to external websites use full url, when linking to another page on your site, use relative urls
- sAme FoLDer - `<a href="reviews.html">Reviews</a>`
- chiLD FoLDer - `<a href="music/listings.html">Listings</a>`
- grAnDchiLD FoLDer - `<a href="movies/dvd/reviews.html"> Reviews</a>`
- PArent FoLDer - `<a href="../index.html">Home</a>`
- grAnDPArent FoLDer - `<a href="../../index.html">Home</a>`
- emial link - `<a href="mailto:jon@example.org">Email Jon</a>`
- open link in new window - `<a href="http://www.imdb.com" target="_blank">`

- linking to parts of a page - give specific parts an "id" and then - ``<h1 id="top">Film-Making Terms</h1>`
`<a href="#top">Top</a>`
- linking to parts of another page is the same just add the id at the end of the link - `<a href="http:/www. htmlandcssbookcom/ #bottom">`
- 
## Layout

### position elements
- Block-level elements start on a new line Examples include:
`<h1> <p> <ul> <li>`
- inline elements flow in Between surrounding text Examples include:
`<img> <b> <i>`
- If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element.
- CSS has the following positioning schemes that allow you to control the layout of a page: normal flow, relative positioning, and absolute positioning. You specify the positioning scheme using the position property in CSS. You can also float elements using the float property.
    - normal flow
        - `position:static`
        - Every block-level element appears on a new line, causing each item to appear lower down the page than the previous one.
    - relative Positioning
        - `p.example {`
            `position: relative;`
            `top: 10px;`
            `left: 100px;}`
        - This moves an element from the position it would be in normal flow, shifting it to the top, right, bottom, or left of where it would have been placed. This does not affect the position of surrounding elements; they stay in the position they would be in in normal flow.
    - aBsolute Positioning
        -    `position: absolute;`
                `top: 0px;`
                `left: 500px;`
                `width: 250px;}`
        - This positions the element in relation to its containing element. It is taken out of normal flow, meaning that it does not affect the position of any surrounding elements (as they simply ignore the space it would have taken up). Absolutely positioned elements move as users scroll up and down the page.
    - fixed Positioning
        - ``position: fixed;`
            `top: 0px;`
            `left: 50px;`
            `padding: 10px;`
            `margin: 0px;`
            `width: 100%;`
            `background-color: #efefef;}`
        - The `<p>` elements are in normal flow and ignore the space that the `<h1>` element would have taken up. Therefore, the margin-top property has
been used to push the first `<p>` element below where the fixed position `<h1>` element is sitting.
            ``example {`
                `margin-top: 100px;}`
        - This is a form of absolute positioning that positions the element in relation to the browser window, as opposed to the containing element. Elements with fixed positioning do not affect the position of surrounding elements and they do not move when the user scrolls up or down the page.
    - floating elements
        - Floating an element allows you to take that element out of normal flow and position it to the far left or right of a containing box. The floated element becomes a block-level element around which other content can flow.
    - `z-index` property allows you to control which box appears on top.
    - 


## Functions methods and objects

### What is a function
- Functions let you group a series of statements together to perform a specific task
- of a function in the JavaScript file. It  is called `updateMessage().`
- To creat a function, you give it a name and then write the statements needed to achieve its task inside the curly braces. known as a function declaration
  `function sayHello() {`
    `document.write('Hello!');`
`}`
- calling a function 
    - `sayHello();`
- If a function needs information to work, you indicate what it needs to know in parentheses after the function name
    - `function getArea(width, height){`
       ` return width * height;`
    `}`
    - `getArea(3,5)` - when this is run, it will take the values and place them in the function appropriately
    - `wallWidth = 3`
    `wallHeight = 5`
    `getArea(wallWidth, wallHeight)`
    
    - `function calculateArea(width, height) {`
       ` var area = width * height;`
        `return area;`
   ` }`
       ` var wallOne = calculatedArea(3,5)`
        `var wallTwo = calculatedArea(8,5)`
    - multiple values out of a function - 
        - `function getSize(width, height, depth){`
           ` var area = width * height;`
           ` var volume = width * height * depth;`
           ` var sizes = [area, volume];`
           ` return sizes;`
        `}`
        `var areaOne = getSize(3,2,3)[0];`
        `var volumeOne = getSize93,2,3)[1];`
    - Immediately invoked functions
        - IIFE
        - parentheses after the curly brackets tells interpreter to call the function immediately
        - 

### Reasons for pair programming
- uses a driver and navigator, 
    - driver types, naviagator gives direction and scans for errors, but does not type on keyboard
- Why?
    - Greater effeciency
    - Engaged collaboration
    - Learning from fellow students
    - Social skills
    - Job interview readiness
    - Work environment readiness
