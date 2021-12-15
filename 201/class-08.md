#Cedric's Notes for code-201n24 course

# <cite> Reading from the Jon Duckett HTML & CSS / Js Books </cite>

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


# CSS Frameworks

CSS Frameworks allow you to import code for common tasks in to your project, such as creating layout grids, styling forms, creating printer friendly versions of pages and so on.

You can include a CSS framework instead of writing CSS from scratch.

# Multiple style sheets

`` @import `` or `` link ``

You can use ``@import url(" ")`` to add multiple style sheets within the CSS file

Or could use link tags within the html.