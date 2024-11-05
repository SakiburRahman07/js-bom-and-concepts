
# JavaScript Window History

The `window.history` object contains the browser's history.

## Window History

The `window.history` object can be written without the `window` prefix.

To protect the privacy of the users, there are limitations to how JavaScript can access this object.

### Some Methods:

- `history.back()` - Same as clicking back in the browser.
- `history.forward()` - Same as clicking forward in the browser.

---

## Window History Back

The `history.back()` method loads the previous URL in the history list.

This is the same as clicking the Back button in the browser.

### Example

Create a back button on a page:

```html
<html>
<head>
<script>
function goBack() {
  window.history.back()
}
</script>
</head>
<body>

<input type="button" value="Back" onclick="goBack()">

</body>
</html>
```

---

## Window History Forward

The `history.forward()` method loads the next URL in the history list.

This is the same as clicking the Forward button in the browser.

### Example

Create a forward button on a page:

```html
<html>
<head>
<script>
function goForward() {
  window.history.forward()
}
</script>
</head>
<body>

<input type="button" value="Forward" onclick="goForward()">

</body>
</html>
```
