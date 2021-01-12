# Class 02 
## [Home Page](../README.md)

#### References:

HTML book by Duckett
- Chapter 2: “Text” (pp.40-61)
- Chapter 10: Ch.10 “Introducing CSS” (pp.226-245)

JavaScript book by Duckett
- Chapter 2: “Basic JavaScript Instructions” (pp.53-84)
- Chapter 4: “Decisions and Loops” only up to the section on switch statements (pp.145-162)

### Text
- tags are called "markup"
    - Stuctural markup
    - Semantic Markup
- HTML has six "levels" of headings:
    - `<h1>` through `<h6>`
- `<p>` paragraphs
- `<b>` for bold
- `<i>` for italics
- `<sup>` used for superscript
    - such as the suffixes of dates or mathematical concepts like raising a number to a power such as 2^2.
- `<sub>` used for subscript
    - commonly used with foot notes or chemical formulas such as H20
- two spaces next to each other cause a line break. 
- `<br />` - used to add a line break in the middle of a sentence
- `<hr />` - horizontal rule, to create a break between themes
    - adds a thin line accross the page to seperate items


- Semantic Markup
    - text elements that are not intended to affect the structure of your web pages, but they do add extra information to the pages
    - `<strong>` - indicates that its content has strong importance.
        - By default, browsers will show in bold
    - `<em>` - emphasis - by default will show in italic
    - `<blockquote>` - used for longer quotes that take up an entire paragraph
    - `<q>` - used for shorter quotes that sit within a paragraph
    - `<abbr>` - If you use an abbreviation or an acronym, then the `<abbr>` element can be used. A title attribute on the opening tag is used to specify the full term.
        - example - `<p><abbr title="Professor">Prof</abbr> Stephen Hawking is a theoretical physicist and cosmologist.</p>`
    - `<cite>` - When you are referencing a piece of work such as a book, film or research paper
    - `<dfn>` - the first time you explain some new terminology. known as the defining instance of it. 
        - Some browsers show the content of the `<dfn>` element in italics. Safari and Chrome do not change its appearance.
    - `<address>` - has quite a specific use: to contain contact details for the author of the page.
        - Browsers often display the content of the `<address>` element in italics.
    - `<ins>` - show content that has been inserted
    - `<del>` - shows content deleted from webpage
    - `<s>` - indicates something is no longer accurate but that should not be deleted
### Introducting CSS 
- CSS works by associating rules with HTML elements.
    - "Selectors" indicate which element the rule applies to.
    - "Declarations" indicate how the elements referred to in the selector should be styled.
        - CSS declarations sit inside curly brackets and each is made up of two parts: a "property" and a "value", separated by a colon
            - Properties indicate the aspects of the element you want to change.
            - Values specify the settings you want to use for the chosen properties.
    - The `<link>` element can be used in an HTML document to tell the browser where to find the CSS file used to style the page. It is an empty element (meaning it does not need a closing tag), and it lives inside the `<head>` element. It should use three attributes:
        - href -This specifies the path to the CSS file 
        - type - This attribute specifies the type of document being linked to. The value should be "text/css".
        - rel - This specifies the relationship between the HTML page and the file it is linked to. The value should be "stylesheet" when linking to a CSS file
    - you can also include CSS rules within an HTML page by placing them inside a `<style>` element, which usually sits inside the `<head> `element of the page.
    - Universal Selector 
        - Applies to all elements in the document
        - `* {}`
    - Type Selector
        - Matches element names
        - `h1, h2, h3 {}`
    - Class selector
        - Matches an element whose class attribute has a value that matches the one specified after the period (or full stop) symbol
        - `.note {}`- targets any element whoes class attribute has a value of note
        - `p.note {}` -  targets only `<p>` elements whose class attributes have a value of note
    - Id Selector 
        - `#introduction {}`- Targets the element whose id attribute has a value of introduction
    - Child Selector
        - `li>a {}`- Targets any `<a>` elements that are children of an `<li>` element (but not other `<a>` elements in the page)
    - Descendant Selector
        - `p a {}` - Targets any `<a>` elements that sit inside a `<p>` element, even if there are other elements nested between them
    - Adjacent Sibling Selector
        - `h1+p {}` - Targets the first `<p>` element after any `<h1>` element (but not other `<p>` elements)
    - General Sibling Selector
        - `h1~p {}` - If you had two `<p>` elements that are siblings of an `<h1>` element, this rule would apply to both
- CSS Cascading rules 
    - Last Rule - If the two selectors are identical, the latter of the two will take precedence
    - Specificity - If one selector is more specific than the others, the more specific rule will take precedence over more general ones
    - `!important`
    You can add `!important` after any property value to indicate that it should be considered more important than other rules that apply to the same element.
- If you specify the font-family or color properties on the `<body>` element, they will apply to most child elements. This is because the value of the font-family property is inherited by child elements
- You can compare this with the background-color or border properties; they are not inherited by child elements
- You can force a lot of properties to inherit values from their parent elements by using `inherit` for the value of the properties

### Basic Javascript Instructions

- A script is a series of instructions that a computer can follow one-by-one. Each individual instruction or step is known as a "statement" 
- JavaScript is case sensitive
- curly braces indicate the start and end of a code block
- STATEMENTS ARE INSTRUCTIONS AND EACH ONE STARTS ON A NEW LINE
    - The semicolon also tells the JavaScript interpreter when a step is over
-  You should write comments to explain what your code does.
    - `/* this is javascript comment*/` for multi line comment
    - `// this is javascript comment` for single line comment

- A script will have to temporarily store the bits of information it needs to do its job. It can store this data in "variables"
-  BEfore you can use a variable, you need to announce that you want to use it
    - this is "declaring" a variable
    - `var` - variable keyword
    - `var quantity;` - "quantity is the variable name
        - can be anything you want 
        - if it is more than one word, its usually written in camelCase
    - `quantity = 3;` - the = is the assignment operator, and the 3 is the variable value 
- JavaScript distinguishes between numbers, strings, and true or false values known as Booleans
    - numbers - decimals, whole numbers etc. 
    - 'this is a string' 
    - boolean are either true, or false
- using quotes inside a string
    - Because strings can live in single or double quotes, if you just want to use double quotes in the string, you could surround the entire string in single quotes.
    - If you just want to use single quotes in the string, you could surround the string in double quotes
    - You can also use a technique called escaping the quotation characters. This is done by using a backwards slash (or "backslash") before any type of quote mark that appears within a string
        - The backwards slash tells the interpreter that the following character is part of the string, rather than the end of it.
-  USING A VARIABLE TO STORE A BOOLEAN
    -  Boolean variable can only have avalue of true or fa1se, but this data type is very helpful.
    - Booleans are used when the value can only be true/ fa1se.
    - Booleans are used when your code can take more than one path
- Variables can be declared and assigned 
    - in the same statement as in `var price = 3`
    - multiple variables declared in the same line as in 
    `var price, quantity, total;`   
    `price = 3;`  
    `quantity = 4;`  
    `total = 15;`  
    - variables are declared and assigned values on the same line, then one other is assigned on the next line

- Once you have assigned a value to a variable, you can then change what is stored in the variable later in the same script.
    - Once the variable has been created, you do not need to
use the var keyword to assign it a new value. You just use the variable name, the equals sign (al so known as t he assignment operator), and the new value for that attribute.
- six rules you must always follow when giving a variable a name:
    - The name must begin with a letter, dollar sign ($),or an underscore (_). It must not start with a number.
    - The name can contain letters, numbers, dollar sign ($), or an underscore (_). Note that you must not use a dash(-) or a period (.) in a variable name.
    - you cannot use keywords or reserved words. 
    - All variables are case sensitive
    - Use a name that describes the kind of information that the variable stores
    - if your variable name is made up of more than one word, use a capital letter for the first letter of every word after the first word.
- An array is a special type of variable. It doesn't just store one value; it stores a list of values.
    - when you create the array, you do not need to specify how many values it will hold
    - The values are assigned to the array inside a pair of square brackets, and each value is separated by a comma
    - Values in an array are accessed as if they are in a numbered list. It is important to know that the numbering of this list starts at zero
- An expression evaluates into (results in) a single value. Broadly speaking there are two types of expressions
    - expressions that just assign a value to a variable
    - expressions that use two or more values to return a single value
-  Expressions rely on things called operators; they allow programmers to create a single value from one or more values
    - arithmetic operators 
        - `+` add
        - `-` subtract
        - `/` divide 
        - `*` multiply
        - `++` incriment
        - `--` decrement
        - `%` modulus (divides two values and returns the remainder)

        - Mulitplication and division happen before addition and subtraction
        - change the order by placing what you want first in parenthasis 
    - String operators
        - the `+` symbol used 
        - the process of joining together two or more strings is called **"concatenation"**
        - quotes around a number makes it a string

### Decisions and loops

- Two components to a decision
    - an expression is evaluated, which returns a value
        - commonly done by comparing two values using a comparison operator which returns a value of either true or false
    - a conditional statement says what to do in a given situation
        - based on the concept of if/then/else; if a conditoin is met, then your code executes one or more statements, else your code does something different
    - `==` is equal to 
    - `===` strict equal to 
    - `!=` is not equal to 
    - `!==` strict not equal to 
    - `>` greater than
    - `<` less than 
    - `>=` greater than or equal to
    - `<=` less than or equal to 

    - there is usually one operator, and two operands
        - the operands are on either side of the operator, they can be values or variables
        - often enlosed in brackets
    - operands do not have to be single values or variable names
        - and operand can be an expression
    - comparison operators usually return single values of true or false. logical operators allow you to compare the results of more than one comparison operator
        - `&&` logical and 
        - `||` logical or 
        - `!` logical not 
    - if statement checks a condition, if the condition evaluates as true, any statements in the subsequent code block are executed
    - if else statement checks a condition,
        - if it resolves as true, the first code block is executed
        - if the condition resolves as false, the second code block is run instead
