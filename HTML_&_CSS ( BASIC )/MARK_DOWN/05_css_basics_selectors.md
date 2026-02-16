📄 05_css_basics_selectors.md

# CSS Basics and Selectors

CSS = Cascading Style Sheets  
Used to style HTML elements.

CSS applies rules to selected HTML elements.

Basic CSS syntax:

selector {
    property: value;
}

---

# 1. Types of CSS

There are 3 types of CSS:

1. Inline CSS
2. Internal CSS
3. External CSS

---

# 1.1 Inline CSS

Written directly inside HTML tag.

```html
<h1 style="color:red;">
    Hello
</h1>

Applies style only to that element.


---

1.2 Internal CSS

Written inside <style> tag in <head>.

<head>
    <style>
        h3 {
            color:brown;
        }
    </style>
</head>

Applies style to whole page.


---

1.3 External CSS

Written in separate file (style.css).

HTML file:

<link rel="stylesheet" href="style.css">

CSS file (style.css):

h5 {
    color:blue;
}

Recommended method for large projects.


---

2. CSS Selectors

Selectors choose which HTML elements to style.


---

2.1 Tag Selector

h1 {
    color:red;
}

Applies to all h1 tags.


---

2.2 ID Selector

HTML:

<h1 id="welcome">Hello</h1>

CSS:

#welcome {
    color:green;
}

ID starts with #

Only one element should use same ID



---

2.3 Class Selector

HTML:

<h5 class="text">This is text</h5>

CSS:

.text {
    color:orange;
}

Class starts with .

Can be used for multiple elements



---

2.4 Universal Selector

* {
    margin:0;
}

Selects all elements.


---

2.5 Group Selector

h3, p {
    color:purple;
}

Applies same style to multiple tags.


---

3. Background Properties

body {
    background-image:url("image.jpg");
    background-repeat:no-repeat;
    background-attachment:fixed;
}

background-image → sets image

no-repeat → prevents repeating

fixed → background does not scroll



---

4. Border Radius

Rounded corners:

div {
    border-radius:15px;
}

For circle:

img {
    width:150px;
    height:150px;
    border-radius:50%;
}

Width and height must be equal.


---

5. Overflow

If content exceeds width:

div {
    width:200px;
    overflow:auto;
}

Adds scroll when content is large.


---

6. Transition (Basic)

Smooth effect when property changes.

img {
    transition:0.3s ease;
}

Used with hover effects.
