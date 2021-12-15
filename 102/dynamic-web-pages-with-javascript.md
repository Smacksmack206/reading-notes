#Cedric's Notes for code-102n57 course

# JavaScript

*JavaScript (JS)* is a lightweight, interpreted, or just-in-time compiled programming language with first-class functions. While it is most well-known as the scripting language for Web pages, many non-browser environments also use it, such as Node.js, Apache CouchDB and Adobe Acrobat. JavaScript is a prototype-based, multi-paradigm, single-threaded, dynamic language, supporting object-oriented, imperative, and declarative (e.g. functional programming) styles. Read more about JavaScript.

Do not confuse JavaScript with the Java programming language. Both "Java" and "JavaScript" are trademarks or registered trademarks of Oracle in the U.S. and other countries. However, the two programming languages have very different syntax, semantics, and use.


## Input Output in plain JavaScript

We are going to see how to get input from the user and combine that with the other two, to create a simple page that can great you.

examples/js/pure_js_greating.html

` <html>
<head>
  <title>Hello World</title>
</head>
<body>
 
First name: <input id="first_name">
Last name: <input id="last_name">
<button id="say">Say hi!</button>
 
<hr>
<div id="result"></div>
 
<script>
function say_hi() {
    var fname = document.getElementById('first_name').value;
    var lname = document.getElementById('last_name').value;
 
    var html = 'Hello <b>' + fname + '</b> ' + lname;
 
    document.getElementById('result').innerHTML = html;
}
 
document.getElementById('say').addEventListener('click', say_hi);
</script>
 
</body>
</html> `
 
In this example we have a bit more HTML than earlier. In addition to having a button, and a div element where we'll show our results, we also have two input elements. Each one with its own ID.

In the JavaScript code we have a function called say_hi. It used the getElementById we have already seen to locate the DOM element representing the input element with the id first_name. The object returned has a method value that will return the text the user has typed in that field.

If you click on the Try link, you'll see two input boxes and a button:
[image](https://code-maven.com/img/input_form.png)

We use this technique to retrieve the content of both input fields and assign their content to two variables: fname and lname.

Then, using these variable we create an HTML snippet and assign it to a new variable called html.

Then we set the innerHTML attribute as earlier to show the HTML we generated. The result might look like this:

[image](https://code-maven.com/img/input_form_and_output.png)


# JavaScript Variables

There are 3 ways to declare a JavaScript variable:

` Using var
Using let
Using const
This chapter uses var. `

The let and const keywords are explained in the next chapters.

## Variables
Variables are containers for storing data (values).

In this example, x, y, and z, are variables, declared with the var keyword:

Example
` var x = 5;
var y = 6;
var z = x + y; `

From the example above, you can expect:

x stores the value 5
y stores the value 6
z stores the value 11


## Much Like Algebra
In this example, price1, price2, and total, are variables:

Example
` var price1 = 5;
var price2 = 6;
var total = price1 + price2; `

In programming, just like in algebra, we use variables (like price1) to hold values.

In programming, just like in algebra, we use variables in expressions (total = price1 + price2).

From the example above, you can calculate the total to be 11.

JavaScript variables are containers for storing data values.

## JavaScript Identifiers

All JavaScript variables must be identified with unique names.

These unique names are called identifiers.

Identifiers can be short names (like x and y) or more descriptive names (age, sum, totalVolume).

The general rules for constructing names for variables (unique identifiers) are:

Names can contain letters, digits, underscores, and dollar signs.
Names must begin with a letter
Names can also begin with $ and _ (but we will not use it in this tutorial)
Names are case sensitive (y and Y are different variables)
Reserved words (like JavaScript keywords) cannot be used as names
JavaScript identifiers are case-sensitive.

## The Assignment Operator
In JavaScript, the equal sign (=) is an "assignment" operator, not an "equal to" operator.

This is different from algebra. The following does not make sense in algebra:

x = x + 5

In JavaScript, however, it makes perfect sense: it assigns the value of x + 5 to x.

(It calculates the value of x + 5 and puts the result into x. The value of x is incremented by 5.)

The "equal to" operator is written like == in JavaScript.

## JavaScript Data Types
JavaScript variables can hold numbers like 100 and text values like "John Doe".

In programming, text values are called text strings.

JavaScript can handle many types of data, but for now, just think of numbers and strings.

Strings are written inside double or single quotes. Numbers are written without quotes.

If you put a number in quotes, it will be treated as a text string.

Example
var pi = 3.14;
var person = "John Doe";
var answer = 'Yes I am!';


## Declaring (Creating) JavaScript Variables
Creating a variable in JavaScript is called "declaring" a variable.

You declare a JavaScript variable with the var keyword:

` ar carName; `

After the declaration, the variable has no value (technically it has the value of undefined).

To assign a value to the variable, use the equal sign:

carName = "Volvo";
You can also assign a value to the variable when you declare it:

var carName = "Volvo";
In the example below, we create a variable called carName and assign the value "Volvo" to it.

Then we "output" the value inside an HTML paragraph with id="demo":

` Example
<p id="demo"></p>

<script>
var carName = "Volvo";
document.getElementById("demo").innerHTML = carName;
</script> `

## One Statement, Many Variables
You can declare many variables in one statement.

Start the statement with var and separate the variables by comma:

` var person = "John Doe", carName = "Volvo", price = 200; `

A declaration can span multiple lines:

` var person = "John Doe",
carName = "Volvo",
price = 200; `

# Value = undefined
In computer programs, variables are often declared without a value. The value can be something that has to be calculated, or something that will be provided later, like user input.

A variable declared without a value will have the value undefined.

The variable carName will have the value undefined after the execution of this statement:

Example
` var carName; `

## Re-Declaring JavaScript Variables
If you re-declare a JavaScript variable, it will not lose its value.

The variable carName will still have the value "Volvo" after the execution of these statements:

Example
` var carName = "Volvo";
var carName; `


## JavaScript Arithmetic
As with algebra, you can do arithmetic with JavaScript variables, using operators like = and +:

Example
` var x = 5 + 2 + 3; `

#### You can also add strings, but strings will be concatenated:

Example
` var x = "John" + " " + "Doe"; `


Also try this:

Example
` var x = "5" + 2 + 3; `

## JavaScript Dollar Sign $
Remember that JavaScript identifiers (names) must begin with:

A letter (A-Z or a-z)
A dollar sign ($)
Or an underscore (_)
Since JavaScript treats a dollar sign as a letter, identifiers containing $ are valid variable names:

Example
` var $$$ = "Hello World";
var $ = 2;
var $myMoney = 5; `
Using the dollar sign is not very common in JavaScript, but professional programmers often use it as an alias for the main function in a JavaScript library.

In the JavaScript library jQuery, for instance, the main function $ is used to select HTML elements. In jQuery $("p"); means "select all p elements".

## JavaScript Underscore (_)
Since JavaScript treats underscore as a letter, identifiers containing _ are valid variable names:

Example
` var _lastName = "Johnson";
var _x = 2;
var _100 = 5; `