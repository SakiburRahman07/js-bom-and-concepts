
# JavaScript Popup Boxes

JavaScript provides three types of popup boxes: the Alert box, Confirm box, and Prompt box.

## Alert Box

An alert box is used to ensure that information is communicated to the user. When an alert box appears, the user must click "OK" to continue.

### Syntax

```javascript
window.alert("sometext");
```

The `window.alert()` method can be used without the `window` prefix.

### Example

```javascript
alert("I am an alert box!");
```

## Confirm Box

A confirm box is used to ask the user to verify or accept something. When it appears, the user must click "OK" or "Cancel" to proceed.

- If the user clicks "OK," the box returns `true`.
- If the user clicks "Cancel," the box returns `false`.

### Syntax

```javascript
window.confirm("sometext");
```

The `window.confirm()` method can also be written without the `window` prefix.

### Example

```javascript
if (confirm("Press a button!")) {
  txt = "You pressed OK!";
} else {
  txt = "You pressed Cancel!";
}
```

## Prompt Box

A prompt box requests the user to input a value before continuing. When the prompt box appears, the user must enter a value and click "OK" or "Cancel."

- If the user clicks "OK," the box returns the input value.
- If the user clicks "Cancel," the box returns `null`.

### Syntax

```javascript
window.prompt("sometext", "defaultText");
```

The `window.prompt()` method can be written without the `window` prefix.

### Example

```javascript
let person = prompt("Please enter your name", "Harry Potter");
let text;
if (person == null || person == "") {
  text = "User cancelled the prompt.";
} else {
  text = "Hello " + person + "! How are you today?";
}
```

## Displaying Line Breaks

To add line breaks in a popup box, use a backslash followed by the character `n`.

### Example

```javascript
alert("Hello\nHow are you?");
```

---

These popup boxes are useful for providing information, confirming actions, or getting input from users.
