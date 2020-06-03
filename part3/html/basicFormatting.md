## Basic Formatting with HTML

HTML's formatting is not dissimilar from what is available in text applications like Word or Pages. The key difference is that instead of using a _Graphical User Interface (GUI)_ like one of those applications, you are writing the code to format the text content yourself.

Let's look at some of the basic text formatting available in HTML.

```html
<!DOCTYPE html>
<html>
  <head>
  	<title>Example</title>
  </head>
  <body>
    <h1>Page Header</h1>
    <p>This is the <em>first</em> <strong>paragraph</strong> on the page.</p>
    <p>This is the <em>second</em> <strong>paragraph</strong> on the page.</p>
    <p><strong><em>This is both bold and italics</em></strong></p>
  </body>
</html>
```

Which renders as:

![Formatting Example](images/htmlTextFormattingEx.png)

As you can see, each of these new _elements_ has added additional formatting to the text they surround. Let's look at each of them.

### `<p></p>`

  * The 'paragraph' tag automatically adds spacing around the text it contains, seperating it from other content, much like a paragraph stands removed from other paragraphs in a text document.

### `<em></em>`

  * The 'emphasis' tag formats text as italics.

### `<strong></strong>`

  * The 'strong' tag formats text as bold.

### `<title></title>`

  * The pair of `<title>` elements in the head are not displaying the word 'Example' in the body of the web page. Instead, the `<title>` tag is responsible for displaying the title of the page in the browser tab above:

![Title](images/htmlTitleEx.png)

<hr>

> ### ![Logo](http://skilldistillery.com/downloads/sd_logo.jpg) Skill Drill
> * ***NOTE:*** This drill continues the work you started in the previous hands on and will build upon those files.
>
> 0. Open the `index.html` document in your `SDPre/Blog` directory.
> 1. In the `<head>` of the document add a `<title>Hello World</title>` element.
> 2. Make the text `Hello World!` italic.
> 3. Beneth the `<h1>` element you created in the [hello world drill](./helloWorld.md) add a `<p>` describing your experience with HTML.
> 4. Make the text inside of your `<p>` tag bold
> 4. From finder, right click (2 finger click ***or*** ctrl + click) on the `index.html`, select 'Open With' and click on your favorite browser (we recommend Chrome).
> 5. Take a look at the updates you have made to the page.

<hr>

[Prev](helloWorld.md) | [Up](README.md) | [Next](lists.md)

