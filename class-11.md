#Cedric's Notes for code-201n24 course

# <cite> Reading from the Jon Duckett HTML book && W3Schools </cite>

## Images (pp.406-427)


You can use height and width attributes on CSS to transform a image to your desired size - this is useful when you have a mockup or a design in mind and want the image to be porportioned a certain way.

You can create animated images by using GIFs in HTML.

## Common Image Formats
Here are the most common image file types, which are supported in all browsers (Chrome, Edge, Firefox, Safari, Opera):

**Abbreviation**|**File Format**|**File Extension**
:-----:|:-----:|:-----:
APNG|Animated Portable Network Graphics|.apng
GIF|Graphics Interchange Format|.gif
ICO|Microsoft Icon|.ico, .cur
JPEG|Joint Photographic Expert Group image|.jpg, .jpeg, .jfif, .pjpeg, .pjp
PNG|Portable Network Graphics|.png
SVG|Scalable Vector Graphics|.svg

## Background Images

The background-image attribute in CSS allows you to use any image as a background. If the image is too small, it repeats its self on the page. You can use the background-repeat attribute to stop it from repeating on the page.

```
<style>
body {
  background-image: url('example_img_girl.jpg');
}
</style>
```


## Background Cover
If you want the background image to cover the entire element, you can set the background-size property to cover.

Also, to make sure the entire element is always covered, set the background-attachment property to fixed:

This way, the background image will cover the entire element, with no stretching (the image will keep its original proportions):


```
<style>
body {
  background-image: url('img_girl.jpg');
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: cover;
}
</style>
```

## HTML5 video and audio (MDN)
The `<video>` and `<audio>` elements allow us to embed video and audio into web pages. As we showed in Video and audio content, a typical implementation looks like this:

```
<video controls>
  <source src="rabbit320.mp4" type="video/mp4">
  <source src="rabbit320.webm" type="video/webm">
  <p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.mp4">link to the video</a> instead.</p>
</video>
```

Link to doc explaining video controls in depth:
https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Video_and_audio_APIs



## Practical information (pp.476-492)

SEO requires accurate use of elements giving the webpage semantic information Search Engines can use to give context and define a webpage for users to search within the entire indexable web, using the right elements increases the relavency and chances targeted traffic will land on your page as well as increase the chance for higher organic ranking. 

### How to identify keyowrds and phrases

Brainstorm - List down words someone might type into Google to find your site, include various services and products.

Organize - Group keywords into seprate lists for different sections or catagories of your site.

Research - Use Google Adwords, Wordtracker.com, or keyworddicovery.com to enter your keywords and get suggested addtional keywords to consider.

Compare - Look at the competition and optimize further by seeing how they optimized for a specific term.

Refine - Pick the keywords you want to focus on.

Map - Start picking keywords for each page.

### Anaytics: Learning about your vistiors

Signing up - The GA services relies on you signing up at:

`www.google.com/analytics`

How it works - Every times osmeone loads a page of your site, the trackign code sends data to the Google serverss where it is stored.
Google then provides a web-based interface that allows you to see how visstors use your site.

The tracking code - A tracking code is provided by Google Analytics for each website you are tracking. it should appear just before your `<head>` tag. The code does not alter the appearance of your page.


### How many people are coming to your site? (pp.484)

Visits
Unique Visits
Page Views
Pages per Visit
Average time on site
Date Selector
Export