📄 07_css_animation_and_media.md

# CSS Animation and Media Query

CSS allows smooth transitions and animations.

Used for:
- Hover effects
- Moving elements
- Interactive UI
- Responsive design

---

# 1. Transition

Transition makes property changes smooth.

Basic syntax:

```css
transition: duration timing-function;

Example:

img {
    transition:0.3s ease;
}

When property changes (like scale, color), it changes smoothly.


---

2. Transform

Used to change size, position, rotation.


---

Scale (Zoom)

.img:hover {
    transform:scale(1.1);
}

Increases size when hovering.


---

Rotate

.img:hover {
    transform:rotate(10deg);
}

Rotates element.


---

3. Hover Effect

button:hover {
    background-color:black;
    color:white;
}

Changes style when mouse is over element.


---

4. Basic Animation

Animation uses @keyframes.

Example:

@keyframes move {
    from {
        left:0px;
    }
    to {
        left:200px;
    }
}

Apply animation:

.box {
    position:relative;
    animation:move 2s infinite;
}

Moves box continuously.


---

5. Media Query (Basic Responsive)

Used to apply styles for different screen sizes.

Example:

@media screen and (max-width:600px) {
    body {
        background-color:lightblue;
    }
}

When screen width is less than 600px, style changes.

Used for:

Mobile layout

Responsive design
