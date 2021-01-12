# Class 1

## Responsive Web Design

### Overview

Responsive web design is the practice of building a website suitable to work on every device and every screen size, no matter how large or small, mobile or desktop. It is focused around providing an intuitive and gratifying experience for everyone. The term was coined and developed by Ethan Marcotte.

### Responsive vs. Adaptive vs. Mobile

- Responsive means to react quickly and positively to any change.

- Adaptive means to be easily Modified for a new purpose or situation. (responsive and adaptive are closely related)

- Responsive design websites continually and fluidly change based on different factors such as viewport width.

- Adaptive websites are built to a group of preset factors.

- A combination of the two is ideal.

- Mobile means to build a separate website commonly on a new domain soley for mobile users.

- Not ideal because you have to work with a new code base and browser sniffing. (does have its uses though)

The most popular technique lies within responsive design, favoring design that dynamically adapts to different browsers and viewports. This solution has the benefits of being responsive, adaptive, and mobile friendly.

### Flexible Layouts

- Flexible layouts is the practice of building the layout of a website with a flexible grid, capable of dynamically resizing to any width.

- Flexible grids are built using relative length units such as percentages or 'em' units.

- These lengths are used to declare common grid property values such as width, margin, or padding.

- Flexible layouts do not advocat the use of fixed measurements units, such as pixels or inches.

- Ethan pointed out an easy formula to help identify proportions of a flexible layout using relative values.

```javascript
target ÷ context = result
```

#### Flexible Grid

Using the formula, a margin of `10px` in a div with a width of `538px` becomes:

```css
margin: 1.858736059%; /*  10px ÷ 538px = .018587361 */
```

- Taking this layout concept and applying it to a grid will create a completely dynamic website.

- This approach alone isn't enough sometimes. At times the width of a viewport may become so small that even scaling the layout proportionally will create columns too small to see.

- This can be helped with media queries.

### Media Queries

- built as an extension to media types commonly found when targeting and including styles.

- provide the ability to specify different styles for individual browser and device circumstances. (e.g. width or device orientation)

#### Initializing Media Queries

- there are a couple different ways to use media queries

  - `@media` rule insde an existing style sheet

  - importing a new style sheet using the `@import` rule

  - or by linking to a separate style sheet from within the html document.

- Generally speaking, it is recommended to use the `@media` rule inside of an existing style sheet to avoid any additional HTTP requests.

HTML

```html
<!-- Separate CSS File -->
<link href="styles.css" rel="stylesheet" media="all and (max-width: 1024px)">
```

CSS

```css
/* @media Rule */
@media all and (max-width: 1024px) {...}

/* @import Rule */
@import url(styles.css) all and (max-width: 1024px) {...}
```

Each media type query may include a media type followed by one or more expressions. Common media types include:

- `all`

- `screen`

- `print`

- `tv`

- `braille`

HTML5 includes new media types even including `3d-glasses`. The default media type is `screen`. The media query expression that follows may include different features and values that equate to `true` or `false`, determining if the rules are applied.

#### Logical Operators in Media Queries

There are three different logical operators available for use within media queries:

- `and`

- `not`

- `only`

Multiple individual media queries can be comma separated, acting as an unspoken `or` operator.

#### Media Features in Media Queries

- `Height` and `Width` Media Features

- `Orientation` Media Feature

- `Aspect Ratio` Media Feature

- `Pixel Ratio` Media Feature

- `Resolution` Media Feature

- Other media Features include identifying available output colors with use of the `color`, `color-index`, and `monochrome` features, identifying bitmap devices with the `grid` feature, and identifying the scanning process of a television with the `scan` feature. These features are less common but equally as helpful when needed.

### Mobile First

One popular technique with using media queries is called _mobile first_. This approach includes using styles targeted at smaller viewports as the default styles for a website, then use media queries to add styles as the viewport grows.

The operating belief behind this is that a user on a mobile device, shouldn't have to load in the styles for a desktop just to have them overwritten later. This is a waste of bandwidth.

### Viewport

Apple invented the `viewport` meta tag to help mobile devices identify the viewport size, scale, and resolution of a website.

#### Viewport Height and Width

```html
<meta name="viewport" content="width=device-width">
```

#### Viewport Scale

```html
<meta name="viewport" content="initial-scale=2">
```

```html
<meta name="viewport" content="user-scalable=yes">
```

#### Viewport Resolution

```html
<meta name="viewport" content="target-densitydpi=device-dpi">
```

#### Combining Viewport Values

The `viewport` meta tag will accept individual values as well as multiple values, allowing multiple viewport properties to be set at once. Setting multiple values requires comma separating them within the `content` attribute value. One of the recommended viewport values is outlined below, using both the `width` and `initial-scale` properties.

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

### Flexible Media

The final important aspect to responsive web design involves flexible media. As viewports change, media doesn't always follow suit. A quick way to make media scalable is by using the `max-width` property with a value of `100%`.

#### Flexible Embedded Media

Specifically `iframes` do not work well with the `max-width` property. There is a work around for this.

- the embedded element needs to be absolutely positioned within a parent element.

- parent element needs to have a width of 100% so that it may scale based on the width of the viewport.

- parent element also needs to have a height of 0 to trigger the hasLayout mechanism within Internet Explorer.

- padding is then given to the bottom of the parent element, the value of which is set in the same aspect ratio of the video.

- This allows the height of the parent element to be proportionate to that of it’s width.

- If a video has an aspect ratio of 16:9, 9 divided by 16 equals .5625, thus requiring a bottom padding of 56.25%.

- Padding on the bottom and not the top is specifically used to prevent Internet Explorer 5.5 from breaking, and treating the parent element as an absolutely positioned element.

[back to README](README.md)
