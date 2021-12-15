#Cedric's Notes for code-201n24 course

## <cite> https://github.com/codefellows/domain_modeling#domain-modeling </cite>

### Domain Modeling
Domain modeling is the process of creating a conceptual model in code for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model.

A domain model that's articulated well can verify and validate the understanding of a specific problem among various stakeholders. As a communication tool, it defines a vocabulary that can be used within and between both technical and business teams.

### Define a constructor and initialize properties
To define the same properties between many objects, you'll want to use a constructor function. Below is a table that summarizes a JavaScript representation of an EpicFailVideo object.

| Property      |    Data     |    Type   |
| -----------   | ----------- |-----------|
| epicRating    | 1 to 10     |   Number  |
| hasAnimals    | true or false | Boolean |

### Here's an implementation of the EpicFailVideo constructor function.

```var EpicFailVideo = function(epicRating, hasAnimals) {
  this.epicRating = epicRating;
  this.hasAnimals = hasAnimals;
}

var parkourFail = new EpicFailVideo(7, false);
var corgiFail = new EpicFailVideo(4, true);

console.log(parkourFail);
console.log(corgiFail);``` 

As you can see, the constructor function is defined using a function expression. In other words, the variable EpicFailVideo is declared and then assigned a function with two parameters called epicRating and hasAnimals.

When the function is called, the data inside these parameters are stored inside the this.epicRating and this.hasAnimals properties respectively. Storing data within properties ensures any newly created object can access that data later.

After the constructor function definition, two objects are instantiated with the new keyword and their properties are initialized by calling the EpicFailVideo constructor function. After being instantiated and initialized, these objects are stored inside the parkourFail and corgiFail variables.



# <cite> Reading from the Jon Duckett HTML book </cite>

## Chapter 6: “Tables” (pp.126-145)

### Basic Table

` <table> `
Is used to create a table, the contents of the table are written out row by row.

` <tr> `
You indicate the start of each row using the opening <tr> tag.
(The tr stands for table row.)

` <td> `
Each cell of a table is represented using a <td> element. (The td stands for table data.)

At the end of each cell you use a closing </td> tag.

### Table Headings

`<th>` creates heading for the table

### Spanning Rows and Columns

`<td colspan="2">` used to block out two columns

`<td rowspan="2">` used to block out two rows

### Long tables (pg 135)

- thread

- tbody

- tfoot


# <cite> Reading from the Jon Duckett Js book </cite>

## Chapter 3: “Functions, Methods, and Objects” (pp.106-144)

### Creating an Object: Constructor Notation

The new keyword and the object constructor create a blank object.

First you create a new object using a combination of the `new` keyword and the `Object()` constructor.

`var hotel = new Object();`

Next having created a blank object you can add properties to it using the dot notation.

#### Properties
hotel.name = 'Quay';
hotel.rooms = 40;
hotel.booked =25;

#### Method
hotel.checkAvailability = function() {
    return this.rooms - this.booked;
}

### Updating an object

To update the value of properties, use dot notation or square brackets.

They work on objects created using literal or constructor notation.

To delete a property use the delete keyword.

`delete hotel.name;`

If you want to clear the value you can set the string to blank

`hotel.name = ' ';`

### Creating Many Objects: Constructor Notation

create an Object constructor with a capital letter on the fuction to remind yourself to use the new keyword to create new instances of that object.

example:

`function Hotel(name, rooms, booked) {
    this.name = name;
    this.room = rooms;
    this.booked = booked;

    this.checkAvailability = function() {
        return this.rooms - this.booked;
    };
}

Notice the properties are using `this.`

This is because it will belong to the function that creates it.


The parameters set the value of a property in the object which will be used as a template to make new objects from the constuctor.

example:
`var quayHotel = new Hotel('Quay', 40, 25);
var parkHotel = new Hotel('Park', 120, 77);

Notice the new keyword is being used to create the new object

while the parameters are the following properties of that object.

### Create & Access Objects Constructor Notation

`+=` operator is used to add content to an existing variable


### Arrays of Objects & Objects in Arrays

You can store arrays in objects and objects in arrays, you can access this with dot notation and using square brackets to indicate index.

This is explained in detail on pages 118-119.

### Three groups of built-in objects (pp 122-123)

- Browser Object Model (pp 124-125)
- Document Object Model (pp 126-127)
- Global Javascript Objects

Aside:
Gobal Object Numbers and Math(pp 128-135)

### Creating an Instance of the date Object/ working with Dates (pp 136-139)
