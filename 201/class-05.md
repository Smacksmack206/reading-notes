#Cedric's Notes for code-201n24 course

# <cite> Reading from the Jon Duckett HTML & CSS </cite>

## Images (pp. 94-125)

#### Adding Images

`<img>`
To add an image into the page you need to use an `<img>` element. this is an empty element (which means there is no closing tag).
it must carry the following two attributes:

`src` 
This tells the browser where it can find the image file.
This will usually be a relative URL pointed to an image on your own site. (in the image folder).

`alt`
This provides a text description of t he image which describes the image if you can't see it.

`title`
YOu can also use the title attribute with the `<img>` element to provide additional infomation about the image. Most browser will display the content of this attribute in a tooltip when the user hovers over the image.


#### Three Rules for Creating Images

There are three rules to remember when you are creating images for your site whichc are summarized below:

- Save images in the right format

Websites mainly use images in jpeg, gif, or png format. If you choose the wrong image format then your image might not look as sharp

- Save images at the right size

You should save the image at the same width and height it will appear on the site (measured in pixels). If the image is smaller than the width or the height that you have specificed the image can be distored or streched.
If the image is larger than the width and height you specified the image will take longer to display on the page.

- Measure Images in Pixels

Computer screens are made up of tiny squares known as pixels shown per inch of screen can vary if the user increases or decreases the resolution. Therefore , when you are saving images at the right size for use on the web, you should alway measure the image in terms of the width and height in pixels.


#### Figure and Figure Caption

Images often come with captions and in HTML5 they introduced the following elements that match the image and captions.

`<figure>` Element you add img tags in between. the figure element is used outside of the `<figcaption>` which holds the caption.

Example:

``` <figure>
<img src="images/otters.jpg" alt="Photograph of two sea otters floating in water" />
<br />
<figcaption>Sea Otters blank blank blank </figcaption>
</figure> ```

## Color (pp. 246-263)

### Foreground Color

`color`
The color property allows you to specify the color of text inside of an element, you can specify any color in CSS in one of three ways.

RGB Values, HEX Codes, or Color Names

### Background Color

`background-color`
CSS treats each HTML element as if it appears in a box, and the background-color property sets the color of the background for that box.

You can specify your choice of backgound color in the same threee ways you can specify foreground colors: RGB Values, HEX Codes, or Color Names.

### Opacity
`opacity, rgba`
The Opacity property allws you to specifcy the opacity of an element and any of its child elements


## Text (pp.264-299)

### Specifying Typefaces

`font-family`

The font-family property allows you to specify the typeface that should be used for any text inside elements(s) to which a CSS rules apply.

`font-size`

The font-size property enables you to specify a size for the font.
There are several ways to specify the size of a font. The most commmon ways are:

`Pixels`
Pixels are commonly used because they alllow web designers very percise control over how much space their text takes up.

`Percentages`
The default size of text in the browsers is 16px. Sow a size of 75% would be the equivalent of 12px, and 200% would be 32px.

`EMS`
An em is equvilent to the width of a letter m.


