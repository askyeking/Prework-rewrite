## Introduction to Cascading Style Sheets (CSS)

### Overview

Cascading Style Sheets (CSS) allow developers to modify the appearance of HTML.

HTML creates the structure of how content will appear in the browser, but has limited flexibility around what it will look like.

CSS allows us to do things like change the color of text, change the position of content on a page, etc etc. Without CSS, web pages would look pretty boring.

<hr>


### Where to write CSS?

* CSS should be written in `.css` files, not inside of a `.html` file.

* Create a file like `app.css`, and then source it in your `.html` file using a link in the `<head>` element:

```html
<head>
  <link rel="stylesheet" href="app.css" />
</head>
```

  * the `link` element's attributes let the web browser know that the resource is a *stylesheet*, and that it should find a file named `app.css`.

  * ***NOTE***: In the above example, `app.css` would need to be in the same directory as your html file, like so:
  ```bash
  Blog
  ├── home.html
  └── app.css
  ```
<hr>

### CSS Selectors
* *CSS Selectors* are element names or class attribute names in HTML that CSS will target to modify.

* Consider the following HTML:

```HTML
<!DOCTYPE html>
<html>
  <head>
    <title>Blog</title>
    <link rel="stylesheet" href="app.css">
  </head>
  <body>

    <h1>Header Text</h1>

    <div class="red">
        Important message
    </div>

  </body>
</html>
```

* Here is an example of how we could style the content within the `<body></body>` element with CSS:

```CSS
/*
  Select the h1 element, make its text
  white and the background behind it green
*/
h1 {
  color : white;
  background : green;
}

/*
  Select any HTML element with the class
  attribute "red", and make its text red
*/
.red {
  color : red;
}
```

* When the html file above loads, it will load the `app.css` file.

* The `app.css` file selects the HTML elements and modifies their styles as indicated.

* The result is this:

![Example Result](images/css-ex.png)

### More Selectors & CSS Properties

This W3 Schools Tutorial has runnable code examples, as well as details additional CSS properties and selectors. Explore it for more styling options.

* https://www.w3schools.com/css/css_syntax.asp

<hr>

[Up](README.md) | [Next](startBlogging.md)

