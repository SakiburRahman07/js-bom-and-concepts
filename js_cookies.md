
# JavaScript Cookies

Cookies allow you to store user information in web pages. With JavaScript, you can create, read, and delete cookies to manage user data and personalize user experiences.

## What are Cookies?

- Cookies are small text files stored on the user's computer.
- They help web servers remember information about users between sessions.
- Cookies are saved in `name=value` pairs, such as `username=John Doe`.

## Creating Cookies with JavaScript

With JavaScript, you can create a cookie using the `document.cookie` property:

```javascript
document.cookie = "username=John Doe";
```

### Adding an Expiry Date

By default, cookies are deleted when the browser is closed. You can add an expiry date to keep cookies longer:

```javascript
document.cookie = "username=John Doe; expires=Thu, 18 Dec 2025 12:00:00 UTC";
```

### Specifying a Path

Cookies can be scoped to a specific path. By default, they belong to the current page:

```javascript
document.cookie = "username=John Doe; expires=Thu, 18 Dec 2025 12:00:00 UTC; path=/";
```

## Reading a Cookie with JavaScript

Cookies can be read by accessing `document.cookie`:

```javascript
let x = document.cookie;
```

## Changing a Cookie

To change a cookie, simply overwrite it:

```javascript
document.cookie = "username=John Smith; expires=Thu, 18 Dec 2025 12:00:00 UTC; path=/";
```

## Deleting a Cookie

To delete a cookie, set its `expires` parameter to a past date:

```javascript
document.cookie = "username=; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/;";
```

## The Cookie String Format

When accessing `document.cookie`, all cookies are returned in a single string in the format `cookie1=value; cookie2=value; ...`. Each cookie is separated by a semicolon.

## JavaScript Cookie Example

The following example demonstrates setting, getting, and checking a cookie:

### Setting a Cookie

This function stores the name of a visitor in a cookie:

```javascript
function setCookie(cname, cvalue, exdays) {
  const d = new Date();
  d.setTime(d.getTime() + (exdays * 24 * 60 * 60 * 1000));
  let expires = "expires=" + d.toUTCString();
  document.cookie = cname + "=" + cvalue + ";" + expires + ";path=/";
}
```

### Getting a Cookie

This function returns the value of a specified cookie:

```javascript
function getCookie(cname) {
  let name = cname + "=";
  let decodedCookie = decodeURIComponent(document.cookie);
  let ca = decodedCookie.split(';');
  for (let i = 0; i < ca.length; i++) {
    let c = ca[i].trim();
    if (c.indexOf(name) == 0) return c.substring(name.length, c.length);
  }
  return "";
}
```

### Checking a Cookie

This function checks if a cookie is set. If set, it displays a greeting; otherwise, it prompts the user for their name and sets a new cookie:

```javascript
function checkCookie() {
  let username = getCookie("username");
  if (username != "") {
    alert("Welcome again " + username);
  } else {
    username = prompt("Please enter your name:", "");
    if (username != "" && username != null) {
      setCookie("username", username, 365);
    }
  }
}
```

## Putting It All Together

Here’s a complete example:

```javascript
function setCookie(cname, cvalue, exdays) {
  const d = new Date();
  d.setTime(d.getTime() + (exdays * 24 * 60 * 60 * 1000));
  let expires = "expires=" + d.toUTCString();
  document.cookie = cname + "=" + cvalue + ";" + expires + ";path=/";
}

function getCookie(cname) {
  let name = cname + "=";
  let ca = document.cookie.split(';');
  for (let i = 0; i < ca.length; i++) {
    let c = ca[i].trim();
    if (c.indexOf(name) == 0) return c.substring(name.length, c.length);
  }
  return "";
}

function checkCookie() {
  let user = getCookie("username");
  if (user != "") {
    alert("Welcome again " + user);
  } else {
    user = prompt("Please enter your name:", "");
    if (user != "" && user != null) {
      setCookie("username", user, 365);
    }
  }
}
```

This example runs the `checkCookie()` function when the page loads, prompting the user if the "username" cookie is not set and welcoming them if it is.

---

**Note**: Cookies won't work if local cookies support is disabled in the browser.
