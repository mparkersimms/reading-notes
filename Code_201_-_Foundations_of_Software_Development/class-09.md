# Class 09 
## [Home Page](../README.md)

#### References:

HTML book by Duckett
- Chapter 7 "Forms" (p144-175)
- Chapter 14 "Lists, Tables & Forms" (pp330 - 357)

JS book by Duckett
- Chapter 6 "Events" (pp.243-292)

## Forms

Adding Text:
- Text input (single line)
- Password input
- Text area (multi line)

Making Choices
- Radio Buttons
- Checkboxes
- Drop-down boxes

Submitting Forms
- Submit buttons
- Image buttons
- File upload

Form Structure
`<form>`
- Form controls live inside a `<form>` element. This element should always carry the action attribute and will usually have a method and id attribute too.
`action`
- Every `<form>` element requires an action attribute. Its value is the URL for the page on the server that will receive the information in the form when it is submitted.
`method`
- Forms can be sent using one of two methods: get or post.

Text Input
`<input>`
- The `<input>` element is used to create several different form controls. The value of the type attribute determines what kind of input they will be creating.
- `type="text"`
When the type attribute has a value of text, it creates a single- line text input.
- `name`
When users enter information into a form, the server needs to know which form control each piece of data was entered into.
- `size`
The size attribute should not be used on new forms. It was used in older forms to indicate the width of the text input

- `maxlength`
You can use the maxlength attribute to limit the number
of characters a user may enter into the text field. Its value is the number of characters they may enter.

Password Input
- `<input>`
`type="password"`
- When the type attribute has
a value of password it creates a text box that acts just like a single-line text input, except the characters are blocked out.
- `name`
- The name attribute indicates the name of the password input, which is sent to the server with the password the user enters.

-` size, maxlength`
- It can also carry the size and maxlength attributes like the the single-line text input.

Text Area
- The `<textarea>` element is used to create a mutli-line
text input. Unlike other input elements this is not an empty element. It should therefore have an opening and a closing tag.

Radio Button
- `<input>`
- `type="radio"`
- Radio buttons allow users to pick just one of a number of `option`s.

- `name` The name attribute is sent to the server with the value of the `option` the user selects

- `value` The value attribute indicates the value that is sent to the server for the selected `option`.

- `checked` The checked attribute can be used to indicate which value (if any) should be selected when the page loads

Checkbox
- `<input>` 
- `type="checkbox"`
Checkboxes allow users to select (and unselect) one or more `option`s in answer to a question.
- `name` The name attribute is sent to
the server with the value of the `option`(s) the user selects.

- `value` The value attribute indicates the value sent to the server if this checkbox is checked.

- `checked` The checked attribute indicates that this box should be checked when the page loads. If used, its value should be checked.

Drop Down List Box

- `<select>` A drop down list box (also known as a select box) allows users to select one `option` from a drop down list.

- `name` The name attribute indicates the name of the form control being sent to the server, along with the value the user selected.

- <`option`> The <`option`> element is used to specify the `option`s that the user can select from. The words between the opening <`option`> and closing </`option`> tags will be shown to the user in the drop down box.

- `value` The <`option`> element uses the value attribute to indicate the value that is sent to the server along with the name of the control if this option is selected.

Multiple Select Box
- `<select>`

- `size` You can turn a drop down select box into a box that shows more than one option by adding the size attribute. Its value should be the number of options you want to show at once. In the example you can see that three of the four options are shown.

- `multiple` You can allow users to select multiple options from this list by adding the multiple attribute with a value of multiple.

File Input Box
- `<input>` If you want to allow users to upload a file (for example an image, video, mp3, or a PDF), you will need to use a file input box.

- `type="file"` This type of input creates a box that looks like a text input followed by a browse button. When the user clicks on the browse button, a window opens up that allows them to select a file from their computer to be uploaded to the website.

Submit Button

- `type="submit"`The submit button is used to send a form to the server.
- `name` It can use a name attribute but it does not need to have one.

- `value` The value attribute is used to control the text that appears on a button. It is a good idea to specify the words you want to appear on a button because the default value of buttons on some browsers is ‘Submit query’ and this might not be appropriate for all kinds of form.

Image Button 
- `type='image'`- If you want to use an image for the submit button, you can give the type attribute a value of image

Button & Hidden Controls
- `<button>`  element was introduced to allow users more control over how their buttons appear, and to allow other elements to appear inside the button.

- `<input>`
`type="hidden"` This example also shows a hidden form control. These form controls are not shown on the page (although you can see them if you use the View Source option in the browser). They allow web page authors to add values to forms that users cannot see.

Labelling Form Control 

- `<label>` - When introducing form controls, the code was kept simple by indicating the purpose of each one in text next to it. However, each form control should have its own `<label> `element as this makes the form accessible to vision-impaired users.

- `for` The for attribute states which form control the label belongs to. Note how the radio buttons use the id attribute. The value of the id attribute uniquely identifies an element from all other elements on a page4

- `<fieldset>`- You can group related form controls together inside the `<fieldset>` element. This is particularly helpful for longer forms.

- `<legend>`
- The <legend> element can come directly after the opening <fieldset> tag and contains a caption which helps identify the purpose of that group of form controls.


## Lists, Tables and Forms

Bullet point styles
- `list-style-type`-
    - Unordered Lists
        - none disc circle square

    - ordered Lists
        - decimal
- 123
- decimal-leading-zero
- 01 02 03
- lower-alpha
- abc
- upper-alpha
- ABC
- lower-roman
- i. ii. iii.
- upper-roman
- I II III
Images for bullets

- url and is followed by a pair of parentheses
- 

Positioning the Marker
- `list-style-position`
    - inside 
    - outside

list shorthand

- list-style
- example - `list-style: inside circle;
  width: 300px;}`

  - table properties
    - width, padding, text-transform, letter-spacing, font-size etc. 

- empty-cells
    - show, hide, inherit

- gaps between cells, 
    - `border-spacing, border-collapse`
    - collapse, 
    - separate

Cursor styles

- auto
- crosshair, default, pointer, move, text, wait, help, url("cursor.gif")

- web developer toolbar
- outlines, 
- structure, 
- css styles


## Events

- INTERACTIONS CREATE EVENTS
- EVENTS TRIGGER CODE
- CODE RESPONDS TO USERS


- events
    - load, 
    - unload, 
    - error, 
    - resize
    - scroll

- keyboard events
    - keydown, 
    - keyup
    - keypress

- Mouse events
    - click
    - dblclick
    - mousedown
    - mouseup
    - mousemove
    - mouseover
    - mouseout

- Terminology 
    - events fire or are raised
    - events trigger scripts

- focus events
    - focus/focusin
    - blur, focusout

form events
- input
- change
- submit
- reset
- cut
- copy
- paste
- select

Mutation events
- DOMSubtreeModified
- DOMNodeInserted
- DOMNodeRemoved
- DOMNodeInsertedIntoDocument
- DOMNodeRemovedFromDocument

How events trigger scripts
- select the element
- indicate which event will trigger response
- state the code you want to run

Three ways to bind an event ot an element
- hHTML handlers
- Traditional DOM event Handlers
- DOM level 2 Event Listeners

Event listeners
- deal with more than one function at a time

Using an event listener

The event Object
- when an event occurs the event object tells you information about the event and the element it happened upon

Event Delegation
- creating event listeners for a lot of elements can slow down a page but event flow allows you to listen for an event on a parent element
Changing default behavior
- the event object has methods that change, the default behavior of an element and how the element ancestors respond to the event

Focus and Blur events
- The HTML elements you can interact with, such as links and form elements, can gain focus, these events fire when they gain or lose focus

Mouse events
- the mouse events are fired when the mouse is moved and also when its buttons are clicked

Where events occur, 
- the event object can tell you where the cursor was positioned when an event was triggered
    - screen, page, client

Keyboard events
- the keyboad events are fired when a user interacts with the keyboard 


Mutation events and observers
- Whenever elements are added to or removed from the DOM, its structre changes, this change triggers a mutation event


