#Cedric's Notes for code-102n57 course

#Programming with JavaScript

## Expressions and operators

### Operators
JavaScript has the following types of operators. This section describes the operators and contains information about operator precedence.

- Assignment operators
- Comparison operators
- Arithmetic operators
- Bitwise operators
- Logical operators
- String operators
- Conditional (ternary) operator
- Comma operator
- Unary operators
- Relational operators

JavaScript has both binary and unary operators, and one special ternary operator, the conditional operator. A binary operator requires two operands, one before the operator and one after the operator:

` operand1 operator operand2 `

For example, ` 3+4 or x*y. `

A unary operator requires a single operand, either before or after the operator:

` operator operand `

or

` operand operator `

` For example, x++ or ++x `

# Assignment operators
An assignment operator assigns a value to its left operand based on the value of its right operand. The simple assignment operator is equal (=), which assigns the value of its right operand to its left operand. That is, x = y assigns the value of y to x.

There are also compound assignment operators that are shorthand for the operations listed in the following table:

| Name	      | Shorthand operator	 | Meaning     |
| :---        |    :----:   |          ---: |
| Assignment   |	x = y  |	x = y  |
| Addition assignment |	x += y	| x = x + y |
| Subtraction assignment |	x -= y |	x = x - y |
| Multiplication assignment |	x *= y |	x = x * y |
| Division assignment |	x /= y |	x = x / y |
| Remainder assignment | 	x %= y |	 x = x % y |
| Exponentiation assignment |	x **= y  |	x = x ** y |
| Left shift assignment |	x <<= y  |	x = x << y  |
| Right shift assignment |	x >>= y  |	x = x >> y |
| Unsigned right shift assignment |	x >>>= y  |	x = x >>> y |
| Bitwise AND assignment |	x &= y  |	x = x & y |
| Bitwise XOR assignment |	x ^= y  |	x = x ^ y |
| Bitwise OR assignment |	x |= y  |	x = x | y |
| Logical AND assignment |	x &&= y	 | x && (x = y) |
| Logical OR assignment |	x ||= y  |	x || (x = y) |  
| Logical nullish assignment |	x ??= y  |	x ?? (x = y) |


### Return value and chaining
Like most expressions, assignments like x = y have a return value. It can be retrieved by e.g. assigning the expression or logging it:

` const z = (x = y); // Or equivalently: const z = x = y; `
` console.log(z); // Log the return value of the assignment x = y. `
` console.log(x = y); // Or log the return value directly. `

The return value matches the expression to the right of the = sign in the “Meaning” column of the table above. That means that (x = y) returns y, (x += y) returns the resulting sum x + y, (x **= y) returns the resulting power x ** y, and so on.


The return value matches the expression to the right of the = sign in the “Meaning” column of the table above. That means that (x = y) returns y, (x += y) returns the resulting sum x + y, (x **= y) returns the resulting power x ** y, and so on.

In the case of logical assignments, (x &&= y), (x ||= y), and (x ??= y), the return value is that of the logical operation without the assignment, so x && y, x || y, and x ?? y, respectively.

Note that the return values are always based on the operands’ values before the operation.

When chaining these expressions, each assignment is evaluated right-to-left. Consider these examples:

` w = z = x = y is equivalent to w = (z = (x = y)) or x = y; z = y; w = y `
 `z += x *= y is equivalent to z += (x *= y) or tmp = x * y; x *= y; z += tmp (except without the tmp). `

### Destructuring
For more complex assignments, the destructuring assignment syntax is a JavaScript expression that makes it possible to extract data from arrays or objects using a syntax that mirrors the construction of array and object literals.

` var foo = ['one', 'two', 'three'];

// without destructuring
var one   = foo[0];
var two   = foo[1];
var three = foo[2];

// with destructuring
var [one, two, three] = foo; `

### Comparison operators
A comparison operator compares its operands and returns a logical value based on whether the comparison is true. The operands can be numerical, string, logical, or object values. Strings are compared based on standard lexicographical ordering, using Unicode values. In most cases, if the two operands are not of the same type, JavaScript attempts to convert them to an appropriate type for the comparison. This behavior generally results in comparing the operands numerically. The sole exceptions to type conversion within comparisons involve the === and !== operators, which perform strict equality and inequality comparisons. These operators do not attempt to convert the operands to compatible types before checking equality. The following table describes the comparison operators in terms of this sample code:

var var1 = 3;
var var2 = 4;


| Equal (==) |	Returns true if the operands are equal.
| Not equal (!=) |	Returns true if the operands are not equal.
| Strict equal (===) |	Returns true if the operands are equal and of the same type. See also Object.is  |  and sameness in JS. |
| Strict not equal (!==) |	Returns true if the operands are of the same type but not equal, or are of   | | different type. |
| Greater than (>) |	Returns true if the left operand is greater than the right operand.
| Greater than or equal (>=) | 	Returns true if the left operand is greater than or equal to the right operand. |
| Less than (<) |	Returns true if the left operand is less than the right operand.
| Less than or equal (<=)  |	Returns true if the left operand is less than or equal to the right operand.

## Functions

Functions are one of the fundamental building blocks in JavaScript. A function in JavaScript is similar to a procedure—a set of statements that performs a task or calculates a value, but for a procedure to qualify as a function, it should take some input and return an output where there is some obvious relationship between the input and the output. To use a function, you must define it somewhere in the scope from which you wish to call it.

## Function declarations
A function definition (also called a function declaration, or function statement) consists of the function keyword, followed by:

The name of the function.
A list of parameters to the function, enclosed in parentheses and separated by commas.
The JavaScript statements that define the function, enclosed in curly brackets, {...}.
For example, the following code defines a simple function named square:

` function square(number) {
  return number * number;
} `

The function square takes one parameter, called number. The function consists of one statement that says to return the parameter of the function (that is, number) multiplied by itself. The statement return specifies the value returned by the function:

` return number * number; `

Primitive parameters (such as a number) are passed to functions by value; the value is passed to the function, but if the function changes the value of the parameter, this change is not reflected globally or in the calling function.

If you pass an object (i.e., a non-primitive value, such as Array or a user-defined object) as a parameter and the function changes the object's properties, that change is visible outside the function, as shown in the following example:

` function myFunc(theObject) {
  theObject.make = 'Toyota';
} 

var mycar = {make: 'Honda', model: 'Accord', year: 1998};
var x, y;

x = mycar.make; // x gets the value "Honda"

myFunc(mycar);
y = mycar.make; ` // y gets the value "Toyota"
                // (the make property was changed by the function)

# Control flow
The control flow is the order in which the computer executes statements in a script.

Code is run in order from the first line in the file to the last line, unless the computer runs across the (extremely frequent) structures that change the control flow, such as conditionals and loops. 

For example, imagine a script used to validate user data from a webpage form. The script submits validated data, but if the user, say, leaves a required field empty, the script prompts them to fill it in. To do this, the script uses a conditional structure or if...else, so that different code executes depending on whether the form is complete or not:

` if (field==empty) {
    promptUser();
} else {
    submitForm();
} `

A typical script in JavaScript or PHP (and the like) includes many control structures, including conditionals, loops and functions. Parts of a script may also be set to execute when events occur.

For example, the above excerpt might be inside a function that runs when the user clicks the Submit button for the form. The function could also include a loop, which iterates through all of the fields in the form, checking each one in turn. Looking back at the code in the if and else sections, the lines promptUser and submitForm could also be calls to other functions in the script. As you can see, control structures can dictate complex flows of processing even with only a few lines of code.

Control flow means that when you read a script, you must not only read from start to finish but also look at program structure and how it affects order of execution.

# JavaScript Functions

A JavaScript function is a block of code designed to perform a particular task.

A JavaScript function is executed when "something" invokes it (calls it).

### Example

` function myFunction(p1, p2) {
  return p1 * p2;   // The function returns the product of p1 and p2
} `

## JavaScript Function Syntax

A JavaScript function is defined with the function keyword, followed by a name, followed by parentheses ().

Function names can contain letters, digits, underscores, and dollar signs (same rules as variables).

The parentheses may include parameter names separated by commas:
(parameter1, parameter2, ...)

The code to be executed, by the function, is placed inside curly brackets: {}

function name(parameter1, parameter2, parameter3) {
  // code to be executed
}


Function parameters are listed inside the parentheses () in the function definition.

Function arguments are the values received by the function when it is invoked.

Inside the function, the arguments (the parameters) behave as local variables.

A Function is much the same as a Procedure or a Subroutine, in other programming languages.

## Function Invocation
The code inside the function will execute when "something" invokes (calls) the function:

When an event occurs (when a user clicks a button)
When it is invoked (called) from JavaScript code
Automatically (self invoked)
You will learn a lot more about function invocation later in this tutorial.

## Function Return
When JavaScript reaches a return statement, the function will stop executing.

If the function was invoked from a statement, JavaScript will "return" to execute the code after the invoking statement.

Functions often compute a return value. The return value is "returned" back to the "caller":


Example
Calculate the product of two numbers, and return the result:

` let x = myFunction(4, 3);   // Function is called, return value will end up in x

function myFunction(a, b) {
  return a * b;             // Function returns the product of a and b
} `

The result in x will be: ` 12 `

## Why Functions?
You can reuse code: Define the code once, and use it many times.

You can use the same code many times with different arguments, to produce different results.

Example
Convert Fahrenheit to Celsius:

` function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
}
document.getElementById("demo").innerHTML = toCelsius(77); `

## The () Operator Invokes the Function 
Using the example above, toCelsius refers to the function object, and toCelsius() refers to the function result.

Accessing a function without () will return the function object instead of the function result.

Example
` function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
} 
document.getElementById("demo").innerHTML = toCelsius; `

## Functions Used as Variable Values
Functions can be used the same way as you use variables, in all types of formulas, assignments, and calculations.

Example
Instead of using a variable to store the return value of a function:

` let x = toCelsius(77);
let text = "The temperature is " + x + " Celsius";
You can use the function directly, as a variable value: `

` let text = "The temperature is " + toCelsius(77) + " Celsius"; `

You will learn a lot more about functions later in this tutorial.

## Local Variables
Variables declared within a JavaScript function, become LOCAL to the function.

Local variables can only be accessed from within the function.

Example
// code here can NOT use carName

` function myFunction() {
  let carName = "Volvo";
  // code here CAN use carName
} 

// code here can NOT use carName `

# JavaScript Operators

Example
Assign values to variables and add them together:

` let x = 5;         // assign the value 5 to x `
` let y = 2;         // assign the value 2 to y `
` let z = x + y;     // assign the value 7 to z (5 + 2) `
The assignment operator (=) assigns a value to a variable.

Assignment
` let x = 10; `
The addition operator (+) adds numbers:

Adding
` let x = 5; `
` let y = 2; `
` let z = x + y; `
The multiplication operator (*) multiplies numbers.

Multiplying
` let x = 5; `
` let y = 2; `
` let z = x * y; `

## JavaScript Arithmetic Operators
Arithmetic operators are used to perform arithmetic on numbers:

| Operator  |	Description |
| +	 | Addition | 
| -	| Subtraction |
| *  |	Multiplication |
| **	 | Exponentiation (ES2016) |
| /	 | Division  |
| %	| Modulus (Division Remainder) |
| ++	| Increment  |
| --	| Decrement  |

Arithmetic operators are fully described in the JS Arithmetic chapter.

## JavaScript Assignment Operators
Assignment operators assign values to JavaScript variables.

|Operator	Example	Same As
| =	 | x = y    | 	x = y |
|+=	x | += y	x = | x + y | 
| -=  |	x -= y	| x = x - y | 
| *=  |	x *= y	| x = x * y |
| /=  |	x /= y	| x = x / y |
| %=  |	x %= y	| x = x % y |
| **=  |	x **= y |	x = x ** y |

The addition assignment operator (+=) adds a value to a variable.

#### Assignment
` let x = 10;
x += 5; `


## JavaScript String Operators
The + operator can also be used to add (concatenate) strings.

Example
` let text1 = "John";
let text2 = "Doe";
let text3 = text1 + " " + text2; `

The result of text3 will be: ` John Doe `


The += assignment operator can also be used to add (concatenate) strings:

Example

` let text1 = "What a very ";
text1 += "nice day"; `

The result of text1 will be: ` What a very nice day `
