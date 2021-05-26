#  HTML Images; CSS Color & Text

# HTML Images:
The HTML `<img>` tag is used to embed an image in a web page.

Images are not technically inserted into a web page; images are linked to web pages. The `<img>` tag creates a holding space for the referenced image.

The `<img>` tag is empty, it contains attributes only, and does not have a closing tag.

The `<img>` tag has two required attributes:

- src - Specifies the path to the image
- alt - Specifies an alternate text for the image

> `<img src="url" alt="alternatetext">`

**Image Filters:** The CSS filter property adds visual effects (like blur and saturation) to an element.
**Hover Effects:** You can also add special effects on hover/mouse-over.
> `<img src="image.jpg" alt="Einstein" class="w3-hover-sepia">`
**The src Attribute** The required src attribute specifies the path (URL) to the image.
> `<img src="img_welcome.jpg" alt="Welcome">`
**The alt Attribute:** The required alt attribute provides an alternate text for an image, if the user for some reason cannot view it (because of slow connection, an error in the src attribute, or if the user uses a screen reader)
> `<img src="welcom-hello.jpg" alt="hello">`

# CSS Color & Text:
## CSS Color
The color property is used to set the color of the text. The color is specified by:

-  color name "red"
-  HEX value "#ff0054"
-  RGB value  "rgb(255,0,0)"

Look at CSS Color Values for a complete list of possible color values. The default text color for a page is defined in the body selector.
```css
body {
  color: red;
}

h1 {
  color: #0054ff;
}
```

## CSS Text

CSS has a lot of properties for formatting text.

- The `text-align` property is used to set the horizontal alignment of a text.
```css
div {
  text-align: justify;
}
```
- The `direction` and unicode-bidi properties can be used to change the text direction of an element:
```css
p {
  direction: rtl;
  unicode-bidi: bidi-override;
}
```
- The `text-decoration` property is used to set or remove decorations from text.
```css
h1 {
  text-decoration: overline;
}

h2 {
  text-decoration: line-through;
}

h3 {
  text-decoration: underline;
}
```
- The `text-transform` property is used to specify uppercase and lowercase letters in a text.
```css
div.uppercase {
  text-transform: uppercase;
}

div.lowercase {
  text-transform: lowercase;
}
```

- The `text-indent` property is used to specify the indentation of the first line of a text:
```css
p {
  text-indent: 15%;
}
```
- The `line-height` property is used to specify the space between lines:
```css
p.hightText {
  line-height: 1.8;
}
```
and more.




