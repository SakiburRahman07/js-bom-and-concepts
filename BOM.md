# The Browser Object Model (BOM)

The **Browser Object Model (BOM)** allows JavaScript to interact directly with the browser window. While there are no official standards for the BOM, modern browsers generally implement similar methods and properties that enable dynamic user interaction.

## The Window Object

The `window` object is a core element of the BOM and is supported by all browsers. It represents the browser's window and serves as the global context for all JavaScript code. This means:

- **Global objects, functions, and variables** in JavaScript automatically become properties or methods of the `window` object.
- The `document` object (from the HTML DOM) is also a property of `window`, so the following two lines are equivalent:

    ```javascript
    window.document.getElementById("header");
    // is the same as
    document.getElementById("header");
    ```

## Determining Window Size

The `window` object provides properties to determine the inner dimensions (in pixels) of the browser window:

- **`window.innerHeight`** - Returns the inner height of the browser window (excluding toolbars and scrollbars).
- **`window.innerWidth`** - Returns the inner width of the browser window.

For example:

```javascript
let width = window.innerWidth;
let height = window.innerHeight;
console.log(`Window Width: ${width}, Window Height: ${height}`);
```
## Other Useful Window Methods

The `window` object includes several useful methods for managing the browser window:

- **`window.open()`** - Opens a new window.
- **`window.close()`** - Closes the current window.
- **`window.moveTo()`** - Moves the current window to a specified position on the screen.
- **`window.resizeTo()`** - Resizes the current window to a specified width and height.

### Example: Opening a New Window and Resizing It

Here’s a simple example that opens a new window and resizes it to a custom size:

```javascript
let newWindow = window.open("https://example.com", "Example", "width=300, height=200");

// Resize the new window after 3 seconds
setTimeout(() => {
  newWindow.resizeTo(500, 400);
}, 3000);
```
In this example, the new window opens with an initial width of 300 pixels and a height of 200 pixels. After 3 seconds, it’s resized to 500 by 400 pixels.
# JavaScript Window Screen

The `window.screen` object contains information about the user's screen. This object can be accessed directly without the `window` prefix.

## Properties of the `window.screen` Object

- **screen.width**: Returns the width of the screen in pixels.
- **screen.height**: Returns the height of the screen in pixels.
- **screen.availWidth**: Returns the available width of the screen, excluding system UI elements.
- **screen.availHeight**: Returns the available height of the screen, excluding system UI elements.
- **screen.colorDepth**: Returns the color depth of the screen, in bits.
- **screen.pixelDepth**: Returns the pixel depth of the screen, in bits.

### Window Screen Width

The `screen.width` property returns the width of the visitor's screen in pixels.

**Example**

Display the width of the screen in pixels:

```javascript
document.getElementById("demo").innerHTML = "Screen Width: " + screen.width;

