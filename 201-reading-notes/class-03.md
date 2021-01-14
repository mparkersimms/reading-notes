# Class 03 
## [Home Page](../README.md)

#### References:

HTML book by Duckett
- Chapter 3: “Lists” (pp.62-73)
- Chapter 13: “Boxes” (pp.300-329)

JavaScript book by Duckett
- Review from Reading 02 - Chapter 2: “Basic JavaScript Instructions” (pp.70-73)  
- Chapter 4: “Decisions and Loops” from switch statements on (pp.162-182)

## Lists 

- Three different types of lists:
    1. Ordered lists
        - `<ol>`, `</ol>`
    1. Unordered lists
        - `<ul>`,`</ul>`
    1. Definitiion lists
        - `<dl>`,`</dl>`
        - Each term being defined is placed between- `<dt></dt>`
        - Each definition is between `<dd></dd>`

- Each item in the list is placed between `<li>` and `</li>`
- you can place a second list inside an `<li>` element to creat a sub-list

## Boxes

### Box Dimensions
    - `width:`, `height:`
    - The most popular ways to specify the size of a box are to use pixels, percentages, or ems  
    - when you use *percentages* it is relative to the size of the browser window, or if the box is encased within another box, it is a percentage of the size of that box
    - When you use *ems*, the size of the box is based on the size of text within it
- Limiting width
    - `min-width:, max-width:`
    - min-width property specifies the smallest size a box can be displayed at when the browser window is narrow
    - max-width property indicates the maximum width a box can stretch to when the browser window is wide
- Limiting Height
    - `min-height, max-height:`
    - same as width
    - If the box is not big enough to hold the content, and the content expands outside the box it can look very messy. To control what happens when there is not enough space for the content of a box, you can use the overflow property, 
- Overflowing content
    - `overflow:`
    - two values :
        - `hidden`
            - simply hides any extra content
        - `scroll`
            - adds a scrollbar to the box so that users can scroll to see the missing content

### Border, Margin, and Padding

    - borders separate the edges of the boxes from one another
    - margins sit outside the edge of the border
        - creates a gap between the borders of adjacent boxes
    - padding is the space between the border of a box and any content inside of it.
- White space and vertical margin
    - white space is the space between items on a page, 
- border width
    - `border-width:`
        - given in pixels or :
        - `thin`
        - `medium`
        - `thick`

    - `border-top-width`
    - `border-bottom-width`
    - `border-right-width`
    - `border-left-width`
    - `{border-width: 1px 4px 12px 4px;}`
        - order is top, right, bottom, left
- border style
    - `border-style:`
    - can individually change the styles of different borders by:
        - `border-top-style `
        - `border-left-style` 
        - `border-right-style` 
        - `border-bottom-style`
- Border color
    - `border-color`
    - `border-top-color`
    - `border-right-color`
    - `border-bottom-color`
    - `border-left-color`
    - `border-color: #bbbbaa #111111 #ee3e80 #0088dd;}`
        - order top, right, bottom, left
- shorthand
    - `border`
        - specify width, style and color in that order in one line
            - `border: 3px dotted #0088dd;}   `
- padding
    - `padding`
        - most often specified in pixels
    - `padding-top`
    - `padding-right`
    - `padding-bottom`
    - `padding-left`
    - `padding: 10px 5px 3px 1px;`
        - order: top, right, bottom, left
- Margin
    - `margin`
        - controls the gap between boxes
    - `margin-top`
    - `margin-right`
    - `margin-bottom`
    - `margin-left`
    - `margin:1px 2px 3px 4px;`
        - order: top right, bottom, left

### centering content

- centering a box on the page, set the left and right margins to auto
- `text-align: center;` will align the text inside a box to the center

### Change inline/block

- `display:`
    - `inline` - causes a block level element to act like an inline element
    - `block` - causes an inline element to act like a block-level element.
    - `inline-block` - causes a block-level element to flow like an inline element, while retaining other features of a block-level element
    - `none` - hides an element from the page

### Hiding Boxes

- `visibility:` 
    - `hidden` - hides the element
    -  `visible` - shows the element
### Border image

- `border-image`
- applies an image to the border of any box. It takes a background image and slices it into nine pieces
- requires three pieces of information:
    - The URL of the image
    - Where to slice the image
    - What to do with the straight edges; the possible values are:
        - `stretch`
        - `repeat`
        - `round` - the tiles do not fit exactly, scales the tile image so they will 

### box shadows

- `box-shadow`
    - allows you to add a drop shadow around a box
    - horizontal offset
        - negative values postion the shadow to the left of the box
    - Vertical offset
        - negative values ofset the shadow to the top of the box
    - blur distance
        - if omitted, the shadow is a solid line like a border
    - spread of shadow
        - if used, a positive value will cause the shadow to expand in all directions and a negative value will make it contract
        - The inset keyword can also be used before these values to create an inner-shadow.
        
### Rounded Corners

- `border-radius:`
    - `border-top-right-radius` 
    - `border-bottom-right-radius` 
    - `border-bottom-left-radius` 
    - `border-top-left-radius`
    - `border-radius: 5px, 10px, 5px, 10px;`
        - top, right, bottom, left

### Elliptical shapes

- `border-radius`
    - to create more complex shapes, you can specify different distances for the horizontal and the vertical parts of the rounded corners.
    - You can even create a circle by taking a square box and making the border-radius the same height as the square, as shown in the third shape on the left.


## Switch Statements

- switch statements start with a variable called the switch value
    - each case indicates a possible value for the variable and the code that should run if the variable matches that value
    - example
        - `switch (level) {
            case 'one' :
            title = 'Level 1';
            break;

            case 'two':
            title = 'Level 2'
            break;

            default:
            title= 'Test';
            break;
        }
### Type coercion and weak typing

- if you use a data type javascript did not expect it tries to make sense of the operation rather than report an error
- javascript can concert data behind the scenes to complete an operation- "type coercion"
- javascript is said to have weak typing because data types can change '1' and 1 can be the same thing
    - so use strict equals operators becasue of this. 
        - === not ==

### Truthy and Falsy values

- Falsy values are treated as if they are false. 
    - treated as the numnber '0'
- Truthy values are treated as if they are true
    - treates as the nunmber '1'
-
### Checking equality and existence

- Because the presence of an object or array can be considered truthy, it is often used to check for the existence of an element within a page.
- A unary operator returns a result with just one operand.

### Short Circuit values

- Logical operators are processed left to right. They short-circuit (stop) as soon as they have a result - but they return the value that stopped the processing (not necessarily true or fa1se

### Loops 

- for loops 
    - for running a loop a set amount of times
- while loops
    - when you dont know how many times to run the loop 
- do while loops
    - similiar to the while loop but it will always run at least once

#### loop counters
 
- starts with an initialization ( var i =0)
- then the condition ( i <10) 
- update (i++)

#### key loop concepts

- keywords
    - break - causes the termination of the loop 
    - continue - continue with the current iteration
- loops and arrays
- infinite loop - if the loop never returns a false it will continue for ever