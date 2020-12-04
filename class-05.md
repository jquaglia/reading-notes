# Class 05

## Images

- The `<img><img>` element is used to add images to a web page.

- You must always specify an src attribute to indicate the source of an image and an alt attribute to describe the content of an image.

- You should save images at the size you will be using them on the web page and in the appropriate format.

### Three rules for creating images

1. save images in the right format

1. save images at the right size

1. measure images in pixels

### Image Formats

- Photographs are best saved as JPEGs; illustrations or logos that use flat colors are better saved as GIFs.

- Where an image is placed in the code will affect how it is displayed. It is a block element.

- Image format should be JPEG for best results with colorful images. (photos)

-Image format should be GIF or PNG for images with few colors or large areas of the same color.

### Image Dimensions

-The images you use on your website should be saved at the same width and height that you want them to appear on the page.

### Figure and Figure Caption

HTML5 has introduced a new `<figure></figure>` element to contain images and their caption so that the two are associated. The `<ficaption></figcaption>` element has been added in order to allow web page authors to add a caption to an image.

## Color

- The `color` property allows you to specify the color of text inside an element.

- The `background-color` property does just what it says for each box element.

- Every color on a computer screen is made by mixing amounts of red, green, and blue. To find the color you want, you can use a color picker.

- color not only brings you site to life but also helps convey the mood and evokes reactions.

- There are three ways to specify colors in CSS; RGB values, hex codes, and color names.

- color pickers can help you find the color you want.

- It is important to ensure that there is enough contrast between text and the background color (otherwise people will not be able to read your content).

- CSS3 has introduced an extra value for RGB colors to indicate Opacity. It is known as RGBA.

- CSS3 also allows you to specify colors as HSL calues with an optional opacity value. It is known as HSLA.

## Text

### Typeface Terminology

- Serif Fonts have extra details on the ends of the main strokes of the letters. These details are known as serifs.

- Sans-Serif fonts have straight ends to letters, and therefore have a much cleaner design.

- Monospace. Every letter in a monospace (or fixed-width) font is the same width.

### Specifying Typefaces

The `font-family` property allows you to specify the typeface that should be used for any text inside the elements to which a CSS rule applies. for example:

```css
p{
font-family: Georgia, Times, serif;
font-size: 12px;
}
h1{
  font-size: 200%;
}
h2{
  font-size: 1.3em;
}
```

Many details about sizing on page 275 in the book.

- There are properties to control the choice of font, size, weight, style, and spacing.

- There is a limited choice of fonts that you can assume most peopel will have installed.

- If you want to use a wider range of typefaces there are several options, but you need to have the right license to use them.

- You can control the space between lines of text, individual letters, and words. Text can also be aligned to the left, right, center, or justified. It can also be indented.

- you can use pseudo-classes to change the style of an element when a user hovers over or clicks on text, or when they have visited a link.(or when it is active)
