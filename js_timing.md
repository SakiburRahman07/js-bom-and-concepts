
# JavaScript Timing Events

JavaScript allows the execution of code at specified time intervals. These intervals are known as timing events, which are primarily managed using the `setTimeout()` and `setInterval()` methods.

## Timing Events Overview

The `window` object provides two key methods to control timing events:

1. **setTimeout(function, milliseconds)** - Executes a function after waiting a specified number of milliseconds.
2. **setInterval(function, milliseconds)** - Repeats the execution of a function continuously at the specified time interval.

These methods are both part of the HTML DOM `Window` object.

---

### The `setTimeout()` Method

Syntax:
```javascript
window.setTimeout(function, milliseconds);
```

- The `setTimeout()` method can be called without the `window` prefix.
- The first parameter is a function to be executed.
- The second parameter is the time to wait in milliseconds before executing the function.

Example:
```html
<button onclick="setTimeout(myFunction, 3000)">Try it</button>

<script>
function myFunction() {
  alert('Hello');
}
</script>
```

### Stopping Execution with `clearTimeout()`

The `clearTimeout()` method stops the execution of a function set by `setTimeout()` if it hasn’t yet executed.

Syntax:
```javascript
window.clearTimeout(timeoutVariable);
```

Example with a Stop Button:
```html
<button onclick="myVar = setTimeout(myFunction, 3000)">Try it</button>
<button onclick="clearTimeout(myVar)">Stop it</button>
```

---

### The `setInterval()` Method

Syntax:
```javascript
window.setInterval(function, milliseconds);
```

- The `setInterval()` method can be called without the `window` prefix.
- The first parameter is the function to execute.
- The second parameter specifies the interval in milliseconds between each execution.

Example (Display the current time every second):
```html
<p id="demo"></p>

<script>
setInterval(myTimer, 1000);

function myTimer() {
  const d = new Date();
  document.getElementById("demo").innerHTML = d.toLocaleTimeString();
}
</script>
```

### Stopping Execution with `clearInterval()`

The `clearInterval()` method stops repeated executions of a function set by `setInterval()`.

Syntax:
```javascript
window.clearInterval(timerVariable);
```

Example with a Stop Button:
```html
<p id="demo"></p>

<button onclick="clearInterval(myVar)">Stop time</button>

<script>
let myVar = setInterval(myTimer, 1000);
function myTimer() {
  const d = new Date();
  document.getElementById("demo").innerHTML = d.toLocaleTimeString();
}
</script>
```

---

## Summary

- **setTimeout()**: Executes a function after a specified delay.
- **clearTimeout()**: Stops a timeout before it executes.
- **setInterval()**: Repeats a function at a specified interval.
- **clearInterval()**: Stops a repeated interval.

Use these methods to manage time-based actions in your JavaScript code!
