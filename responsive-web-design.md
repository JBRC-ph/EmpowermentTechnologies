# Responsive Web Design

To follow the examples here, fork or clone this project: https://github.com/JBRC-ph/responsive-design-example

### Set the viewport in your HTML

```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Set the image to resize based on browser width

Add to your CSS:

```
section.hero img {
	width: 100%;
	height: auto;
}
```

If you don't want the image to be resized beyond its original size, use `max-width` instead of `width`:

```
section.hero img {
	max-width: 100%;
	height: auto;
}
```

To center the image, add the `display: block` and `margin: auto` properties:

```
section.hero img {
    max-width: 100%;
    height: auto;
    display: block;
    margin: auto;
}
```

### Add styles based on the screen size using media queries

Example: we want to hide the two `<img class="optional-pic">` images when the screen size is less than 500 pixels.

Add this to the CSS:

```
@media only screen and (max-width: 500px) {
    img.optional-pic {
        display: none;
    }
}
```

Another example: observe how [https://www.microsoft.com/en-ph/](https://www.microsoft.com/en-ph/) changes from a four-column layout to two-column and eventually single-column as you resize the browser screen.

_Note: media queries check the browser size, not the actual screen size._
