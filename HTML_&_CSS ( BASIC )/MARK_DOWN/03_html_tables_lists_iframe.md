📄 03_html_tables_lists_iframe.md

# HTML Tables, Lists, Div, Span and Iframe

This section covers:
- Tables
- Caption
- Colspan and Rowspan
- Lists (Ordered & Unordered)
- Div and Span
- ID navigation
- Iframe

---

# 1. Tables in HTML

Used to display structured data in rows and columns.

Basic structure:

```html
<table>
    <thead>
        <tr>
            <th>SNO</th>
            <th>Project Name</th>
            <th>Language</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>1</td>
            <td>DBMS</td>
            <td>Python</td>
        </tr>

        <tr>
            <td>2</td>
            <td>Hand Cricket</td>
            <td>Python</td>
        </tr>
    </tbody>
</table>


---

2. Table Tags Explanation

<table> → Main table

<thead> → Header section

<tbody> → Body section

<tr> → Table row

<th> → Table header (bold by default)

<td> → Table data cell



---

3. Table Caption

<table>
    <caption>My Projects</caption>
</table>

Caption appears above the table.


---

4. Colspan

Used to merge columns.

<th colspan="2">P-Name</th>

This makes one header cover two columns.


---

5. Rowspan

Used to merge rows.

<td rowspan="2">Common Data</td>

One cell covers two rows.


---

6. Table Border and Size

<table style="border:1px dashed;">

Increase width or height:

<table width="300px" height="300px">


---

7. Lists in HTML

7.1 Unordered List (No numbers)

<ul>
    <li>Line 1</li>
    <li>Line 2</li>
</ul>


---

7.2 Ordered List (Numbered)

<ol>
    <li>Line 1</li>
    <li>Line 2</li>
</ol>


---

7.3 Ordered List Type

<ol type="A">

Types:

"1"

"A"

"a"

"I"

"i"



---

7.4 Nested Lists

Lists can be inside another list.

<ul>
    <li>Main Item
        <ul>
            <li>Sub Item</li>
        </ul>
    </li>
</ul>


---

8. Div and Span

Div

Block element. Used to group elements.

<div>
    <p>Content</p>
</div>


---

Span

Inline element. Used for styling part of text.

<span>Inline text</span>


---

9. ID Navigation (Internal Link)

Assign id:

<img src="image.jpg" id="name">

Link to it:

<a href="#name">Go to Image</a>

When clicked, page scrolls to that element.

Only one id value can be used per page.


---

10. Iframe

Used to display another webpage inside current webpage.

<iframe src="name.html"></iframe>

Loads another HTML file inside page.
