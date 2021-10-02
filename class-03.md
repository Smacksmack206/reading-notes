#Cedric's Notes for code-201n24 course

# <cite> Reading from the Jon Duckett HTML & CSS / Js Books </cite>

## Lists (pp.62-73)

There are lots of occasions when we need to use lists. HTML provides us with three different types:


`<ol>`− An ordered list will used numbers to indicate order.
`<ul>` − An unordered list begins with a bullet point (rather than characters that indicate order).
`<dl>` − A definition list are made up of a set of terms along with the definitions for each of those terms.

## Boxes (pp.300-329)

At the beginning of this section on CSS, you saw how CSS treats each HTML element as if it lives in its own box.

### Border, Margin & Padding

Every box has three available properties that can be adjusted to control its appearance:

``` Border - Every Box has a border, even if it’s not visible or is specified to be 0 pixels wide.The border separates the edge of one box to another. ```

``` Margin - Margins sit outside the edge of the border, you can set the width of a margin to create the gap between the borders of two adjacent boxes. ```

``` Padding - Padding is the space between the border of a box and may content contained within it. Adding padding can increase the readability of its contents. ```


## Basic JavaScript Instructions (pp.70-73)

### Creating an Array

You can create an array and give it a name juust like you would any other variable.

The values are assigned to the array inside a pair of square brackets, and each value is seperated by a comma.

The values in the array do not need to be the same data type.

This technique for creating an Array is called Array Litteral:


``` Colors = ['1', 'red', 'cedric']; ```


## Decisions and Loops (pp.162-182)

### If..Else Statements

The If...else statement checks a condition. 
if it resolves to true the first codee block is executed.
If the condidtion resolved to false the secode code block is run instead.

``` if (score >= 50) {
  congratulate();
}
else {
  encourage();
} ```

### Switch Statements 

A switch statement starts with a variable called the stwich value.
Each case inidicates a possible vlaue for this variable and the code that should run if the variable matches that value.


### Loops 

Loops check a condition. If it returns true, a code block will run.
Then the condition will be checked again, and if it still remains true, the code block will run again, it repeats until the conditons return false.
There are three common types of loops:

#### for 
If you need to run code a specific number of times.
In a for loop, the condition is usually the counter which is used to tell how many times the loop should run.

#### while 
If you dont know how many times thje code should run, you ccan use a while loop.
Here the condition can be something other than a counter, and the code will continue to loop for as long as the condition remains true.


#### do while
The do...while loop is very simlar to the while loop, but has one key difference, it will always run the statements inside the currly braces at least once, even if the condition evaluetes as false.

