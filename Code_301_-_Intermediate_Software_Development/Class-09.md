# Class 09 

## References

https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa

https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec

## Concepts of Functional Programming in Javascript
by TK Nov 25, 2018

“Complexity is anything that makes software hard to understand or to modify." — John Outerhout

### What is functional programming?

Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data — Wikipedia

#### Pure functions

What makes a function pure?
- It returns the same result if given the same arguments (it is also referred as deterministic)
- It does not cause any observable side effects

#### impure functions
- If our function reads external files, it’s not a pure function

- Any function that relies on a random number generator cannot be pure.

- examples of observable side effects include modifying a global object or a parameter passed by reference.

### Immutability 

Unchanging over time or unable to be changed.

- if you want to change an immutable object, you have to creat a new object with the new value

### Referential transparency

"pure functions + immutable data = referential transparency"

### Functions as first-class entities

- functions are also treated as values and used as data.

- Functions as first-class entities can:
    - refer to it from constants and variables
    - pass it as a parameter to other functions
    - return it as result from other functions

### Higher-order functions

a function that takes one or more functions as arguments, or returns a function as its result

- Filter - Given a collection, we want to filter by an attribute
    - expects a true or false value to determine if the element should or should not be included in the result collection

    
```

var filterArray = function(x, coll) {
  var resultArray = [];

  for (var i = 0; i < coll.length; i++) {
    if (coll[i] < x) {
      resultArray.push(coll[i]);
    }
  }

  return resultArray

console.log(filterArray(3, [10, 9, 8, 2, 7, 5, 1, 3, 0])); // (3) [2, 1, 0];

```
can be written like this using "filter"
```
function smaller(number) {
  return number < this;
}

function filterArray(x, listOfNumbers) {
  return listOfNumbers.filter(smaller, x);
}

let numbers = [10, 9, 8, 2, 7, 5, 1, 3, 0];

filterArray(3, numbers); // [2, 1, 0]

```

- map
    - The map method transforms a collection by applying a function to all of its elements and building a new collection from the returned values.

    turning this: 

``` 
    var people = [
  { name: "TK", age: 26 },
  { name: "Kaio", age: 10 },
  { name: "Kazumi", age: 30 }
];

var peopleSentences = [];

for (var i = 0; i < people.length; i++) {
  var sentence = people[i].name + " is " + people[i].age + " years old";
  peopleSentences.push(sentence);
}

console.log(peopleSentences); // ['TK is 26 years old', 'Kaio is 10 years old', 'Kazumi is 30 years old']

```
into this :
```
const makeSentence = (person) => `${person.name} is ${person.age} years old`;

const peopleSentences = (people) => people.map(makeSentence);
  
peopleSentences(people);
// ['TK is 26 years old', 'Kaio is 10 years old', 'Kazumi is 30 years old']
```

- reduce

The idea of reduce is to receive a function and a collection, and return a value created by combining the items.
turning this:
```
var orders = [
  { productTitle: "Product 1", amount: 10 },
  { productTitle: "Product 2", amount: 30 },
  { productTitle: "Product 3", amount: 20 },
  { productTitle: "Product 4", amount: 60 }
];

var totalAmount = 0;

for (var i = 0; i < orders.length; i++) {
  totalAmount += orders[i].amount;
}

console.log(totalAmount); // 120
```
into this:

```
let shoppingCart = [
  { productTitle: "Product 1", amount: 10 },
  { productTitle: "Product 2", amount: 30 },
  { productTitle: "Product 3", amount: 20 },
  { productTitle: "Product 4", amount: 60 }
];

const sumAmount = (currentTotalAmount, order) => currentTotalAmount + order.amount;

const getTotalAmount = (shoppingCart) => shoppingCart.reduce(sumAmount, 0);

getTotalAmount(shoppingCart); // 120
```





