# Class 01
## [Home Page](README.md)

#### References:  

HTML & CSS by Dcukett
- Introduction (pp.2-11)
- HTML Chapter 1: “Structure” (pp.12-39)
- HTML Chapter 8: “Extra Markup” (p.176-199)
- HTML Chapter 17: “HTML5 Layout” (pp.428-451)
- HTML Chapter 18: “Process & Design” (pp.452-475)  

Javascript and JQuery by Duckett
- Introduction
- JS Chapter 1: “The ABC of Programming” (pp.11-52)

### HTML Intro:
- HTML
    - What words you want to show up on the webpage
    - With tags to make it easy to identify where you want the words to show up 
- CSS
    - Presentation 
    - layout

- Coding websites should keep in mind the web browser, device, ans screen reader devices the user will use to view the website

### Stucture
- stucturing word documents
    - use headings, sub headings, 
- in HTML you structure the webpage by using elements and tags
    - elements liv inside angled brackets
    - elements are usually made up of two tags: an opening tag and closing tag ( closing tag has an extra / )
        - opening tag ``` <p> ```
        - closing tag ```</p> ```
- ``` <HTML> ```)
    - indicates anything between the html tags is HTML code 
- ``` <body> ``` 
    - indicates what is on the main body of the web page
- ```<h1> ```
    - main heading
- ```<p> ```
    - paragraph
- ```<h2>``` 
    - subheading 
- attributes consist of two elements 
    - a **name** and a **value** 
    - live inside the opening tag

    - before the body tag you have the ```<head>``` tag, 
        - contains information about the website that is not shown on the main page 
    - ```<title>``` 
        - shown in the top of the browser
    - you can see how other websites are structured by using the "inspect" option on any webpage and view the code in the inspection window

### Extra Markup 
- HTML 4 released in 1997 
    - most of the book is written in HTML 4
- XMTML 1.0 released in 2000
    - added some new strict rules about writing markup
- HTML 5 work in progress
    - dont need to close all tags, 
    - although its not complete it can still be used 
- use a DOCTYPE prior to writting code to specify which language you are using
    - ```<!DOCTYPE html>``` 
- adding a comment to your code 
    ``` - <!-- comment goes here --> ```
- id attribute 
    - used to uniquely identify an element 
    - oonly one element on a webpage can use the same id 
    - ``` <p id="example">```
- class attribute 
    - identifing several elements on a webpage with a class
    - ```<p class="exampleclass"> ```

- block elements 
    - elements that always appear to start on a new line and take up as much room as they can 
        - examples are ``` <h1>, <p>, <ul>, and <li>```

- inline elements 
    - elements appear to continue on the same line as their neighbors 
    - examples are  ``` <a>, <b>, <em>, <img> ```

- grouping text or elements in a block 
    - ```<div>``` 
    - allows you to group other elements inside a single block element 
- gouping text or elements inline 
    - ``` <span> ```
    - acts as an inline sequencer
- iframes 
    - ```<iframe>``` 
    - allow you to show the contents of another webpage inside your webpage 
    - requires a  
        - src attribute
        - a height attribute 
        - a width attribute 
- meta data allows you to add keywords for search engines 
- escape characters
    - &lt; Less than sign = &lt;lt:
    - &gt; Greater than sign = &amp;gt;
    - &amp; Ampersand = &amp;amp;
    - " Quotation marks = &amp;quot;
    - cent sign = &amp;cent;
    - Pound sign = &amp;pound;
    - Yen sign = &amp;yen;
    - Euro sign = &amp;euro;
    - Copyright symbol = &amp;copy;
    - Registered trademark = &amp;reg;
    - Trademark = &amp;trade;
    - left single quote = &amp;lsquo;
    - right single quote = &amp;rsquo;
    - left double quote = &amp;ldquo;
    - right double quote = &amp;rdquo;
    - multiplication sign = &amp;times;
    - division sign = &amp;divide;

### HTML5 Layout  
- eleminates alot of the ```<div>``` elements on a webpage by giving specific items their own name 
- ```<header>, <footer> ```
    - whats in the header and the footer of the webpage
- ``` < nav>```
    - the nav bar 
- ```<article> ```
    - any elements that could stand alone
- ``` <aside>``` 
    - used inside and outside an article 
    - either information related to the article or to the entire webpage
- ```<section> ```
    - groups related content together
    - should not be used as a wrapper for the entire webpage 
        - unless the webpage is one distinct piece of information
- ```<hgroups>``` 
    - group together a set of 1 or more ```<h1>``` through ```<h6>``` tags
- ```<figure> and <figcaption>```
    - used to contain any content that is referenced from the main flow of the article not just the image
- ```<div>``` 
    - still an important way to group content together 
- ```<a> ```
    - allows you to turn the entire block into a link 
- some older browsers dont understand HTML 5 
    - you should use a line of CSS code to specify the which new elements are block- level elements 
    - example : 
        - ``` header, footer, section, aside, article {
            display: block}
### Process and Design
- understand:
    - who the site is for, 
    - why people are visiting the site 
    - what your visitors are trying to achieve
    - what info your visitors need
    - how often people will visit the site
- site maps 
    - help organize the webpage 
- wireframes
    - simple sketch of the webpage and layout
- use design    
    - content, 
    - prioritization
    - organization
    - visual heirarchy 
        - size of elements
        - color
        - style 
    - grouping 
        - proximity, 
        - closure
        - continuance 
        - white space 
        - color 
        - borders 
        - consistency 
        - headings
    - similiarity
    - designing navigation
        - consise, 
        - clear
        - selective 
        - context 
        - interactive
        - consistent
### The ABCs of programming 
- a - what is script?
    - a series of instuctions
    - writing script is 
        - defining the goal 
        - designing the script
            - tasks 
                - once you know the goal, you can define what steps it is going to take to accomplish the goal 
            - steps
                - each task is broken down into a sequence of steps
        - code each step
            - learn the new language 
                - vocabulary
                - syntax
        - each time a script is run it might only use a subset of all the instructions
        - computers solve tasks *programmatically*
- b - how do computers fit in with the world around them ?
    - computers creat models of the world using data
    - objects 
        - are things 
    - properties
        - are characteristics
    - events 
        - is what computers understand as "something just happened" 
        - can be used to trigger a specific set of instructions or types of functionalites
    - Methods 
        - how things interact with a object
        - contains lots of instructions that together represent one task
- c - how do i write a script for a webpage?
    - how HTML, CSS, and JavaScript fit together 
        - HTML - content layer
        - CSS -  presentation layer
        - JavaScript - behavior layer
    - best to keep javascript in its own text file with the ```.js``` extension
    - ```<script>``` element is used in HTML to tell the browser to load the javascript file 
    
