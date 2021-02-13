# Class 08 
## [Home Page](../README.md)

#### References:

HTML book by Duckett
- Chapter 15: “Layout” (pp.358-404)


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

