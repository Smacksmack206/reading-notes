#Cedric's Notes for code-201n24 course

# <cite> https://betterprogramming.pub </cite>

## Classifying JavaScript’s Eight Data Types

JavaScript currently supports eight different data types. This includes seven primitive value types and objects. Here’s the full list.

- Boolean
- Null
- Undefined
- Number
- BigInt
- String
- Symbol
- Objects

 **Arrays, functions, and dates** all play an important role in JavaScript programs, but they are really just objects under the hood.

## The Difference Between Immutable and Mutable Data

The Difference Between Immutable and Mutable Data

Put simply, this means that primitive values cannot be changed (or mutated), but object references can be changed.

### An example of immutable data

First, let’s look at an immutable data type — strings. To begin we will create a variable, word, and assign a value to it.

`let word = 'snow'`

The variable now exists in memory and you can access individual letters of the string by using square bracket notation. If I wanted to get the first letter, for example, I could check for the value in the 0 index and log it to the console.

`console.log(word[0]) // "s"`

You can’t change the string because it is immutable.

If you need to get around this constraint you have to create a new string from the old one and reassign the word variable with that new value:

```word = `k${word.slice(1)}`
console.log(word) // "know"```

## An example of mutable data

Next, let’s look at a mutable data type, arrays. Again — arrays are really just special objects in JavaScript.

``` let letters = ['s', 'n', 'o', 'w']
letters[0] = 'k'
console.log(letters) // (4) ["k", "n", "o", "w"] ```

Since arrays are mutable you can alter them directly. There’s no need to assign a new value to letters since you can just change the existing array directly.

Aside: the code written above used the let keyword to create the letters variable, but you could define the variable with const and the result would still be the same. const prevents you from reassigning values, but it does not prevent you from mutating existing values.

If you want to create a new object instead of a second reference to the same object (as we did above), you should use Object.assign instead:

```let lead = {
  name: 'John Lennon',
  group: 'The Beatles'
}
let coLead = Object.assign({}, lead, {
  name: 'Paul McCartney'
})
console.log(lead, coLead)
// {name: "John Lennon", group: "The Beatles"}
// {name: "Paul McCartney", group: "The Beatles"}```

The first argument that Object.assign accepts is the target object. Any arguments provided after this are source objects that will have their properties copied onto that target.

In the example above a new object ({})is created as the target (first argument), and then each property from the lead object is applied to it (second argument), and then a new name property (‘Paul McCartney’) is applied as well (third argument).

This approach allows you to copy one object from another and still keep the original object unchanged.

Object references, on the other hand, do not contain values directly — they contain references.

 This causes equality checks with objects to give results that may not be intuitive to new developers:

``` { name: 'Moe Szyslak' } === { name: 'Moe Szyslak' } // false
[] === [] // false
new Date(0) === new Date(0) // false
NaN === NaN // false (NaN is another type of object)``` 

In all four of the object comparison checks above, a new object is created on both the left and the right of the === operator. Even though the contents of the left side are the same as the contents on the right side, the reference, or memory address that the contents are stored at, is different. This is why the comparison is found to be false in each case.

If you create a duplicate reference to the same object, you will see that the equality check is now found to be true:

```let lead = {
  name: 'John Lennon',
  group: 'The Beatles'
}
let coLead = lead
console.log(lead === coLead) // true```

In order to check whether the contents (not the reference) of two objects are the same you need to either:

Iterate through the object and check that each key and value match. This can be tricky because an object’s property can be an object in itself.

Convert the object to a suitable primitive before doing the equality check.

Here’s an example of how object literals can be converted to strings for comparison. 

This should be thought of as a quick-and-dirty approach, but I often find it handy.

```const moeA = { name: 'Moe Szyslak' }
const moeB = { name: 'Moe Szyslak' }
moeA === moeB // false
JSON.stringify(moeA) === JSON.stringify(moeB) // true```

And here is how dates, for example, could be converted to numbers for comparison:

```const dateA = new Date(0)
const dateB = new Date(0)
dateA === dateB // false
dateA.getTime() === dateB.getTime() // true```


# <cite> Reading from the Jon Duckett Js book </cite>

## Object Literals (pp.100-105)

In an Object, Variables Become Known As Properties.

In an Object, Functions become known as methods.

### Creating An Object: Literal Notation

#### Literal notation is the easiest and most popular way to create objects. (There are serveral ways to create objects.)

The objects is the curly braces and their contents.

Seperate each key from its value using a colon. Serpate each property and method with a comma.

### Accessing an object and Dot Notation

You can access the properties and methods of an object using dot notation.

You can also acess properties using square brackets

```var hotelName = hotel.name;
var roomsFree = hotel.checkAvailability();

var hotelName = hotel[name];
var roomsFree = hotel[checkAvailability]();```

## Document Object Model (pp.183-242)


### Working with the DOM Tree

Accessing and updating the DOM tree involes two steps:

1: Locate the node that repeprsents the elements you want to work with.

2: Use its text context, child elements, and attributes.

Here is an overview of the methods and properties that traverse the DOM and Access it.

#### Select An Indivadual Element Node

Here are three common ways to select an individual element:

getElementById()
Uses the value of an element's id attribute (which should be unique within the page)

querySelector()
Uses a CSS selector, and reutrns the first matching element.

You can also select indivdual element by traversing from one element to another within the DOM tree.

#### Select Multiple Elements (NODELISTS)

There are three common ways to select multiple elements

getElementsByClassName()
Selects all elements that have a specific value for their class attribute

getElementsByTagName()
Selects all elements that have the specified tag name.

querySelectorAll()
Uses a CSS selector to select all matching element

#### Traversing Between ELements Nodes

You can move from one element node to a related element node.

parentNode
Select the parent of the current element node (which will return just one element)

previousSibling/ nextSibling
Selects the previous or next sibling from the DOM tree.

firstChild/ lastChild
Select the first or last child of the current element.

#### Access/ Update Text Nodes

The text inside any elemetn is stored next to a text node 
to access the text node
1. Select the <li> element
2. Use the firstChild property to get the text node
3. Use the text node's only property (nodeValue) to get the text from the element

nodeValue
This property lets you access or update content of a text.

Work with HTML Content

One property allows access to child elemts and text content:

innerHTML

Another just the text content:
textContent

Several methods let you create new nodes, add nodes to a tree, and remove nodes from a treeL

createElement()
createTextNode()
appendChild() / removeChild()

This called DOM manipulation.

Access or update attribute values

Here are some of the properties and methods you can use to work with attributes:

className / id

Lets you get or update the value of the class and id attributes.

```hasAttribute()
getAttribute()
setAttribute()
removeAttribute()```

The first checks if an attribute exists. 
The second get its value.
The third updates the value.
The fourth removes an attribute.

### Selecting an element from a NODELIST

There are two ways to slect an element from a NODELIST:

The `item()` Method

example:

``` var firstItem = pets.item(0)```

#### From an element node you can access and update its content using properties such as textContent and innerHTML or using DOM manipulation techniques.

#### Notes to self

Revisit p.240-241 in Js book for a great overview of DOM and ways of accessing and manipulating it.