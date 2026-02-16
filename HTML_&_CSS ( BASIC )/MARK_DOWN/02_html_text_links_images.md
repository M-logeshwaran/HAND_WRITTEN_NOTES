📄 02_html_text_links_images.md

# HTML Text Formatting, Links and Images

This section covers:
- Text formatting tags
- Anchor (link) tag
- Image tag
- Attributes
- Favicon
- Mailto

---

# 1. Text Formatting Tags

HTML provides tags to style text.

## Bold Text

```html
<b>Bold Text</b>
<strong>Important Text</strong>

<b> → Makes text bold

<strong> → Bold + gives importance (semantic meaning)



---

Italic Text

<i>Italic Text</i>
<em>Emphasized Text</em>

<i> → Slanted text

<em> → Slanted + importance



---

Small and Mark

<small>Small Text</small>
<mark>Highlighted Text</mark>

<small> → Smaller size

<mark> → Highlighted background



---

Deleted and Inserted

<del>Deleted Text</del>
<ins>Inserted Text</ins>

<del> → Strike-through text

<ins> → Underlined inserted text



---

Subscript and Superscript

<p>a<sup>2</sup> + b<sup>2</sup></p>
<p>a<sub>2</sub> + b<sub>2</sub></p>

<sup> → Superscript

<sub> → Subscript



---

Abbreviation Tag

<abbr title="Data Structure">DS</abbr>

When hovering over text, full form appears.


---

2. Anchor Tag (Link)

Used to create hyperlinks.

<a href="https://google.com">Go to Google</a>


---

Open in New Tab

<a href="https://google.com" target="_blank">Open</a>

target="_blank" → Opens in new tab.


---

Mail Link

<a href="mailto:mg.logesh55@gmail.com">
    Email Me
</a>

Clicking opens email application.


---

3. Image Tag

Used to insert images.

<img src="image.jpg">

Image tag is an empty element (no closing tag).


---

Important Attributes

<img src="image.jpg"
     height="200px"
     width="200px"
     alt="This is image">

src → Image path

height → Image height

width → Image width

alt → Shown if image not found



---

Relative Path Example

<img src="images/gow2.jpg">

Image must be inside folder.


---

4. Linking Image as Logo

<a href="index.html">
    <img src="logo.png" height="40px">
</a>

Clicking image navigates to page.


---

5. Title Attribute

<img src="kratos.jpg"
     title="Kratos (GOW2)">

When hovering image, tooltip appears.


---

6. Favicon (Website Tab Icon)

Placed inside <head> tag.

<head>
    <title>Games</title>
    <link rel="icon"
          type="image/x-icon"
          href="images/gow2.ico">
</head>

Favicon appears in browser tab.


---

7. Multiple Tags Inside Each Other

HTML allows nested tags.

<h1>
    <small><mark>Welcome</mark></small>
</h1>

Tags can be used inside other tags.

---
