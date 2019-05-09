---
title: "Customizing Your Page"
slug: customizing-your-page
---

Now you have the baseline of your Launch Page, but nobody likes something so generic! Let's spice things up.

# Add a Theme

First off, the easiest thing you can do to add some uniqueness to your page is to use a **Bootstrap Theme**. Some themes are fancy, complex, and cost money, but we're just going to use a free one that skin's bootstrap itself without adding any extra components.

Navigate to [Bootswatch.com](https://bootswatch.com/) and pick a theme you like.

You can either download the `.min.css` file and add it to your project, or just use the url to link it in your head BELOW where you added bootstrap itself:

```html
```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>

  <!-- BOOTSTRAP -->
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css">
  <!-- BOOTSTRAP THEME -->
  <link rel="stylesheet" href="https://bootswatch.com/4/cyborg/bootstrap.min.css">

</head>
```

How's that look?

You might want to tweek your navbar to be either `navbar-light` or `navbar-dark` and change the background to `bg-white` or `bg-dark` or play with colors like: `bg-primary`, `bg-secondary` etc. And the footer too you might want to change.

# Customize the Navbar

Now we might want to make the Navbar a bit different. The easiest thing to do is change the height a little bit. We can do this by altering the padding a bit.

```css
.navbar {
  padding 1rem;
}
```

You might want to give it a custom color as well:

```css
.navbar {
  padding 1rem;
  background-color: blue;
}
```

To do this you'll have to remove any `bg-color` class you've added.

# Customize the Footer

Like the navbar, you can make the footer fatter and customize its color.

# Customize Your Forms

Form inputs and buttons are a good way to make your site a bit more unique. Explore changing some of the shapes and colors of your buttons.

You can add special `hover` effects like this:

```css
.btn-primary:hover {
  background-color: blue;
  color: white;
}
```

# Customize Title and Sharing

Let's also customize some of the meta data in the `<head>` tag.

Change the `<title></title>` tag to say something else, e.g. "Launch Page":

```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">

  <title>My Launch Page</title>

  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css">
  <link rel="stylesheet" href="https://bootswatch.com/4/cyborg/bootstrap.min.css">
</head>
```

The title tag also is displayed in the tab of the browser. Can you add an emoji here?
