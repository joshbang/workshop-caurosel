# workshop-caurosel
##Objective

Make a working carousel demo, like this one :
https://spencerkekauoha.github.io/lesson-carousel/

Like the example we will be using slick.
http://kenwheeler.github.io/slick/
I'm confident that there are other resources that we could use to accomplish the same thing. For now, we'll practice

We will need images to use in our carousel. I really like this resource:
https://unsplash.com/

##step one

Fork and clone this repo.

##step two

Familiarize yourself with the code. Get familiar particularly the index.html. You don't need to worry about the css for now. Open index.html in your browser or use live-server. See where the current picture of a horse is? That is where we are going to setup our carousel.

##step three

You can choose to install slick to use it, but we're going to use one of the CDN options. Let's follow the steps on https://github.com/kenwheeler/slick/. First lets link up their css in our html like so:

*index.html*
```html
<link rel="stylesheet" type="text/css" href="//cdn.jsdelivr.net/jquery.slick/1.6.0/slick.css"/>
<!-- Add the slick-theme.css if you want default styling -->
<link rel="stylesheet" type="text/css" href="//cdn.jsdelivr.net/jquery.slick/1.6.0/slick-theme.css"/>
```

Then let's bring in the JavaScript. Before your closing ```<body>``` tag add:

*index.html*
```html
<script type="text/javascript" src="//cdn.jsdelivr.net/jquery.slick/1.6.0/slick.min.js"></script>
```


##step four

Now that we have slick brought in lets use it and write some jQuery. Create a carousel.js file in your directory. Set up your file with :

*carousel.js*

```javascript
$(document).ready(function(){



});

```

To actually use slick, select our carousel container and call the slick method on it like:

*carousel.js*

```javascript
$(document).ready(function(){

  $('.carousel-container').slick({
    autoplay: true
  });

});
```
Now make sure you  add it to the html.

*index.html*
```html
<script src="carousel.js" charset="utf-8"></script>
```

##step five

sweet! We have a carousel now but with only one picture. Go back to index.html and add some more images in our carousel container.

*index.html*
```html
<section class="carousel-container">
  <img src="img/Photo by Alex Blăjan _ Unsplash _ Unsplash.jpeg" alt="horse" />
  <img src="https://hd.unsplash.com/photo-1450052590821-8bf91254a353" alt="horse 2" />
  <img src="https://hd.unsplash.com/photo-1456880563181-32f48af98fb5" alt="horse 3" />
  <img src="https://hd.unsplash.com/photo-1438283173091-5dbf5c5a3206" alt="horse 4" />
</section>
```
