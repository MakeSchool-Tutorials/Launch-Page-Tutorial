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
}
```


# Adding Images

Above we added a "background image", but what if we just want to add a new element that is an image? We can use the `<img />` tag for that.

Now if we use the `<img />` by itself, the image will render as whatever size the image is. But what if we want the image to fit into the page as the size of its parent element. For that we will use Bootstrap's `img-fluid` class.



# Adding a Video

Nothing beats a good video to explain or show off a product, service, or organization.

If we want to embed a video and make it also scale to the size of its parent element we can use bootstrap's `embed-responsive` class and include our desired **Aspect Ratio**. For youtube vidoes that will be "16by9".

```html
<div class="embed-responsive embed-responsive-16by9">
  <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/zpOULjyy-n8?rel=0" allowfullscreen></iframe>
</div>
```
