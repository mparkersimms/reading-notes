# Structure Webpages with HTML

#### Table of Contents
* [README](README.md)
* [Growth Mindset](Growth-Mindset.md)
* [Markdown](markdown.md)
* [Coders Computer](coders-computer.md)
* [Git-Tutorial](Git_Tutorial.md)
* [Structure web pages](Structure_webpages.md)

# Process &amp; Design

references: 
Chapter 18, HTML &amp; CSS by Duckett

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
Chapter 17, HTML &amp; CSS by Duckett

## New HTML5 Layout Elements 
HTML5 introduces a new set of elements that allow you to divide the parts of a page and eliminates many "div" elements

## Headers and Footers
&amp;lt;header> &amp;lt;/header>
&amp;lt;footer>&amp;lt;/footer>
appear on the top and the bottom of a web page or possibly even an &amp;lt;article> or &amp;lt;section>

## Navigation
&amp;lt;nav>

Used to contain the major navigational blocks on the site such as the primary site navigation

## Articles
&amp;lt;article>

- acts as a container for any section of a page that could *stand alone* or be syndicated
- an independent piece of content

## Asides
&amp;lt;aside>
has two purposes
    - inside an &amp;lt;article>
        - should contain information that is related to the article but not essential to its overall meaning
    - outside of an &amp;lt;article>
        - acts as a container that is related to the entire page

## Sections
&amp;lt;section>
groups related content together and typically has its own heading
    - may have one or many &amp;lt;article> elements in them 

## Heading Groups
&amp;lt;hgroup>
purpose is to group together a specific set of &amp;lt;h1> through &amp;lt;h6> elements 

## Figures
&amp;lt;figure> &amp;lt;figcaption>
can be used to contain any content that is referenced from the main flow of an article (not just images)
used for something that only references content not something that is integral to the flow of the page
examples:
- images
- videos
- graphs
- diagrams
- code samples
- text that supports the main body of an article
should also contain &amp;lt;figcaption> which provides a description of what is in the &amp;lt;figure> element

## Sectioning Elements 
&amp;lt;div> 
When there is no other wrapper for a specific set of elements use the &amp;lt;div> still 
example would be to contain all the information on a page
*everyting that is not contained inside a &amp;lt;header> &amp;lt;footer> or &amp;lt;aside> is considered as the main content

## Linking Around Block-Level Elements 
HTML5 allows you to place a &amp;lt;a> element around a block level element that contains child elements and makes the entire block a link




# Extra Markup
Reference:
Chapter 8, HTML &amp; CSS by Duckett

## Doctypes 
&amp;lt;!DOCTYPE html> 
becuase of several versions of HTML created every webpage needs to start with a DOCTYPE to determine what language the webpage is written in 

## Comments in HTML
&amp;lt;!-- --> 
&amp;lt;!-- comments go here -->
will not display on the webpage unless the user is viewing the source code 
used to explain certain things in the code, or to assist in explaining what is going on in the code. 

## ID Attribute
&amp;lt;p id="uniqueattribute">

- should only start with a *letter* or an *underscore* nothing else and should be have a unique id. 
- nothing else on that page should have the same id, it would then not be unique
- allows that unique group to be formatted using CSS differently than everything else on the page
- also called a **global attribute** becuase it can be used on any element

## Class Attribute
&amp;lt;p class="somethingdescriptive">
its a way to uniquely identify a group of elements the same way
separate names with a space to indicate that a particual element has more than one class attribute eg &amp;lt;p class="somethingdescriptive somethingelse">

## Block Elements 
elements that appear to always start on a new line in a browser window
examples are : 
- &amp;lt;h1>
- &amp;lt;p>
- &amp;lt;ul>
- &amp;lt;li>

## Inline Elements 
elements that always appear to contine on the same line as their neighboring elements 
examples are :
- &amp;lt;a>
- &amp;lt;b>
- &amp;lt;em>
- &amp;lt;img>

## Grouping Text &amp; Elements in a Block
&amp;lt;div> 
allows you to group a set of elements together in one block-level box

## Grouping Text &amp; Elements Inline
&amp;lt;span> 
acts like the inline equivalent to the &amp;lt;div> element

## Iframes
&amp;lt;iframe> "inline frame"
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
&amp;lt;meta> 
lives inside the &amp;lt;head> element and contains information about the webpage
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

- &lt; Less than sign = &amp;lt;
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