---
title: "Images and Videos"
slug: images-and-videos
---

Let's continue customizing!

There's a lot you can do with HTML, just to get a taste, we can add some images and even embed some videos into this launch page.

# Adding Background Images

First let's add a background image to our Hero. [Unsplash](https://unsplash.com/) is a great place to find some free photographs.

Pick a photo, download it, and add it to your project folder.

Now we can add this to your hero jumbtron.

Add the second class `hero-background-img` to your hero jumbotron, and now define that class in your css:

```css
/* styles.css */

.hero-background-img {
  background-image: url("file-name.png");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
```

How does that look?

You can make the tag taller using padding on the top and bottom:

```css
.hero-background-img {
  background-image: url("file-name.png");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  padding-top:200px;
  padding-bottom:200px;
}
```

Is your text still readable? Try adding a background shadow to the image. That takes using a "pseudo class" `:after`

```css
.hero-background-img {
  position: relative;
  background: rgba(0, 0, 0, 0.3); /* If our image is bright, we can tone it down with this darker overlay */
  padding-top:200px;  
  padding-bottom:200px;
}

.hero-background-img:after {
  content: "";
  position: absolute;
  background-image: url("file-name.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: -1;
  opacity: 0.5; /* Tone the image down further by giving it transparency */
}

```

Try swapping in a few pictures, until you get one you like.

# Adding Images

Above we added a "background image", but what if we just want to add a new element that is an image? We can use the `<img />` tag for that.

Now if we use the `<img />` by itself, the image will render as whatever size the image is. But what if we want the image to fit into the page as the size of its parent element. For that we will use Bootstrap's `img-fluid` class.

We can add an image below the benefits. Grab another image from unsplash and lets add it:

```html
  <!-- BENEFITS -->
  <div class="container mb-5 mt-5">
    <!-- THE BENEFITS COLUMNS -->

    <div class="row m-5">
      <div class="col-lg-6 offset-lg-3">
        <img src="cat.jpg" class="img-fluid rounded">
      </div>
    </div>
  </div>
```

In this code we are using the `rounded` bootstrap **Utility Class** to round the corners of the image. We are also using the `m-5` to give it a large margin all the way around it.

Great!

# Adding a Video

Nothing beats a good video to explain or show off a product, service, or organization.

If we want to embed a video and make it also scale to the size of its parent element we can use bootstrap's `embed-responsive` class and include our desired **Aspect Ratio**. For youtube vidoes that will be `16by9`.

When adding YouTube videos, you want to grab the **embedded** url, and not the regular one that you see when watching a video.

> [action]
>
> Watch this short vifeo on how to get the embed link from a YouTube Video:
>
> ![ms-video](assets/embed_youtube.mov)

Try commenting out your image and put this instead. Remember to replace the youtube link with the video you'd like to use.

```html
<div class="embed-responsive embed-responsive-16by9">
  <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/zpOULjyy-n8?rel=0" allowfullscreen></iframe>
</div>
```

Onward!
