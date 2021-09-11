#Cedric's Notes for code-102n57 course

# Structure web pages with HTML

## Wireframe and Design
### What is a wireframe?
Wireframing is a practice used by UX designers which allows them to define and plan the information hierarchy of their design for a website, app, or product. This process focuses on how the designer or client wants the user to process information on a site, based on the user research already performed by the UX design team.

When designing for the screen you need to know where all the information is going to go in plain black and white diagrams before building anything with code—whether that’s a developer coding it, or you the designer. Wireframing is also a great way of getting to know how a user interacts with your interface, through the positioning of buttons and menus on the diagrams.

### Wireframe examples
Before you start designing the wireframes of your own app or product, take a look at some examples of wireframes. This will give you some inspiration for your own wireframes, as well as giving you an idea of the variety of ways of creating them. Some people like to draw their wireframes by hand, others feel more comfortable using software like Invision, or Balsamiq to create theirs. We’ll go through some of the tools you can use to create wireframes shortly, but it’s important to emphasize that how you make yours is up to you: some people feel more creative when sat at their computer, while others prefer to have a pen and paper in hand.

[image](https://dpbnri2zg3lc2.cloudfront.net/en/wp-content/uploads/old-blog-uploads/versions/samuel-student-wireframe---x----972-715x---.png)

###  Things to consider before you start wireframing
As we mentioned above, different UX designers approach the task of wireframing in different ways. Some like to draw by hand, while others like to use apps or tools found online. But more often than not, the decision to use online tools or to wireframe by hand, and the process used to get to from wireframe to code, is less related to the individual preference of the UX Designer, and much more related to what approach the particular situation requires. It depends largely on how much emphasis there is on visual design in a project, and how much uncertainty there is with respect to what is being designed.

Here are a number of ways different designers can structure the process from design to implementation:

Wireframe > Interactive Prototype > Visual > Design
Sketch > Code
Sketch > Wireframe > Hi-Def Wireframe > Visual > Code
Sketch > Wireframe > Visual > Code
If the task is very narrow and the visual design is either set or considered unimportant (such as with many backend administrative interfaces), then going from a sketch to coding/development makes sense, whereas if the time and resources and the business value are all high, then spending the time to make a high-definition wireframe and going through a cycle of testing with a fully realized interactive prototype makes better sense.

### The best tools for wireframing
There are heaps of free wireframe tools out there, so you should experiment with as many as you can to find the ones that suit you the best. Don’t forget that you can also just use pen and paper! Below we’ve listed three online tools we find particularly good. The examples below all have free trials, so check them out!

UXPin: UXPin has a wide range of functionalities, but one of the best ones is how it facilitates building responsive, clickable prototypes directly in your browser.

InVision: InVision allows you to get feedback straight from your team and users through clickable mock-ups of your site design. It’s completely free too!

Wireframe.cc: Wireframe.cc provides you with the technology to create wireframes really quickly within your browser, the online version of pen and paper.

## Steps to make a wireframe

1. Do your research
first two steps; namely understanding who your audience is by way of user research, detailing requirements, creating user personas and defining use cases, and complementing this with further competitor and industry research. What does that mean? That means carrying out analysis of similar product lines to your own, digging into prevailing UX trends and best practises, and, of course, reviewing your own internal design guidelines.

2. Prepare your research for quick reference

3. Make sure you have your user flow mapped out

4. Draft, don’t draw. Sketch, don’t illustrate
- How can you organise the content to support your users’ goals?
- Which information should be most prominent? Where should your main message go? 
- What should the user see first when arriving at the page?
- What will the user expect to see on certain areas of the page?
- Which buttons or touch points does the user need to complete the desired actions?

5. Add some detail and get testing

## Start turning your wireframes into prototypes


How to make your wireframe good: Three key principles
The following points should be at the forefront of your mind when building your wireframe:

1. Clarity
Your wireframe needs to answer the questions of what that site page is, what the user can do there, and if it satisfies their needs. Your wireframe is an aid for you to visualize the layout of your site page and ensure that the user’s most important questions are answered and goals are achievable without being distracted by more aesthetic considerations.

2. Confidence
Ease of navigation through your site and clear calls-to-action increase user confidence in your brand. If your site page is unpredictable, or has buttons or boxes in unexpected places user confidence diminishes. A lot of this information can already be organized at the wireframing stage. Using familiar navigational processes and placing buttons in commonly-used and intuitive positions, user confidence will soar–and that’s before you’ve even gotten around to thinking about colors and styles.

3. Simplicity is key
Too much information, copy, or links, can be distracting to the user and will have a detrimental affect on your users’ ability to achieve their goals. You want your users to be able to find their way through your site with as little extra ‘fluff’ as possible, to the elements that map to their most significant goals in a given context.

Your wireframe should be a visual guide to the framework of your site and how it will be navigated. Attractiveness at this stage is not a consideration. Once you’ve decided who your product or service is for, you can begin laying out the information they are looking for in an intuitive and natural way that is not only familiar to them as users of this kind of service, but that also guides them towards the conversion point or otherwise helps them to achieve their goals in the interaction. By presenting your information in this way, you are aligning both the business goals of your site with the needs of the customer.


## HTML basics
HTML (Hypertext Markup Language) is the code that is used to structure a web page and its content. For example, content could be structured within a set of paragraphs, a list of bulleted points, or using images and data tables. As the title suggests, this article will give you a basic understanding of HTML and its functions.


### So what is HTML?
HTML is a markup language that defines the structure of your content. HTML consists of a series of elements, which you use to enclose, or wrap, different parts of the content to make it appear a certain way, or act a certain way. The enclosing tags can make a word or image hyperlink to somewhere else, can italicize words, can make the font bigger or smaller, and so on.  For example, take the following line of content:

` My cat is very grumpy `

If we wanted the line to stand by itself, we could specify that it is a paragraph by enclosing it in paragraph tags:

` <p>My cat is very grumpy</p> `

### Anatomy of an HTML element
Let's explore this paragraph element a bit further.

[image](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics/grumpy-cat-small.png)

The main parts of our element are as follows:

*The opening tag:* This consists of the name of the element (in this case, p), wrapped in opening and closing angle brackets. This states where the element begins or starts to take effect — in this case where the paragraph begins.
*The closing tag:* This is the same as the opening tag, except that it includes a forward slash before the element name. This states where the element ends — in this case where the paragraph ends. Failing to add a closing tag is one of the standard beginner errors and can lead to strange results.
*The content:* This is the content of the element, which in this case, is just text.
*The element:* The opening tag, the closing tag, and the content together comprise the element.

Elements can also have attributes that look like the following:

[image](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics/grumpy-cat-attribute-small.png)

Attributes contain extra information about the element that you don't want to appear in the actual content. Here, class is the attribute name and editor-note is the attribute value. The class attribute allows you to give the element a non-unique identifier that can be used to target it (and any other elements with the same class value) with style information and other things.

An attribute should always have the following:

1. A space between it and the element name (or the previous attribute, if the element already has one or more attributes).
2. The attribute name followed by an equal sign.
3. The attribute value wrapped by opening and closing quotation marks.

### Nesting elements
You can put elements inside other elements too — this is called nesting. If we wanted to state that our cat is very grumpy, we could wrap the word "very" in a <strong> element, which means that the word is to be strongly emphasized:

` <p>My cat is <strong>very</strong> grumpy.</p> `


You do however need to make sure that your elements are properly nested. In the example above, we opened the <p> element first, then the <strong> element; therefore, we have to close the <strong> element first, then the <p> element. The following is incorrect:

` <p>My cat is <strong>very grumpy.</p></strong> `

The elements have to open and close correctly so that they are clearly inside or outside one another. If they overlap as shown above, then your web browser will try to make the best guess at what you were trying to say, which can lead to unexpected results. So don't do it!

### Empty elements
Some elements have no content and are called empty elements. Take the <img> element that we already have in our HTML page:

` <img src="images/firefox-icon.png" alt="My test image"> ` 

This contains two attributes, but there is no closing </img> tag and no inner content. This is because an image element doesn't wrap content to affect it. Its purpose is to embed an image in the HTML page in the place it appears.

### Anatomy of an HTML document
That wraps up the basics of individual HTML elements, but they aren't handy on their own. Now we'll look at how individual elements are combined to form an entire HTML page. Let's revisit the code we put into our index.html example (which we first met in the Dealing with files article):

` <!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My test page</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="My test image">
  </body>
</html> `

Here, we have the following:

- <!DOCTYPE html> — doctype. It is a required preamble. In the mists of time, when HTML was young (around 1991/92), doctypes were meant to act as links to a set of rules that the HTML page had to follow to be considered good HTML, which could mean automatic error checking and other useful things. However these days, they don't do much and are basically just needed to make sure your document behaves correctly. That's all you need to know for now.
- <html></html> — the <html> element. This element wraps all the content on the entire page and is sometimes known as the root element.
- <head></head> — the <head> element. This element acts as a container for all the stuff you want to include on the HTML page that isn't the content you are showing to your page's viewers. This includes things like keywords and a page description that you want to appear in search results, CSS to style our content, character set declarations, and more.
- <meta charset="utf-8"> — This element sets the character set your document should use to UTF-8 which includes most characters from the vast majority of written languages. Essentially, it can now handle any textual content you might put on it. There is no reason not to set this and it can help avoid some problems later on.
- <title></title> — the <title> element. This sets the title of your page, which is the title that appears in the browser tab the page is loaded in. It is also used to describe the page when you bookmark/favorite it.
- <body></body> — the <body> element. This contains all the content that you want to show to web users when they visit your page, whether that's text, images, videos, games, playable audio tracks, or whatever else.

### Images
Let's turn our attention to the <img> element again:

` <img src="images/firefox-icon.png" alt="My test image"> `


As we said before, it embeds an image into our page in the position it appears. It does this via the src (source) attribute, which contains the path to our image file.

We have also included an alt (alternative) attribute. In this attribute, you specify descriptive text for users who cannot see the image, possibly because of the following reasons:

1. They are visually impaired. Users with significant visual impairments often use tools called screen readers to read out the alt text to them.
2. Something has gone wrong causing the image not to display. For example, try deliberately changing the path inside your src attribute to make it incorrect. If you save and reload the page, you should see something like this in place of the image:


The keywords for alt text are "descriptive text". The alt text you write should provide the reader with enough information to have a good idea of what the image conveys. In this example, our current text of "My test image" is no good at all. A much better alternative for our Firefox logo would be "The Firefox logo: a flaming fox surrounding the Earth."


### Links
Links are very important — they are what makes the web a web! To add a link, we need to use a simple element — <a> — "a" being the short form for "anchor". To make text within your paragraph into a link, follow these steps:

Choose some text. We chose the text "Mozilla Manifesto".
Wrap the text in an <a> element, as shown below:

` <a>Mozilla Manifesto</a> `

Give the <a> element an href attribute, as shown below:

` <a href="">Mozilla Manifesto</a> `

Fill in the value of this attribute with the web address that you want the link to link to:

` <a href="https://www.mozilla.org/en-US/about/manifesto/">Mozilla Manifesto</a> `

You might get unexpected results if you omit the https:// or http:// part, called the protocol, at the beginning of the web address. After making a link, click it to make sure it is sending you where you wanted it to.

href might appear like a rather obscure choice for an attribute name at first. If you are having trouble remembering it, remember that it stands for hypertext reference.

Add a link to your page now, if you haven't already done so.

## Semantics
In programming, Semantics refers to the meaning of a piece of code — for example "what effect does running that line of JavaScript have?", or "what purpose or role does that HTML element have" (rather than "what does it look like?".)

### Semantics in JavaScript
In JavaScript, consider a function that takes a string parameter, and returns an <li> element with that string as its textContent. Would you need to look at the code to understand what the function did if it was called build('Peach'), or createLiWithContent('Peach')?

### Semantics in CSS
In CSS, consider styling a list with li elements representing different types of fruits. Would you know what part of the DOM is being selected with div > ul > li, or .fruits__item?

### Semantics in HTML
In HTML, for example, the <h1> element is a semantic element, which gives the text it wraps around the role (or meaning) of "a top level heading on your page."

` <h1>This is a top level heading</h1> `

By default, most browser's user agent stylesheet will style an <h1> with a large font size to make it look like a heading (although you could style it to look like anything you wanted).

On the other hand, you could make any element look like a top level heading. Consider the following:

<span style="font-size: 32px; margin: 21px 0;">Is this a top level heading?</span>

This will render it to look like a top level heading, but it has no semantic value, so it will not get any extra benefits as described above. It is therefore a good idea to use the right HTML element for the right job.

HTML should be coded to represent the data that will be populated and not based on its default presentation styling. Presentation (how it should look), is the sole responsibility of CSS.

Some of the benefits from writing semantic markup are as follows:

- Search engines will consider its contents as important keywords to influence the page's search rankings (see SEO)
- Screen readers can use it as a signpost to help visually impaired users navigate a page
- Finding blocks of meaningful code is significantly easier than searching through endless divs with or without semantic or namespaced classes
- Suggests to the developer the type of data that will be populated
- Semantic naming mirrors proper custom element/component naming

When approaching which markup to use, ask yourself, "What element(s) best describe/represent the data that I'm going to populate?" For example, is it a list of data?; ordered, unordered?; is it an article with sections and an aside of related information?; does it list out definitions?; is it a figure or image that needs a caption?; should it have a header and a footer in addition to the global site-wide header and footer?; etc.

### Semantic elements
These are some of the roughly 100 semantic elements available:

`<article> <aside> <details> <figcaption> <figure> <footer> <header> <main> <mark> <nav> <section> <summary> <time> ` 


## HTML: HyperText Markup Language

HTML uses "markup" to annotate text, images, and other content for display in a Web browser. HTML markup includes special "elements" 
such as ` <head>, <title>, <body>, <header>, <footer>, <article>, <section>, <p>, <div>, <span>, <img>, <aside>, <audio>, <canvas>, <datalist>, <details>, <embed>, <nav>, <output>, <progress>, <video>, <ul>, <ol>, <li> ` and many others.

An HTML element is set off from other text in a document by "tags", which consist of the element name surrounded by "<" and ">".  
The name of an element inside a tag is case insensitive. That is, it can be written in uppercase, lowercase, or a mixture. 

