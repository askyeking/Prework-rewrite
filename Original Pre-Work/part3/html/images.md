## Images
To display images in your HTML documents you must use an `<img>` element. `<img>` tags take a `src` attribute that references the location of the image. You can link to images stored locally on your system, or images on the web.

### External image
By passing the url location of an image as the `src` property your HTML document will display the image on the page.

```html
<img src="https://pbs.twimg.com/profile_images/720847195860127744/K4Ld3JCd.jpg" />
```

### Local image
You can also path to your image using the relative location of the image from your `.html` document.

```html
<img src="../images/sd_logo.jpg" />
```

The file structure in this example would look something like this:
```bash
MySite
├── images
│   ├── sd_logo.jpg
│   ├── smiley_face.jpg
│   └── ...
└── html
    └── index.html
```

### Image links
If you want to create an image that is a link to another page you can nest a `<img>` tag inside of a `<a>` tag that we discussed earlier.

```html
<a href="http//www.skilldistillery.com">
  <img src="../../images/sd_logo.jpg" />
</a>
```

> ### ![Logo](http://skilldistillery.com/downloads/sd_logo.jpg) Skill Drill
> * ***NOTE:*** This drill continues the work you started in the previous hands on and will build upon those files.
>
> 0. Open the `index.html` document in your `SDPre/Blog` directory.
> 1. Find an image that you like and save the url.
> 2. In your html document create an external image link to display it.
> 3. From finder, right click (2 finger click ***or*** ctrl + click) on the `index.html`, select 'Open With' and click on your favorite browser (we recommend Chrome).
> 4. Take a look at the updates you have made to the page.

<hr>

[Prev](links.md) | [Up](README.md) | [Next](tables.md)

