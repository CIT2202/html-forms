# HTML Forms
The following provides an overview of HTML forms. Here's a simple HTML form.

```html
<form>
<div>  
<label for="firstname">First Name:</label>
<input type="text" name="fname" id="firstname">
</div>
<div>
<label for="secondname">Second Name:</label>
<input type="text" name="secName" id="secondname">
</div>
<input type="submit">
</form>
```

Here's what this form would look like in a browser:-

---

<form action="process.php" method="POST">
<div>  
<label for="firstname">First Name:</label>
<input type="text" name="fname" id="firstname">
</div>
<div>
<label for="secondname">Second Name:</label>
<input type="text" name="secName" id="secondname">
</div>
<input type="submit">
</form>

---

## The ```<form>``` tags
The ```<form>``` element is simply a container that marks out the start and end of the form. Every form must have an opening and a closing ```<form>``` tag!

## Form Controls
Text fields, buttons, checkboxes etc. are known as form controls.
Most form controls are specified by the ```<input>``` tag
The ```type``` attribute specifies the type of form control. In this example *text* for a text field

```html
<input type="text" name="fname" id="firstname" value="Fred">
```

* The *name* attribute is used to identify data when sent to a web server
* The *value* attribute is the actual data that will be sent. For text fields the user would type this in. In this example I have added a value as an HTML attribute so we can see the effect.
This form control would be rendered as:

  <input type="text" name="fname" id="firstname" value="Fred">

## The ```<label>``` element

The ```<label>``` element associates a label with a form control.

```html
<label for="firstname">First Name:</label>
<input type="text" name="fname" id="firstname">
```
The *for* attribute links the label to a specific *id* attribute. In this example *firstname*. This is for accessibility reasons. Visually impaired users may not be able to see what the purpose of a form control is, the ```<label>``` element explicitly links a description to the form control.

## Buttons
By changing the *type* attribute, we can specify a submit button instead of a text field e.g.
```html
<input type="submit">
```
When the user clicks the submit button, the data in the form will be sent to the server for processing.

## Checkboxes
By changing the *type* attribute, we can specify a checkbox instead of a text field.

```html
<div>
<input  type="checkbox" name="info" id="info">
<label for="info">Tick this box if you would like to receive more
information</label>
</div>
```
This would be rendered as:-

  <div>
  <input  type="checkbox" name="info" id="info">
  <label for="info">Tick this box if you would like to receive more
  information</label>
  </div>

## Radio Buttons
Radio buttons work as a group
* If you select one button the other buttons are automatically deselected.
* Each radio button **must** have the same **name** because they are all part of the same group.

```html
<fieldset>
<legend>Which of these is not a colour of the rainbow</legend>
<input type="radio" name="colours" id="red"> <label for="red">Red</label>
<input type="radio" name="colours" id="silver"> <label for="silver">Silver</label>
<input type="radio" name="colours" id="blue"> <label for="blue">Blue</label>
</fieldset>
```

* The ```<fieldset>``` is used to group a collection of form controls together.
* The ```<legend>``` element provides a label for the ```<fieldset>```

These radio buttons would be rendered as:-


<fieldset>
<legend>Which of these is not a colour of the rainbow</legend>
<input type="radio" name="colours" id="red"> <label for="red">Red</label>
<input type="radio" name="colours" id="silver"> <label for="silver">Silver</label>
<input type="radio" name="colours" id="blue"> <label for="blue">Blue</label>
</fieldset>

## Learning More
Have a look at MDN for useful info on forms, specifically:-
* https://developer.mozilla.org/en-US/docs/Learn/Forms/Your_first_form
* https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form
* https://developer.mozilla.org/en-US/docs/Learn/Forms/Basic_native_form_controls
* https://developer.mozilla.org/en-US/docs/Learn/Forms/HTML5_input_types
* https://developer.mozilla.org/en-US/docs/Learn/Forms/Styling_web_forms
