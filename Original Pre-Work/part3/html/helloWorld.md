## HTML "Hello World"

### HTML Documents

An HTML _document_ is a file ending with a `.html` extension which contains _elements_ formatted in a way that can be understood by Web Browsers. Your web browser (be it Google Chrome, Safari, Edge etc) contains something called a 'layout engine' which can process HTML and 'render' it in a formatted, human readable way.

As an example, the following is an extremely simple HTML document :

```html
<!DOCTYPE html>
<html>
  <head>
  </head>
  <body>
    <h1>Hello World</h1>
  </body>
</html>
```

A browser will 'render' this document as :

![Hello World](images/htmlHelloWorldEx.png)

Notice that the browser didn't display the _elements_ (`<html>`, `<head>`, `<body>`, `<h1>`). Those inform the browser how to render information and what it should look like.

<hr>

### Understanding HTML Elements
An HTML _element_, sometimes referred to as a _tag_, is defined by some number of characters contained within an opening and closing angle bracket.

Many HTML _elements_ have _closing tags_, these are _elements_ preceded by a forward slash (`</h1>`). A _closing tag_ concludes the formatting that was begun by the opening element. Thus, `<h1>Hello</h1>World` will only result in the word "Hello" being formatted as a header.

![Hello World](images/htmlHelloEx2.png)

Let's take a deeper look at the basic HTML document from earlier:

```html
<!DOCTYPE html>
<html>
  <head>
  </head>
  <body>
    <h1>Hello World</h1>
  </body>
</html>
```

* The `<!DOCTYPE html>` _element_ is a declaration that tells the browser rending our HTML that the text that follows is an HTML document. The `html` following `DOCTYPE` specifically tells the browser that the document is _HTML5_.

* `<html></html>` simply indicates that everything enclosed within it is HTML code.

* The `<head></head>` _elements_ denote content that will not appear on our web page, but may contain additional resources, such as links to _Cascading Style Sheet_ or JavaScript files.

* `<body></body>` _tags_ indicate that anything contained within them should be shown in the browser window and displayed to the user.

* Finally, the `<h1></h1>` is a top level header, as seen in the "Hello World" example above. There are lesser sub-headers available in html as well: `<h2>`,`<h3>`,`<h4>` ... These format similarly as `<h1>`, but result in smaller text.

<hr>

> ### ![Logo](http://skilldistillery.com/downloads/sd_logo.jpg) Skill Drill
> Over the next course of the next several pages these "Skill Drill" exercises will help you construct an HTML page and gain experience with a variety of HTML elements. In this first hands on, we will follow convention and create a "Hello World". The objective is to familiarize you with HTML basics so that you have a foundation from which you can build a basic blog (later).
>
> 0. Create a new directory (folder) in your `SDPre` directory named "Blog"
>    * inside of blog make a file named `index.html`
> 1. In `index.html`, create an HTML document.
> 2. Within the `<body></body>` add a header (`<h1>`) with the text `Hello World!`.
> 3. From finder, right click (2 finger click ***or*** ctrl + click) on the `index.html`, select 'Open With' and click on your favorite browser (we recommend Chrome).
> 4. Bask in the glory that is your 'Hello World!' HTML page.

<hr>

[Prev](README.md) | [Up](README.md) | [Next](basicFormatting.md)

