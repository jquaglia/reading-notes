# Class 04

## Links

Links are created using the `<a></a>` element which has an attribute called href. The value of the href attribute is the page that you want people to go to when they click the link. When linking to pages in the same site, you can use the relative URL. This is akin to linking to the file of the page.

### Email Links

To create a mail link that starts up the user's email program and addresses an email to a specified email address, you use the `<a>` element. However this time the value of the hred attribute starts with `mailto:`

### Opening Links in a New Window

If you want a link to open in a new window, you can use the target attribute in the opening `<a>` tag. The value of this attribute should be blank.

## Layout

- `<div>` elements are often used as containing elements to group together sections of a page.

- Browsers display pages in normal flow unless you specify relative, absolute, or fixed positioning.

- The float property moves content to the left or right of the page and can be used to create multi-column layouts. (Floated items require a defined width.)

- Pages can be fixed width or liquid (stretchy) layouts.

- Designers keep pages within 960-1000 pixels wide, and indicate what the site is about within the top 600 pixels (to demonstrate its relevance without scrolling)

- Grids help create professional and flexible designs.

- CSS Frameworks provide rules for common tasks.

- You can include multiple CSS files in one page.

### Positioning Schemes

- Normal Flow

- Relative Positioning moves an element from the positioning it would be in normal flow, shifting it to the top, right, bottom, or left of where it would have been. This doesn't affect the positioning of other elements around it.

- Absolute Positioning moves the element in relation to its containing element. It is taken out of normal flow. Absolutely positioned elements movve as users scroll up and down the page.

- Fixed Positioning moves the element in relation to the browser window. These elements do not move when the user scrolls up or down.

- Floating Elements allows you to take that element out of normal flow and position it to the far left or right of a containing box. The floated element becomes a block which other content can flow.

## Functions, Methods, and Objects

### Functions

Functions let you group a series of statements together to perform a specific task. If different parts of a script repeat the same task, you can reuse the function (rather than repeating the same set of statements)

### Declaring a function

```javascript
function sayHello() {
    document.write('Hello!');
}
```

Having declared the function, you can then execute all of the statements between its curly braces with just one line of code. this is known as **calling the function** You can call the function as many times as you want in the same JS file.

```javascript
sayHello();
```

### Declaring functions that need information

Sometimes a function needs specific information to perform its task. in such cases, when you declare the function you give it **parameters**. inside the function, the parameters act like variables.

```javascript
function getArea(width, height) {
    return width * height;
}
```

When you call a function that has parameters, you specify the values it should use in the paranthesis that follow its name. The values are called **arguments** and they can be provided as values or variables.
