---
title: "Get started with writing tutorials!"
slug: getting-started
---

**The above title becomes the tutorials first header**, so an introduction to the tutorial page should be given here **before** any more headers are created.

# Supported syntax

## Headers

Use `#` to create new headers.

```
# This is an h1 header, use to partition page into steps
## This is an h2 sub-header
### This is an h3 sub-header
#### This is an h4 sub-header
```

Each `h1` header creates a "Mark Complete" button for content between it and next `h1` header. **_Make sure there is a full "step" of content for each `h1` header._**

## Text formatting

- Italics can be done with _underscores_. Use italics for the name of applications and introducing new concepts.
- Bold can be done with **asterisks**. Use bold for names of buttons.
- Bold-italics can be done with **_asterisks around underscores_**.
- Strikethrough can be done with ~~two tildes~~.
- Inline code references (file names, class names, function names, etc) can be made with `back-ticks`, code blocks are discussed below.

## Links

[This](https://github.com/MakeSchool-Tutorials/Tutorial-Template) creates a link. Relative links should only be used when [linking to assets in the repository](assets/ms-logo.png).

_Relative links to files in the same works on makeschool.com but the links will not do anything when clicked from ms-markdown-preview._

## Images

Images syntax is similar to links and will work with most image types (including `gif`). Images should be located in the page's `assets` folder and referenced locally. This syntax transforms into an HTML image tag.

```
![Alt text](assets/image_name.png "Title text")
```

turns into

```
<img src="assets/image_name.png" alt="Alt text" title="Title text">
```

Make sure that every image has both alt and title text defined. Both are important for SEO. Alt text is displayed when a user is has images disabled. Title text is displayed when a user hovers over the image.

![Make School logo](assets/ms-logo.png "Make School")

## Other embedded assets

The renderer has overhauled the image syntax for embedding MP4 videos, YouTube videos, and PDF files.

### YouTube

The following syntax will embed a YouTube video into the tutorial. The video must be embeddable (see video's settings on YouTube).

![ms-video-youtube](https://www.youtube.com/watch?v=6rT00QXqZak)

### MP4/MOV

The following syntax will embed an MP4/MOV video with controls. Videos can be referenced with URLs or relative links if they are included in the repository. This works great with short screencasts made with QuickTime.

![ms-video](assets/short-video.mov)

### PDF

The following syntax will embed a PDF for viewing in-line. PDFs can be referenced with URLs or relative links if they are included in the repository.

![ms-pdf](assets/empty-slides.pdf)

Images can also be included by full URL. This should be avoided in favor of images being stored in the tutorial repository.

## Lists

### Unordered lists

- This is an unordered list
- The space after the `-` is necessary!

### Ordered lists

1. This is an ordered list
1. With multiple items
1. Use one and let the processor count for you or the linter will get angry!
1. But don't be lazy...

### Nested lists

1. This is a nested list
    1. Use four spaces for each level
    1. More nested items

1. Formatting can get a little weird so only nest once!
    - You can even combine ordered and unordered lists when nesting
    - Just remember to use four spaces for each level

1. Such an amazing list

## Tables

We also support markdown tables!

| This is a header    | This is another header |
|:--------------------|:-----------------------|
| Sample contents     | Such table             |
| So nicely formatted | Much wow               |

## Code blocks

Always use fenced code blocks. Do not use indented code blocks in any new tutorials! Fenced code blocks allow you to specify the language of a code sample and are easier to edit.

```
// Code within fenced code blocks should be left-aligned!
print("Hello, Make School!")
print("Follow each language's style guide.")

if containsIndentation {
  print("Be consistent with number of spaces in indentation.")
}
```

### Overriding auto-detected language

Linguist will sometimes fail to classify a code sample's language correctly. When this happens (you'll notice while checking `ms-markdown-preview`), label the code block with the correct language.

#### This is incorrectly classified as Ruby

```
<h1>Hello, Rails!</h1>
```

#### This forces Highlight to recognize it as HTML

```html
<h1>Hello, Rails!</h1>
```

This works for most languages we use at Make School (html, css, js, pug, etc.). Make sure to preview them in `ms-markdown-preview` to insure that they appear correctly.

# Action highlights

Read about the following boxes and use them when appropriate.

## Quote box

Use quote boxes to include a quote.

> I think everyone should learn how to program a computer, because it teaches you how to think. I view computer science as a liberal art, something everyone should learn to do.
>
> - Steve Jobs

## Info box

Use info boxes to draw a students attention to an important concept.

> [info]
> Important concepts should be recapped or summarized in info boxes.

## Action box

Use action boxes whenever the student should do something (add code, implement pseudocode, change IDE settings, download files, etc).

> [action]
> Add the following import statement to the top of _TimelineViewController.swift_:
>
```
import ConvenienceKit
```
>
> This is still part of the box! Remember, code blocks need an empty line above them. In the case of code blocks inside of boxes, the line before and after a code block should only contain a `>` character.

This is no longer part of the box.

## Solution box

Use solution boxes to keep a solution hidden until the student hovers over it. These should be placed after a student has been asked to try implementing something themselves.

> [solution]
> This content is hidden until the user hovers over the box. Check it out with ms-markdown-preview!
>
```
import ConvenienceKit
```

This is not part of the box.

## Challenge box

Use challenge boxes should be used for additional features the user might want to implement.

> [challenge]
> Would you kindly add a high score popup?
>
> The game could use some social integration as well!

This is not part of the box.

## Boxes followed by boxes

### This will not render correctly

```
> [action]
> Try viewing this with ms-markdown-preview!

> [info]
> The renderer will treat these as the same box :(
```

### This will render correctly

> [action]
> Try viewing this with ms-markdown-preview!

<!--  -->

> [info]
> Adding an empty comment forces the renderer to treat these as separate boxes :D
>
> The comment needs an empty line above and below it!

## Code blocks within action highlight boxes

> [info]
> Fenced code blocks exit prematurely if they contain an empty line while within an action highlight box. **To fix this, you will need to include a `>` on each empty line within the fenced code block!**
>
```
import ConvenienceKit
>
func doesNothing() {
>
}
```
>
> This will not render correctly without the `>` on empty lines within the fenced code block.
