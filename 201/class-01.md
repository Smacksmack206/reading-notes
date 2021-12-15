#Cedric's Notes for code-201n24 course

# Reading from the Jon Duckett HTML & CSS / Js Books

## Introduction (pp.2-11)
- This book is for those who want to learn to design and build websites.

- Or for those who already have a website or is using a CMS, Blogging software, or an E-commerce platform and would like more control over their pages.

The only thing you will need in order to use this book is a web browser and a text editor.

I've focused on the code you need to use 90% of the time and omitted the code that you would rarely see even if writing websites is your full time job.

## HTML Chapter 1: “Structure” (pp.12-39)
### HTML
You start by writing words you want to appear on your page.
You then add tags or elements to the words so that the browser knows what is a heading, where a paragaph begins and ends, and so on.

The rest of this section introduces you to tags you have at your disposal to create web pages, grouped into chapters on: text, list, links, images, tables, forms, video audio and flash, and miscellaneous elemeents.

### CSS
We start this section with a chapter that explains how CSS uses rules to enable you to control the styling and layout of a web page. 

Then go on to look at a wide variety of CSS rules properties you can use in your CSS rules.

These properties generally fall into two catagories:

#### Presentation: 
How to control things like the color of text, the fonts you want to use and the size of those fonts, how ot add background colors to pages (or parts of a page), and how to add background images.

#### Layout: 
How to control where the diffrent elements are positioned on the screen. You will also learn several techniques that professionals use to make their pages more attractive.

### Practical
We end up with some helpful information that will assist you with building better websites.

We look at some new tags that will be interoducesa in HTML5 to help describe the structure of your pages.
before learing about these elements, you need a good grasp of how CSS is used to control the design of web pages.

Finally, we end uip looking at topics that helpo you once you build your site, such as putting it on the web serch engine optimasation (SEO) and using analyttics software to track who comes to your site  and what they are looking at.

## HTML Chapter 8: “Extra Markup” (p.176-199)
### DOCTYPES

- HTML5 
` <!DOCTYPE html> `

- HTML 4
` <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd"> `

- Transitional XHTML 1.0
` <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> `

- Strict XHTML 1.0
` <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd"> `

- XML Declaration
` <?xml version="1.0" ?>

### Comments in HTML
You can create a comment that will not be visable by the user's browser by using the following:
` <!-- --> `

### ID Attribute
Every HTML element can carry the id attribute. it is used to unique identify that element from other elements.
You can also use identified elements to style with CSS; which can style it unique from other instances of the same element.
If you go on to learn about Javascript you can use id attributes to work with a particlar element.

example:
` <p id='pullquote'>lorum ipsum</p> `

### Class Attribute
Every HTML element can also carry a class attribute. 
Sometimes rather than uniquely identifying one element within a document you will want to identify several elements - You can use Class Attrributes for that reason.

example:
` <p class='important'>lorum ipsum</p> `

### Block Elements
Some elements will always appear to start on a new line in the browser window.
These are known as block level elements.

Examples of block elements are `<h1>, <p>, <ul>, and <li>.`


### Inline Elements
Some elements will always appear to continue on the same line as their neighbouring elements. These are known as inline elements.

Examples of inline elements are `<a>, <b>, <em>, and <img>.`

### Grouping text and elements in a block

` <div> `

The `<div>` elemlent allows you to group a set of elements together in one block-level-box.

For example, you might create a `<div>` element to contain all of the elements for the header of your site (the logo and the nav) or you might create a `<div>` element to contain commments from visitors.

In the browser the contents of the `<div>` element will start on a new line, buit other than this it will make no difference to the presentation of the page.

Using an id or class attribute on the `<div>` element however means that you can create CSS style rules to indicate how much space the `<div>` element should occupy on the screen and change the appearance of all the elements containt within in.

It can also make it easier to follow the code if you used `<div>` elements to hold each section of the page.

### Grouping Text & Elements Inline

`<span>`

The `<span>` element acts like an inline equivalent of the `<div>` element.

It is used to either:

1. Contain a section of text where there is no other suitable element to differentiate it from its surrounding text
2. Containt a number of inline elements

The most common reasons why people use `<span>` is to control the appearance of these elements through CSS.

### IFRAMES

`<iframe>`

An iframe is like a little window that has been cut into your page -- and in that window you can see another page.

One common use of iframes is to embed a Google Map into a page.
The content of the iframe can be anyt html page (either located on the same server or anywhere else on the web)

An iframe is created using the `<iframe>` element.
there is a few attriubtes you need to know in order to use it.

`src` 
the `src` attribute specifices the url of the page to show in the frame

`height`
specifies the height of the iframe in pixels

`width` 
specifies the width of the ifram in pixels

`scrolling`
not supported in HTML5, in HTML 4 and XHTML, it indicates whether the iframe should have scroll bars or not.

`frameborder`
not supported in HTML5, in HTML 4 and XHTML, it indicates if the frame should have a border or not.

`seamless`
in HTML5, a new attribute can be applied to a iframe where scrollbars are not wanted, and it does not need a value.

## HTML Chapter 17: “HTML5 Layout” (pp.428-451)
### Traditional HTML Layouts
For a long time web page authors used `<div>` elements to group together related elements on the page. Authors used class or id attributes to indicate the rold of the `<div>` element in the structure of the page.   

### New HTML5 Layout Elmements
HTML5 introduces a new set of elements that allow you to divide up the parts of a page. The names of these elements indicate the kind of content you will find in them. They are stil subject to chjange but that has not stopped many web page authors from already using them.

### HEADERS & FOOTERS
`<header> && <footer>`

The header and footer elements can be used for:

- The main header or footer that appears at the top or bottom of every page on the site.

- A header or footer for an individual `<article>` or `<section>` within the page.

The `<header>` Can be used to contain the main navagation.
The `<footer>` Can be used to contain copyright information.

Each individual `<article>` and `<section>` element can also have its own `<header>` and `<footer>` to hold information for that section within the page.

### NAVIGATION
The `<nav>` element is used to contain the major navigational blocks on the site such as the primary site navigation.

### ARTICLES
The `<article>` elementacts as a containter for any section of a page that could stand alone and potentially be syndicated.

This could be an individual article or blog entry, a comment or forum post, or any other indeppenedent piece of content.

### ASIDES
The `<aside>` element has two purposes depending on wheter it is inside an `<article>` element or not.

When the `<aside>` element is used insdie an `<article>` element it should contain the information that is related to the article but not essential to its overall meaning.

When the `<aside>` element is used outside of an `<article>` elememnt it acts as a comntainter for content that is related to the entire page.

### SECTIONS
The '<section>' element groups related content together, and typically each section would have it's own heading.

Because the `<seciton>` element groups related items together, it may contain sever distinct `<article>` elements that have a common theme or purpose.

### Heading Groups
The purpose of the <hgroup> element is to group together a set of one or more <h1> through <h6> elements so that they are treated as one single heading.

## HTML Chapter 18: “Process & Design” (pp.452-475)

# Who is the site for?

Every website should be designed for the target audience - not just for yourself or the siteowner.
It is important to know your target audience.

#### Target Audience: Individuals
- What is the age range of the audiance
- Will it appeal more to women or men? what is the mix?
- Which country do they live in?
- What kind of devices do they use to access the internet?

#### Target Audience: Companies
- What is the size of the company or relevent department?
- What is the position of the people who will visit the site
- How large of a budget do they control?

### Why People Visit Your Site?
Now that you know who is coming to your site, you need to now know why they are coming.

Your content and design should be influensed by the goal of your users

- What is their motivations?

- What is their goals?

#### KEY MOTIVATIONS
- Are they looking for entertainment?
- Is the goal as professional one?
- Is this activity essential or a luxury?

#### SPECIFIC GOALS

- Are they trying to Research/ Fact check
- Are they needing to get familiar with your service or offerings
- Are they looking for time sentive info like the news, or an particular update

### What information does your visitors need?
Figure out what they need to know so you help them reach their goals quickly

### SITEMAPS
Now organize the site in regards to order and what needs pages in what sections

From the Duckett JS book:

## Introduction


## JS Chapter 1: “The ABC of Programming” (pp.11-52)
### THE ABC's of PROGRAMMING
Before you learn how to read and write the javascript language you need to be familar with the following covered in three sections:

- A - WHAT IS A SCRIPT AND HOW DO I CREATE ONE?
- B - HOW DO COMPUTERS FIT IN WITH THE WORLD AROUND THEM
- C - HOW DO I WRITE A SCRIPT  FOR A WEB PAGE

#### A SCRIPT IS A SERIOS OF INSTURCTIONS
A script is a series of instructions that a comper can follow to achieve a goal.

To write a script you need to state your goal and then list the tast need to be completed to achieve it.

1. Define the Goal
2. Design the script
3. Code each step

#### DEFINE THE GOAL &  DESIGNING THE SCRIPT
Consider how you mnight approach a different type of script.

The first thing you should do is detail your goals for the scrtipt that you want to achieve.

Then break it into a series of task that have to be performed in order to achieve the goal.

#### COMPUTERS CREATE MODELS OF THE WORLD USING DATA
Here is a model of a hotel, along with some model trees, model people, and model cars, to a homan, it is clear what kind of real-world object each one represents.

OBJECT TYPE: HOTEL
OBJECT TYPE: CAR

Each object can have its own:
- Properties
- Events
- Methods

Each property has a *name* and *value*

#### METHODS
Methods represent things people need to do with objects.
They can retieve or uipdate the values of an object's properties.

They are like questions and instuctions that 
- Tell you something about that object
- Change the valuie of one or more of that object's properties

The code for a method can contain lots of instructions that together represent one task.

#### PUTTING IT ALL TOGETHER 
Computers use data to create models of things in the real world, the events, methods, and prop0erties of an object all relate to each other  .
Events can trigger methods, methods can retireve or update and object's properties.

#### PLACING THE SCRIPT IN THE PAGE
You may see JavaScript in the HTML between opening <script> and closing </script> tags
but it is better to put scripts in their own files.

#### HOW TO USE OBJECTS & METHODS
This one line of JavaScript shows how to use objects and methods.
Referred to as calling a method of an object.

`document.write('Good afternoon!');

the object is document which referes to the entire webpage
the dot is the member operator which allows you to access methods and properties of an object
write() is the method of the document object allows new content to be written into the page where the script element ends.
In between the parenthises is the parameters which whenever a method is called it needs some info to worwhich owuld be given through an parameter.

#### JAVASCRIPT RUNS WHERE IT IS FOUND IN THE HTML
When the browser comes across a `<script>` element, it needs to load the scirpt and then checks to se f it needs to do anything.
