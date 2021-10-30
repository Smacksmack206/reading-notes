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

Google analyitics is one of the best free tools available for webmasters, web admins, and websites to track numerous KPIs like page visits, reffering domain, link clicks, etc.
Setting up GA on a site is easy and quick, you would just need to add code to the head of your site which you can find in the GA Docs.