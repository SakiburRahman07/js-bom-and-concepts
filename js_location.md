
# JavaScript Window Location

The `window.location` object can be used to get the current page address (URL) and to redirect the browser to a new page.

## Window Location

The `window.location` object can be written without the `window` prefix.

### Some Examples

- `window.location.href` returns the href (URL) of the current page.
- `window.location.hostname` returns the domain name of the web host.
- `window.location.pathname` returns the path and filename of the current page.
- `window.location.protocol` returns the web protocol used (http: or https:).
- `window.location.assign()` loads a new document.

---

## Window Location Href

The `window.location.href` property returns the URL of the current page.

### Example

Display the href (URL) of the current page:

```javascript
document.getElementById("demo").innerHTML = 
"Page location is " + window.location.href;
```

**Result is:**

```
Page location is https://www.w3schools.com/js/js_window_location.asp
```

---

## Window Location Hostname

The `window.location.hostname` property returns the name of the internet host (of the current page).

### Example

Display the name of the host:

```javascript
document.getElementById("demo").innerHTML = 
"Page hostname is " + window.location.hostname;
```

**Result is:**

```
Page hostname is www.w3schools.com
```

---

## Window Location Pathname

The `window.location.pathname` property returns the pathname of the current page.

### Example

Display the path name of the current URL:

```javascript
document.getElementById("demo").innerHTML = 
"Page path is " + window.location.pathname;
```

**Result is:**

```
Page path is /js/js_window_location.asp
```

---

## Window Location Protocol

The `window.location.protocol` property returns the web protocol of the page.

### Example

Display the web protocol:

```javascript
document.getElementById("demo").innerHTML = 
"Page protocol is " + window.location.protocol;
```

**Result is:**

```
Page protocol is https:
```

---

## Window Location Port

The `window.location.port` property returns the number of the internet host port (of the current page).

### Example

Display the port number:

```javascript
document.getElementById("demo").innerHTML = 
"Port number is " + window.location.port;
```

**Result is:**

```
Port number is
```
*Note:* Most browsers will not display default port numbers (80 for http and 443 for https).

---

## Window Location Assign

The `window.location.assign()` method loads a new document.

### Example

Load a new document:

```html
<!DOCTYPE html>
<html>
<head>
<script>
function newDoc() {
  window.location.assign("https://www.w3schools.com")
}
</script>
</head>
<body>

<input type="button" value="Load new document" onclick="newDoc()">

</body>
</html>
```

