# Class 07 
## [Home Page](../README.md)

#### References:

HTML book by Duckett
- Chapter 6 "Tables" (pp.126-145)
JS book by Duckett
- Chapter 3: “Functions, Methods and Objects” (pp.106-144)


## Domain Models
-   some tips to follow when building your own domain models.

    - When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.
    - Model its attributes with a constructor function that defines and initializes properties.
    - Model its behaviors with small methods that focus on doing one job well.
    - Create instances using the new keyword followed by a call to a constructor function.
    - Store the newly created object in a variable so you can access its properties and methods from outside.
    - Use the this variable within methods so you can access the object's properties and methods from inside.

## Tables
- `<table>`
    - The `<table>` element is used to create a table. The contents of the table are written out row by row.
- `<tr>` 
    - You indicate the start of each row using the opening `<tr>` tag. (The tr stands for table row.)
    - It is followed by one or more `<td>` elements (one for each cell in that row).
    - At the end of the row you use a closing `</tr>` tag.
- `<td>`
    - Each cell of a table is represented using a `<td>` element. (The td stands for table data.)
    - At the end of each cell you use a closing `</td>` tag.
    - Some browsers automatically draw lines around the table and/or the individual cells. 
- ``<th>``
    - The ``<th>`` element is used just like the `<td>` element but its purpose is to represent the heading for either a column or a row.
    - The `colspan` attribute can be used on a ``<th>`` or `<td>` element and indicates how many columns that cell should run across.
    - The `rowspan` attribute can be used on a `<th>` or `<td>` element to indicate how many rows a cell should span down the table.
- `<thead>`
    - The headings of the table should sit inside the `<thead>` element.
-  <`tbody`>
    - The body should sit inside the <`tbody`> element.
- <`tfoot`>
    - The footer belongs inside the <`tfoot`> element.


## Constructing an Object:

- ``
    var hotel = new Object();
        hotel.name = 'Quay'
        hotel.rooms = 40;
        hotel.booked = 25;
        hotel.checkAvailability = function(){
            return this.rooms - this.booked;
    };
    ``
- updating object
    - ` hotel.name = 'Park';`
    - `hotel['name'] = 'Park';`
- delete a property
    - `delete hotel.name;`
- clear a value 
    - `hotel.name = ''`

- constructor notations
    - ``function Hotel(name, rooms, booked) {
        this.name = name;
        this.rooms = rooms;
        this.booked = booked;
        this.checkavailability = function(){
            return this.rooms - this.booked;
        };
    }``

    - creating instances of the object using the constructor function:
        - `var quayHotel = new Hotel('Quay', 40, 25);`
        - `var parkHotel = new Hotel('Park', 120,77);`

- This is a key word
    - can be used to find value for some key in a function that it belongs, or in the global sense. 

- Arrays are object\
    - hold a related set of key/value pairs

    - object :
    `` costs = {
        room1: 420,
        room2: 460,
        room3: 230,
    } ``
    - array :
    ``costs = [420, 460, 230];

- arrays of object And objects in array
    - ``cost = {
        room1: items[420,40,10],
        room2: items[440,10,30],
        room3: items[230,0,0],
    }``
    - `` cost = [ {accom: 420, food: 40, phone:10}, {accom: 440, food: 10, phone:30 }, {accom: 420, food: 40, phone:10}
    ]
- The window object
    - `window . innerHeight` 
    - `window.innerWidth` 
    - `window.pageXOffset` 
    - ` window.screenX` 
    - `window . screenY` 
    - `window.location`
    - `window.document`
     - `window.history`
    - `window.a1ert ()` 
    - `window. open ()`

- The browser Object
    - `document.title` 
    - `document.lastModified` 
    - `document . URL `
