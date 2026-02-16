📄 06_css_layout_flexbox.md

# CSS Layout and Flexbox

Flexbox is used to arrange elements in a flexible way.

It helps to:
- Align items
- Create horizontal layouts
- Make responsive layouts
- Control spacing

---

# 1. Display Flex

To make a container flex:

```css
div {
    display:flex;
}

All child elements become flex items.


---

2. Justify Content

Controls horizontal alignment.


---

Space Between

div {
    display:flex;
    justify-content:space-between;
}

First item → left
Last item → right
Equal space between items.


---

Space Around

div {
    display:flex;
    justify-content:space-around;
}

Equal space around each item.


---

Space Evenly

div {
    display:flex;
    justify-content:space-evenly;
}

Equal space everywhere.


---

3. Flex Wrap

Used when items exceed container width.

div {
    display:flex;
    flex-wrap:wrap;
}

If child elements exceed width, they move to next line automatically.


---

4. Image Card Example (Hover + Transition)

HTML:

<img src="image.jpg" class="imgs">

CSS:

.imgs {
    width:400px;
    height:400px;
    border-radius:30px;
    transition:0.3s ease;
}


---

5. Hover Effect (Zoom)

.imgs:hover {
    transform:scale(1.2);
    cursor:pointer;
}

When hovering:

Image zooms

Cursor changes



---

6. Box Shadow

Used to create shadow effect.


---

Outer Shadow

box-shadow:0px 0px 15px black;


---

Inner Shadow

box-shadow:0px 0px 15px black inset;

Shadow inside element.


---

7. Flex Container Example

.container {
    display:flex;
    justify-content:space-evenly;
    flex-wrap:wrap;
}

Used for:

Navigation bar

Card layouts

Product grids
