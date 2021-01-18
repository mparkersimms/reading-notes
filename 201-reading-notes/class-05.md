# Class 05 
## [Home Page](../README.md)

#### References:

HTML book by Duckett
- Chapter 5: “Images” (pp.94-125)
- Chapter 11: “Color” (pp.246-263)
- Chapter 12: “Text” (pp.264-299)

### Images 

- `<img>` To add an image into the page you need to use an `<img>` element. This is an empty element (which means there is no closing tag). It must carry the following two attributes:

    - src 
        - This tells the browser where it can find the image file. This will usually be a relative URL pointing to an image on your own site. (Here you can see that the images are in a child folder called images relative URLs were covered on pages 83-84).
    - alt 
        - This provides a text description of the image which describes the image if you cannot see it.
    - title 
        - You can also use the title attribute with the ``<img>`` element to provide additional information about the image. Most browsers will display the content of this attribute in a tootip when the user hovers over the image.
    - height
        - This specifies the height of the image in pixels.
    - width
        - This specifies the width of the image in pixels. Images often take longer to load than the HTML code that makes up the rest of the page. It is, therefore, a good idea to specify the size of the image so that the browser can render
    - align
        - The align attribute was commonly used to indicate how the other parts of a page should flow around an image

- `<figure>`
    - Images often come with captions. HTML5 has introduced a new `<figure> `element to contain images and their caption so that the two are associated. You can have more than one image inside the `<figure>` element as long as they all share the same caption.
- `<figcaption>`
    - The `<figcaption>` element has been added to HTML5 in order to allow web page authors to add a caption to an image.

## Tables

- `<table>`
    - The `<table>` element is used to create a table. The contents of the table are written out row by row.
- `<tr>`
    - You indicate the start of each row using the opening `<tr>` tag. (The tr stands for table row.) It is followed by one or more ``<td>`` elements (one for each cell in that row). At the end of the row you use a closing `</tr>` tag.
- ``<td>``
    - Each cell of a table is represented using a ``<td>`` element. (The td stands for table data.) At the end of each cell you use a closing `</td>` tag. Some browsers automatically draw lines around the table and/or the individual cells. 
- `<th>`
    - The `<th>` element is used just like the `<td>` element but its purpose is to represent the heading for either a column or a row. (The th stands for table heading.) Even if a cell has no content, you should still use a `<td>` or `<th>` element to represent the presence of an empty cell otherwise the table will not render correctly

- `<thead>`
    - The headings of the table should sit inside the `<thead>` element.
- `<tbody>`
    - The body should sit inside the `<tbody>` element.
- `<tfoot>`
    - The footer belongs inside the `<tfoot>` element.


### Foreground   
"color"  
allows you to specify the color of the text on a specific   
- can be specified in three ways
    - RGB values
    - Hex codes
    - Color names 

### Background   
"background-color"  
-same three ways, RGB, Hex, Color name

#### RGB values  
-Values for Red, Green, and Blue  
between 0 and 255  
eg. "rgb(102,205,170)

#### Hex Codes 
-represent values for red, green, and blue in hexidecimal code  
eg. (#66cdaa)  

#### Color names
-147 different color names supported by browsers

#### Hue
-the colloquial idea of the color

#### Saturation
-amount of grey in the color

#### Brightness
-how much black is in the color

### Contrast
-the difference between the forground color and the background color

### CSS3: Opacity
"opacity, rgba"
between the values of 0.0 and 1.0  
(0.5 is 50% opacity and 0.15 is 15% opacity)  

### CSS3: HSL Colors
Hue - colloquial idea of the color
- value between 0- 360  

Saturation- amount of gray in the color 
- 100% is full saturation, 
- 0% is the shade of gray

### CSS3: HSL & HSLA   
"hsl, hsla"  
Example: backgound_color: hsla(0, 100%, 100%, 0.5)  
Stands for hue, saturation, and lightness and alpha  
**Alpha** is transparency   
-values between 0 and 1.0


## Text

- font-family
The font-family property allows you to specify the typeface that should be used for any text inside the element(s) to which a CSS rule applies.
The value of this property is the name of the typeface you want to use.
The people who are visiting your site need the typeface you have specified installed on their computer in order for it to be displayed.

- font-size
The font-size property enables you to specify a size for the
font. There are several ways to specify the size of a font. The most common are:
pixelS
Pixels are commonly used because they allow web designers very precise control over how much space their text takes up. The number of pixels is followed by the letters px.
percenTageS
The default size of text in browsers is 16px. So a size of 75% would be the equivalent of 12px, and 200% would be 32px.
If you create a rule to make all text inside the <body> element to be 75% of the default size (to make it 12px), and then specify another rule that indicates the content of an element inside the <body> element should be 75% size, it will be 9px (75% of the 12px font size).
- emS
An em is equivalent to the width of a letter m.

- @font-face
@font-face allows you to use
a font, even if it is not installed on the computer of the person browsing, by allowing you to specify a path to a copy of the font, which will be downloaded if it is not on the user's machine.
Because this technique allows
a version of the font to be downloaded to the user's computer, it is important that the license for the font permits it to be used in this way.

- font-family
This specifies the name of the font. This name can then be used as a value of the font-family property in the rest of the style sheet (as shown in the rule for the <h1> and <h2> elements).
src
This specifies the path to the font. In order for this technique to work in all browsers, you will probably need to specify paths to a few different versions of the font, as shown on the next page.
format
This specifies the format that the font is supplied in
- font-weight
The font-weight property allows you to create bold text. There are two values that this property commonly takes:
normal
This causes text to appear at a normal weight.
bold
This causes text to appear bold.
In this example, you can see that the element whose class attribute has a value of credits has been bolded.
- font-style
If you want to create italic text, you can use the font-style property. There are three values this property can take:
normal
This causes text to appear in a normal style (as opposed to italic or oblique).
italic
This causes text to appear italic.
oblique
This causes text to appear oblique.
In this example, you can see that the credits have been italicized.
- text-transform
The text-transform property is used to change the case of text giving it one of the following values:
uppercase
This causes the text to appear uppercase.
lowercase
This causes the text to appear lowercase.
capitalize
This causes the first letter of each word to appear capitalized.
In this example, the <h1> element is uppercase, the <h2> element is lowercase, and the credits are capitalized. In the HTML, the word by in the credits had a lowercase b.
- text-decoration
The text-decoration property allows you to specify the following values:
none
This removes any decoration already applied to the text.
underline
This adds a line underneath the text.
overline
This adds a line over the top of the text.
line-through
This adds a line through words.
blink
This animates the text to make it flash on and off (however this is generally frowned upon, as it is considered rather annoying).
In this example, the credits have been underlined.
- line-height
Leading (pronounced ledding) is a term typographers use for the vertical space between lines of text. In a typeface, the part of
a letter that drops beneath the baseline is called a descender, while the highest point of a letter is called the ascender. Leading
is measured from the bottom of the descender on one line to the top of the ascender on the next

- letter-spacing, word-spacing
Kerning is the term typographers use for the space between each letter. You can control the space between each letter with the letter-spacing property.
It is particularly helpful to increase the kerning when your heading or sentence is all in uppercase. If your text is in sentence (or normal) case, increasing or decreasing the kerning can make it harder to read.
You can also control the gap between words using the word-spacing property.
- text-align
The text-align property allows you to control the alignment of text. The property can take one of four values:
left
This indicates that the text should be left-aligned.
right
This indicates that the text should be right-aligned.
center
This allows you to center text.
justify
This indicates that every line in a paragraph, except the last line, should be set to take up the full width of the containing box.
- vertical-align
The vertical-align property is a common source of confusion. It is not intended to allow you to vertically align text in the middle of block level elements such as <p> and <div>, although it does have this effect when used with table cells (the <td> and <th> elements).
It is more commonly used with inline elements such as <img>, <em>, or <strong> elements. When used with these elements, it performs a task very similar to the HTML align attribute used on the <img> element, which you met on pages 103-106. The values it can take are:
                                               baseline
                                               sub
                                               super
                                               top
                                               text-top
                                               middle
                                               bottom
                                               text-bottom

- text-indent
The text-indent property allows you to indent the first line of text within an element. The amount you want the line indented by can be specified in a number of ways but is usually given in pixels or ems.
It can take a negative value, which means it can be used
to push text off the browser window. You can see this technique used in this example, where the <h1> element uses a background image to represent the heading. The text has been moved far to the left, off the screen.
- text-shadow
The text-shadow property has become commonly used despite lacking support in all browsers.
It is used to create a drop shadow, which is a dark version of the word just behind it and slightly offset. It can also be used to create an embossed effect by adding a shadow that is slightly lighter than the text.
The value of this property is quite complicated because it can take three lengths and a color for the drop shadow.
- :first-letter, :first-line
You can specify different values for the first letter or first line of text inside an element using :first-letter and :first-line.
Technically these are not properties. They are known as pseudo-elements.
 - :link, :visited
Browsers tend to show links
in blue with an underline by default, and they will change the color of links that have been visited to help users know which pages they have been to.
In CSS, there are two pseudo- classes that allow you to set different styles for links that have and have not yet been visited.
:link
This allows you to set styles for links that have not yet been visited.
:visited
This allows you to set styles for links that have been clicked on.
They are commonly used to control colors of the links and also whether they are to appear underlined or not.
- :hover, :active, :focus
There are three pseudo-classes that allow you to change the appearance of elements when a user is interacting with them.
:hover
This is applied when a user hovers over an element with a pointing device such as a mouse. This has commonly been used to change the appearance of links and buttons when a user places their cursor over them. It is worth noting that such events do not work on devices that use touch screens (such as the iPad) because the screen is not able to tell when someone is hovering their finger over an element.
:active
This is applied when an element is being activated by a user; for example, when a button is being pressed or a link being clicked. Sometimes this is used to make a button or link feel more like it is being pressed by changing the style or position of the element slightly.
:focus
This is applied when an element has focus. Any element that you can interact with, such as a link you can click on or any form control can have focus.