#Cedric's Notes for code-201n24 course

# <cite> Reading from the Jon Duckett HTML & CSS / Js Books </cite>

## Links (pp.74-93)

### Writing Links

Links are created using the <a> element. User can click on anything between the opening <a> tag and the closing </a> tag. You specifiy which page you want to link to using the href attribute.

Example:
``` <a href="http://www.imdb.com">IMDB</a> ```

The text between the opening <a> tag and closing </a> tag is known as link text. Where possible, your link text should explain where visitors will be taken if they click on it (rather than just saying "click here"). 

To write good link text, you can think of words that people might use when searching for the apge that you are linking to.
(For example, rather than writing "places to stay" you could write something like "Hotels in New York.")

### Linking To Other Sites

` <a> `
links are created using the ` <a> ` element which has an attribute called href. The value of the href attribute is the page that you want people to go to when they click on the link.

### Directory Structure

On larger websites it''s a good idea to organize your code by placing the pages for each different section of the site into a new folder. folders on websites are sometimes reffered to as directories. 

#### Structure

Top level folder is known as the root folder.

Each section of the site is placed in a seperate folder; this helps organize the files.

If ytou are wokring with a content management system, blogging software, or an e-commerce system, you might not have individual files for each page of the website.

#### Relationships

The relationshiop between files and folders on a website is described using the same terminology as a family tree.

Instead, these systems often use one template file for each different typpe of page.

#### Homepages

The main homepage of a site written in HTML (and the homepages of each section in a child folder) is called a index.html

Web servers are usually set up to return the index.html file if no file name is specified.
Therefore, if you enter examplearts.com it will return examplearts.com/index.html, and examplearts.com/music/index.html

Editing the template file would change all of the pages that use that template. Do not change any code that is not HTML or you may break the page.

### Email Links

` mailto: `
To create a link that starts up the user's email programand addresses an email to a specified email address, you use the `<a>` element.
However, this time the value of the href attribute starts with `mailto:` and is followed by the email address you want the email to be sent to.

` target `

If you want a link to oen a new window, you can use the target attribute on the opening `<a>` tag. 
However, thhe valuie of the attribute should be _blank.

### Linking To A Specific Part Of The Same Page

You must give the element you want to link to an ID attribute.

To link to an elment that uses an id attribute you can use the `<a>` element again, but the value of the href attribute starts with `#` symbol, followed by the value of the id attribute.

Example:
<a href="#top">

## Layout (pp.358-404)

### Key Concepts in Positioning Elements

#### Building Blocks

CSS treats each HTML element as if it is in its own box. This box will either be a block level box, or an inline box.

Block level boxes startson a new line and acts as the main building blocks of any layout, while inline flow between surrounding text.

#### Containing Elements

If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element.

It is common to group a number of elements together inside a `<div>` element.
For example, You might group together all of the elements that form the header of a site (such as the logo, and the main navigation.).

A box may be nested inside of several other elements. The containing element is always the direct parent of that element.

### Controlling The Position Of Elements

CSS has the following positioning schemes that allows you to control the layout of a page: normal flow, relative positoning, and absolute positioning.

#### Normal Flow

Every Block-level element apears on a new line, causing each item to apear lower down the age than the pprevious one. Even if you specify thewidth of the boxes and there is space for two elements to site side by side.
They will not apear nedxt to each other this is the defualt behavior unless you tell the browser to do something else.

#### Relative Positioning

This moves an element from the position it would be in normal flow, shifting it to the top, right , bottom, or left of where it would been placed.
This does not affect the position of surrounding elements; they stay in the position they would be in normal flow.

#### Absolute Positioning

This positions the element in relation to its containg element. It is taken out of normal flow, meaning that it does not affect the position of any surrounding elements. (as they simply ignore the space it would have taken up)
Absolutely positioned elements move as users scroll up and down the page.

#### Fixed Positioning

This is a form of absolute positioning that postins the element in trelation to the browser window. as opposed to the containing element.
Elements with fixed positing do not affect the positioning do not affect the position of surrounding elements and they do no0t move when the user scrolls u or down the age.

#### Floating ELements

Floating an element allows you to take that element out opf normal flow and position it to the far left or right of a containing box the floated element around which other content can flow.

When you move any elememnt from normal flow boxes can overlap.

The z-index proerty allows you to control which box apppears on top.

#### CSS Properties:

Normal Flow
`position:static`

Relative Positioning
`postition:relative`

Absolute Positioning
`position:absolute`

Fixed Postioning
`position:fixed`

Overlapping elements
`z-index`

Floating elements
`float`

Clearing floats
`clear`

#### Layout Summary

- `<div>` elements are often used as contaning elements to group together sectikons of a page

- Browsers display pages in normal flow unless you specify relative, absolute, or fixed positioning.

- The float property moves content to the left or right of the page and can be used to create multi-colmn layouts. 

- Pages can be fixed width or liquid (strechy) layouts.

- Designers keep ppages within 960-1000 pixels wide, and indicate what the site is about within the 600 pixels (to demostrate it's relevence without scrolling.)

- Grids help create professional and flexible designs.

- CSS Frameworks provide rules for common tasks.

- You can use multiple CSS 
files in one page.



## Functions, Methods, and Objects (pp.86-99)

### What Is A Function?

Functions let you group a series of statements together to perform a specific task. 

If different parts of a script repeats the same task, you can reuse the function (rather htan repeating the same set of statements).

### Declaring A Function

To create a function, you give it a name and then write the statements needed to achive its task inside the curly braces.

You declare a function using the function keyword.

You give the function a name called an iedentifier followed by parenthesis.

The statment that performs the task sits in a code block.

Example:
``` function sayHello() {
    dociument.write('Hello')
} ```

### Calling A Function

Having declared the function, you can then ex ecute all of the statements bnetween its curly braces with just one line of code.

This is called calling a funciton.

To run the code in the function, you use the funciton name followed by parentheses.

Example:
``` sayHello(); ```

###Declaring Functions That Need Information

Sometimes a function needs secific info to perform its task. in such cases, when you declare the function you give it parameters. inside the function, the parameters act like variable.

If a function needs information to work, you indicate what it needs to know in arentheses after the fuction name. 

The item that appears inside these aprenthesis known as the arameters of the funciton.
inside function those words act like variable name.

``` function getArea(width, height) {
    renturn width * height;
} ```

This function will calculate and return the area of a rectangle. To do this, it needs the rectangle's width and height. Each time you call the function these values could be different.

This demostrates how the code can perform a task without knowing the exact details in advance, as long as it has rules it can follow to achieve the task.

So, when you design a script, you need to make the information the fucntion the require in order to perform its task.

If you look inside the function, the parameternames are used just as you would use variables. Here, the arametere names width and height reersent the width and height of the wall.

### Calling Function That Need Information

When you call a function that has arameters , you specify the values it should use in the parentheses that follow its name. The value are called arguments, and they can be rovided as valuies or as varibales.

