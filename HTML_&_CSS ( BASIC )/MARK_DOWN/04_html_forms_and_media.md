📄 04_html_forms_and_media.md

# HTML Forms and Media

This section covers:
- Form structure
- Input types
- Radio and Checkbox
- Action attribute
- Placeholder, Value, Disabled
- Fieldset and Legend
- Background image
- Border radius for images and tables

---

# 1. Basic Form Structure

```html
<form>
    <label>Name</label>
    <input type="text">
    <br>

    <label>Password</label>
    <input type="password">
    <br>

    <input type="submit">
</form>

<form> → Container for form elements

<label> → Text label

<input> → Input field


<input> is an empty element (no closing tag).


---

2. Input Types

Text

<input type="text">


---

Password

<input type="password">

Text will be hidden.


---

Date

<input type="date">


---

Submit

<input type="submit">

Submits form.


---

3. Radio Button

Used to select one option.

<label>Male</label>
<input type="radio" name="gender">

<label>Female</label>
<input type="radio" name="gender">

Important: Radio buttons must have same name to select only one.


---

4. Checkbox

Used to select multiple options.

<input type="checkbox" id="agree">
<label>Terms & Condition</label>


---

5. Form Action Attribute

Used to navigate to another page after submit.

<form action="index.html">

When submit button is clicked, it navigates to the given file.


---

6. Placeholder, Value and Disabled

<input type="text"
       placeholder="Enter Name"
       value="Default"
       disabled>

placeholder → Hint text

value → Default value

disabled → Cannot edit



---

7. Fieldset and Legend

Used to group form elements.

<fieldset>
    <legend>Sign Up Form</legend>

    <form>
        <input type="text">
    </form>
</fieldset>

Creates bordered box around form.


---

8. Background Image

<body style="background-image: url(image.jpg);">

Adds background image to page.


---

9. Border Radius (Rounded Corners)

For Image

<img src="image.jpg"
     style="width:150px;
            height:150px;
            border-radius:50%;">

Note: For circle, width and height must be equal.


---

For Table

<table style="border:1px solid;
              border-radius:15px;">


---

For Fieldset

<fieldset style="border-radius:30px;
                 padding:5px;">


---

Summary

<form> collects user input.

<input> supports multiple types.

Radio → single selection.

Checkbox → multiple selection.

action navigates to another file.

fieldset groups form elements.

border-radius creates rounded corners.
