#Cedric's Notes for code-201n24 course

# Reading from the Jon Duckett HTML & CSS / Js Books

## Text (pp.40-61)

### SuperScript
` <sup> `
The `<sup>` element is used to contain characters that should be superscript such as the suffixes of dates or mathmetical concepts like raising a number to a power.

Basically characters that will go towards the top of other characters (ie: Power of two or 4th or CO2)

### SubScript
` <sub> `
The `<sub>` element is used to contain characters that should be subscript.
It is commonly used with foot-notes or chemical formulas. 

Basically characters that will go towards the bottom of other characters (ie: H20 - where the 2 is lower than the H and the 0.)


### White Space

In order to make code eaiser to read, web page authors often add extra spaces or start some elements on new lines. 

**When the browser comes across two or more spaces next to each other, it only displays one space.**

**Similarly if it comes across a line break. it treats that as a single space too. This is known as white space collapsing.**

You will often see that web page authors take advantage of white sppace collapsing to indent their code in order to make it easier to follow.

### Horizontal Rules

To create a break between themes - such as a change of topic in a book or a new scene in a play - you canadd a horizontal rule between sections using the `<hr />` tag.

There are a few elements that do not have any words between an opening and closing tag. they are known as empty elements and they are written diffrently.

An empty element ususally has only one tag. Before the closing angled bracket of an empty element there will oten be a space and a forward slash character. Some web page authors miss this out but it is a good habit to get into.

## Introducing CSS (pp.226-245)

### Using External CSS

`<link>`
The `<link>` element can be used in an HTML document to tell the browser where to find the CSS file used to style the page. is is an empty element (meaning it does not need a closing tag.) and it lives inside the `<head>` element it should use threee attributes.

`href`
This specifies the ath to the CSS file which is often placed in the css or styles folder.

`type`
This attribute specifies the ttype of document being linked to. The value should bne test/css.

`rel`
This specifies the relationship between the HTML page and the fille it is linked to. The value should bne stylesheet when linking to a CSS file.

An HTML page can use more than one CSS stylesheet. To dio this it could have a <link> element for every CSS file it uses. For example, some authors use one CSS file to control the resentation (such as fonts and colors) and a secord to control the layout.

Example:

 ` <link href="css/styles.css" type="text/css" rel="stylesheet" ;/> `


Using Internal CSS 

`<style>`
You can also include CSS rules within an HTML age by placing them inside a `<style>` element. which usually sit inside the `<head>` element of the page.

The `<style>` element should uise the type attribute to indicate that the style are specified in CSS. The value should be text/css.

When buiilding a site with more than one page, you should use an external CSS stylesheet. 
This allows:

- Allows all ages to use the same style rules (rather than repeating them in each page)

- Keeps the content seperate from how the page looks.

- Means you can change the styles used across all pages by altering just one file (rather than each individual pages.)

### How CSS Rules Casscade

If there are two or more rules that aply to the same element, it is imortant to understand which whill take precedence.

#### Last Rule

If the two selectors are identical, the latter of the two will tkae precedence.

#### Specificity
If one selector is more specific than the others, the more specific rule will take precedence over more general ones.

#### Importance
YOu can add important after any property valiue to indicate that it should be considered more important than other rulesx that aply to the same element.


## Basic JavaScript Instructions (pp.53-84)

Sometimes you will want to use a double or single quote mark within a string.

Because strings can live in a single or double quotes. if you jhust want to use double quotes in the strings, you could surrond the entire string in single quotes.

If you just want to use single quotes in the string, you could surrond the string in double quotes.

You can also use a technique called **escaping** the quoteation characters by putting a backslash before any type of quote mark, this tell the interpreter not to end the string there.

example:
` message = '<a href=\"sale.html\'>25% off!</a>'; `

### Creating an Array

You create an array and give it a name  just like you would any other variable (using the var keywoard followed by the name of the array).

The values are assigned to the array inside a pair of square brackets, and each value is spperated by a comma. 
The values in the array do not need to be the same data type, so you can store a strriung. a number and a Boolean all in the same array.

The technique for creating an array is know as an array literal. it is usually preferred method for creating an array you can also write each value on a seperate line.

Example:
`Colors - ['white','black','red'];`

On the left, you can see an array created using a different technique called an arrayt contructor.
This uses the new keyword followed by Array();
The values are then sperated with parentheses (not square brackets)

Example:
` new Array('whtie','black','red'); `

### Accessing & Changing values in an Array

Create the array
` var colors = ['white','black','red']; `

Update the Third item
` colors[2] = 'blue'; `

Get the element with an id of colors
`var el = document.getElementbyID('colors')`

Replace with third item from the array
` el.textContent = colors[2]; `

In the last two statements the newly updated third item in the array is added to the page.




## Decisions and Loops (pp.145-162)

### Evaluating conditions & conditonal statements

#### Evaluation of a condition
In order to make a decision, your code checks the current status of the script.
This is commonly done by comparing tow values using a comparison oerator which returns a value of true or false.

#### Conditional Statements
A conditional statement is based on a concept of if/then/else; if a condition is met, then youyr code executes one or more statements, else your code does something different (or skips the step.)

Example:

``` 
if (score > 50) {
    document.write('You passed!');
} else {
    document.write('Try again');
} 
``` 

**What this code is saying**
If the condition returns ture execute the statements between the first set of curly brackets otherwise execute the statements between the second set of curly brackets

(You will also meet truthy and falsy values on p167. They are treated as if true or false.)

You can also have multile conditions by combining two or more comparison operators. For example, you can check whether two conditions are both met, or if just one of several conditions is met.

Over the next few pages, you will meet several permutations of the if... statements and also a statment called switch.
Collectivly these are known as conditional statements.

### Comparison operators evaluating conditions

**You can evaluate a situation by comaring one value in the script to what you expect it might be. The result will be a Boolean: true or false.**

Programmers refer to testing or checking of condition as evaulating the condition.

` == `
Is equal to

` != `
Not equal to

` > ` 
Greater than

` < ` 
Less than

` === ` 
Strict equal to

` !== `
Strict not equal to

` >= `
Greater than or equal to

` <= `
Less than or equal to

` && ` 
Logical And
Both expressions have to return true, to execute statements

` || `
Logical Or
Only one expression has to return true, to execute statements

` ! `
Logical Not
Putting this before an expression changes the expression to the opposite expected boolean value
If it was true, it becomes false and visa/versa.

### Switch Statements

A switch statement starts with a variable called the switch value.

Each case indicates a ossible value for this variable and the code tghat should run if the variable matches that value.

default runs when the value of the switch variable set is not any case defined in the switch statement

Example

` switch (level) {
    case 'One':
     title = 'level 1';
     break;

    case 'Two':
     title = 'level 2';
     break;

    default:
     title = 'Test';
     break; 
}
