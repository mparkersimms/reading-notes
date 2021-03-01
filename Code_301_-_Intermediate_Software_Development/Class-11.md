# EJS

## References

https://www.youtube.com/watch?v=IqpfBGsALqc&list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt&index=1

## Using EJS 

### Getting started 

install EJS from command line using `npm install -S EJS`

then in server.js 

```
const path = require('path')

app.set('views', path.join(__dirname, 'views'));
app.set('vew engine' , 'ejs' );

app.get('/', function(request, response));
 response.render('index');

app.listen(3000, console.log('up on 3000'))
```

set the views folder to handle all of the views, 
set the views engine to ejs npm package

Then when nodemon listens to the server, it will populate whats in the index.ejs file on the page of the server. 

### Injecting values

the response.render takes 3 parameters (string of the file name, an object of local variables, and a callback function)

so, create an object of local variables 
``` 
response.render('index', {
   foo: 'bar', 
})
```
now go to the index.ejs file and apply the ejs syntax to add  <%= foo %> to the file;

### For loops and arrays

changing the object of one key value pair, to an array of objects :
```
response.render('index', [
    { name: 'barry'},
    { name: 'jerry'}
]);
```
Then on the index.ejs file and getting rid of the text, and add a `<ul><li></li></ul>`
apply the <% for(var person of peopel){ %>
<% } %>

getting the for loop to populate on the server page. 

### If/else statements

working on the index.ejs adding an if/else statement written in ejs, and allowing the logic to display what is written in the .js file. 



