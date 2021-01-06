# Structure Webpages with HTML

#### Table of Contents
* [README](README.md)
* [Growth Mindset](Growth-Mindset.md)
* [Markdown](markdown.md)
* [Coders Computer](coders-computer.md)
* [Git-Tutorial](Git_Tutorial.md)
* [Structure web pages](Structure_webpages.md)

# Process & Design

references: 
Chapter 18, HTML & CSS by Duckett

## Who is the site for?
### Target Audience
#### Individuals
* age range
* gender 
* country of origin
* urban/ rural
* average income
* level of education
* martial status
* occupation
* hours they work per week 
* device type

#### Companies
* size 
* position of the people 
* for themselves or others
* budget

*invent some fictional visitors of your target audience* 
    * *theyll influence design*

### Why people visit your website
*Some may be by chance, most will be for a specific reason*

#### Key motivations 
* general entertainment vs specific goal
* personal or professional 
* essential vs luxury

#### Specific Goals
* research general information or specific topic
* are they familiar with what you offer
* time sensitive information (news, etc.)
* info to help decide whether to buy something or not
* do they need to contact you?

### What your visitors are trying to achieve
* create a list of why people would be coming to your site using your fictional characters

### What information your visitors need
* with the known information of who is coming and why to your site, now is the time to figure out what they need to know
* prioritize levels of information based on who and what 
* will the visitors be familiar with the information or do you need to introduce yourself/ product
* what differentiates you from competitors
* common questions after they visit your site

### How often people will visit your site
* how often do you need to update your site, based on how often people revisit the site
#### goods/services
* how often do they return to purchase from you
* how often is your stock updated
#### information
* how often is it updated
* what percentage would return for updated info on a subject

### site maps
* a **site map** is *a diagram of the pages that will be used to structure the site* 
* **card sorting**
    * involves placeing each piece of information that a visitor might need to know on a seperate sheet of paper and then organizing the related info into groups
* groups are turned into a site map
* usually begins with a home page 
* larger sites might require sections to have section homepages
* This is how the user will navigate the site
* try to format the site with the user in mind and how they would expect to navigate

### Wireframes
*a simple sketch of key information that needs to go on each page*
* placing logos, info, navigation bars etc. 
* no color schemes or font choices or backgrounds
* focus just on the information needed 

### Getting your Message across using design

#### content
* masthead or logo
* links to navigate
* login options
* copyright info
* links

#### prioritizing
* making parts of the page distinct from the surrounding info
* visual hierarchy 
    * helps draw the users attention around the page 

#### organizing 
* grouping together related topics into blocks or chunks
* users should identify the purpose of each chunk
* present related info in a similar visual style

### visual Hierarchy
*the order in which your eyes perceive what they see*
*created by adding **visual contrast** between items being displayed

#### size 
* larger elements will grab attention

#### color 
* brighter sections tend to draw attention

#### Style
* different style from surround will make it stand out

#### images
* create a high visual contrast

### grouping and similarity

#### proximity
items close together are perceived to be related

#### closure
in a complicated arrangement of items, we tend to look for a singular shape or pattern

#### continuance
* items grouped into a singular line or curved are perceived to be related

#### white space
grouping items with more or less space between them to give the illusion of groups

#### color
a background around related items used to group

#### borders
a line used to combine groups

#### consistency
consistant style will translate meaning from one chunk to another

#### headings
tells whether the chunk is relevent to the user

### designing navigation

#### Concise 
quick and easy to read

#### Clear
Users should be able to predict what kind of information they will find get before they click the link 

#### Selective
should only reflect the sections or content of the site
    * functions like logins and search and legal info should be elsewhere

#### Context
should allow users to identify where they are on website
    * should be formatted using different color or font to show where the user is currently

#### Interactive
links should be big enough to click on and should change when the user hovers over it

#### Consistent
Keep primary navigation exactly the same page to page
    * secondary navigation will change however


# HTML5 Layout

reference
Chapter 17, HTML & CSS by Duckett

## New HTML5 Layout Elements 
HTML5 introduces a new set of elements that allow you to divide the parts of a page and eliminates many "div" elements

## Headers and Footers
&ltheader> &lt/header>
&ltfooter>&lt/footer>
appear on the top and the bottom of a web page or possibly even an <article> or <section>

## Navigation
<nav>

Used to contain the major navigational blocks on the site such as the primary site navigation

## Articles
&ltarticle>

- acts as a container for any section of a page that could *stand alone* or be syndicated
- an independent piece of content

## Asides
&ltaside>
has two purposes
    - inside an <article>
        - should contain information that is related to the article but not essential to its overall meaning
    - outside of an <article>
        - acts as a container that is related to the entire page

## Sections
&ltsection>
groups related content together and typically has its own heading
    - may have one or many <article> elements in them 

## Heading Groups
&lthgroup>
purpose is to group together a specific set of &lth1> through &lth6> elements 

## Figures
&ltfigure> &ltfigcaption>
can be used to contain any content that is referenced from the main flow of an article (not just images)
used for something that only references content not something that is integral to the flow of the page
examples:
- images
- videos
- graphs
- diagrams
- code samples
- text that supports the main body of an article
should also contain <figcaption> which provides a description of what is in the <figure> element

## Sectioning Elements 
<div> 
When there is no other wrapper for a specific set of elements use the <div> still 
example would be to contain all the information on a page
*everyting that is not contained inside a <header> <footer> or <aside> is considered as the main content

## Linking Around Block-Level Elements 
HTML5 allows you to place a <a> element around a block level element that contains child elements and makes the entire block a link




# Extra Markup
Reference:
Chapter 8, HTML & CSS by Duckett

## Doctypes 
<!DOCTYPE html> 
becuase of several versions of HTML created every webpage needs to start with a DOCTYPE to determine what language the webpage is written in 

## Comments in HTML
<!-- --> 
<!-- comments go here -->
will not display on the webpage unless the user is viewing the source code 
used to explain certain things in the code, or to assist in explaining what is going on in the code. 

## ID Attribute
<p id="uniqueattribute">
should only start with a *letter* or an *underscore* nothing else and should be have a unique id. 

- nothing else on that page should have the same id, it would then not be unique
- allows that unique group to be formatted using CSS differently than everything else on the page
- also called a **global attribute** becuase it can be used on any element

## Class Attribute
<p class="somethingdescriptive">
its a way to uniquely identify a group of elements the same way
separate names with a space to indicate that a particual element has more than one class attribute eg <p class="somethingdescriptive somethingelse">

## Block Elements 
elements that appear to always start on a new line in a browser window
examples are : 
- <h1>
- <p>
- <ul>
- <li>

## Inline Elements 
elements that always appear to contine on the same line as their neighboring elements 
examples are :
- <a>
- <b>
- <em>
- <img>

## Grouping Text & Elements in a Block
<div> 
allows you to group a set of elements together in one block-level box

## Grouping Text & Elements Inline
<span> 
acts like the inline equivalent to the <div> element

## Iframes
<iframe> "inline frame"
a window cut into your page and in that window you can see another page

- **src** --> specifies the URL of the page to show in the frame
- **height** --> specifies the height of the iframe in pixels
- **width** --> specifies the width of the iframe in pixels
- **scrolling** --> not available in HTML5 but allows the iframe to have a scroll bar. 
    - three options ( yes, no, and auto) 

- **frameborder** --> not supported in HTML5 indicates whether the frame should have a border or not. 
    - a value of "0" indicates no border, "1" indicates that a border should be shown
- **seamless** --> used where scrollbars are not desired, does not need a value

## Information About Your Pages
<meta> 
lives inside the <head> element and contains information about the webpage
- not visible to the user but contains a number of usefull purposes such as telling search engines about your page who created it, and whether or not it is time sensitive

#### descriptions
description of the page 

- words commonly used by search engines to understand what the page is about 
- maximum of 155 characters
- sometimes displayed in search engine results

#### keywords

- contains a list of comma separated words that a user might search on to find the page

#### robots 

- indicates whether search engines should add the page to their search results or not. 
- a value of "noindex" can be used if search engines shoudl add this page in their results but not any pages that it links to 

#### author
defines the author of the webpage

#### pragma
prevents the browser from caching the page 
    
 - saving it locally to save time downloading it on subsequent visits

#### expires
indicates when the page should expire and no longer be cached

## Escape Characters

- < Less than sign = &lt;
- > Greater than sign = &gt;
- & Ampersand = &amp;
- " Quotation marks = &quot;
- cent sign = &cent;
- Pound sign = &pound;
- Yen sign = &yen;
- Euro sign = &euro;
- Copyright symbol = &copy;
- Registered trademark = &reg;
- Trademark = &trade;
- left single quote = &lsquo;
- right single quote = &rsquo;
- left double quote = &ldquo;
- right double quote = &rdquo;
- multiplication sign = &times;
- division sign = &divide;