📄 01_html_basics_structure.md

# HTML Basics and Document Structure

HTML (HyperText Markup Language) is used to create the structure of a web page.

It defines:
- Headings
- Paragraphs
- Images
- Links
- Tables
- Forms

HTML is NOT case sensitive.
(Recommended to write all tags in lowercase)

---

# 1. Basic HTML Document Structure

Every HTML page must follow this structure:

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>
</head>
<body>

    <h1>Hello World</h1>

</body>
</html>

Explanation:

<!DOCTYPE html>
Tells the browser that this document uses HTML5.

<html>
Root element. Everything must be inside this tag.

<head>
Contains meta information (title, CSS link, etc.)

<title>
Shows page title in browser tab.

<body>
Contains visible content of website.



---

2. Comments in HTML

Used for developer understanding. Not displayed in browser.

<!-- This is a comment -->

Comments are helpful for:

Explaining code

Temporarily disabling code



---

3. Heading Tags

HTML provides 6 heading levels.

<h1>Main Heading</h1>
<h2>Sub Heading</h2>
<h3>Section Heading</h3>
<h4></h4>
<h5></h5>
<h6></h6>

<h1> → Largest

<h6> → Smallest

Used for structure and SEO



---

4. Paragraph Tag

Used to write text content.

<p>I am a software developer.</p>

Each paragraph automatically starts on a new line.


---

5. Line Break and Horizontal Rule

Line Break

<br>

Moves content to next line.


---

Horizontal Line

<hr>

Creates a horizontal divider line.

Both <br> and <hr> are empty elements. (No closing tag required)


---

6. Case Sensitivity

HTML is NOT case sensitive.

Both work:

<H1>Hello</H1>
<h1>Hello</h1>

But best practice: Always use lowercase.

---
