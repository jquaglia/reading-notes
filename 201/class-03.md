# Class 03

## Lists

### Ordered Lists

The ordered list is created with the `<ol></ol>` element. Each item iin the list is placed between an opening and closing `<li></li>` tag.

### Unordered Lists

The unordered list is created with the `<ul></ul>` element. Each item in the list is placed between an opening and closing `<li></li>` tag.

### Definition Lists

The definition list is created with the `<d1><d1>` element. Inside this you will find pairs of `<dt>` and `<dd>` tags. They are for the terms and definitions respectively.

### Nested Lists

You can put a second list inside of an original one. This looks like nested elements in html essentially.

## Boxes

### Box Dimensions

By default a box is sized just big enough to hold its contents. You can set your own dimensions using `height` or `width` properties. You can also limit these dimensions and set `min-width` or `max-height` and vice versa. This is helpful for versatile code that can be read on mobile or desktop. You don't want the text to appear too wide in a big browser window.

### Overflow

The overflow property tells the browser what to do if the content contained within a box is larger than the box itself. It can have one of two values.

- `hidden` Simply hides any extra content that does not fit in the box.

- `scroll` This adds a scrollbar to the box so that users can scroll to see the missing content.

### Border

Every box has a border. The border separates each box from one another.

### Margin

Margins sit outside the edge of the border. You can set the width of a margin to create a gap between the borders of two adjacent boxes.

### Padding

Padding is the space between the border of a box and any content contained within it. (all of this found around page 307)

### Border Width

The `border-width` property is used to control the width of a border. This can be given in pixels or `thin, medium, thick` You can control each side of the border separately.

### Border Style

This property can take the following values:

- solid

- dotted

- dashed

- double

- groove

- ridge

- inset

- outset

- hidden/none

These can all be changed per side of the box as well.

### Border Color

You can specify the color of a border using either RGB, hex codes, or CSS color names. These can all be changed per side as well.

### Border Shorthand

The `border` property can be used to specify the `width, style`, and `color` of a border at the same time. In that order.

### Padding Property

The `padding` property allows you to specify how much space should appear between the content of an element and its border.

### Margin Property

The margin property controls the gap between boxes. It's value is normally given with pixels although you may use percentages or ems. You can center content by setting left and right margins to auto. `(top, right, bottom, left)`

### Display

The `display` property allows you to change an inline element into a box element and vice versa. You can also make an `inline-block` or change it to `display: none;` which will hide the element as if its not on the page.

### Visibility

The `visibility` property allows you to hide boxes from users but it leaves a space where the element would have been. `(hidden, visible)`

### Box

Boxes can be made to have `box-shadow` as well as `border-radius`.

## Arrays

An array is a special type of variable. It doesn't just store one value; it stores a list of values. It is done like this:

```javascript
var colors;
colors = ['white', 'black', 'custom'];

var el = document.getElementById('colors');
el.textContent = colors[0];
```

or

```javascript
var colors = new Array(
    'white',
    'black',
    'custom'
);

var el = document.getElementById('colors');
el.textContent = colors[0];
```

Values in an array are accessed as if they are in a numbered list. It is important to know that the numbering of this list starts at zero.

## Decisions and Loops

If... else statements allow you to run one set of code if a condition is true, and another if it is false.

Switch statements allow you to compare a value against possible outcomes (and also provides a default option if none match).

Data types can be coerced from one type to another.

All values evaluate to either truthy or falsy.

There are three types of loop: for, while, and do...while. each repeats a set of statements.

### Switch Statements

A switch statment starts with a variable called the switch value. Each case indicates a possible value for this variable and the code that should run if the variable matches that value. If a match is found, that code is run; then the __break__ statement stops the rest of the __switch__ from running. (providing better performance than multiple if statements.)

### Type Coercion and Weak Typing

If you use a data type JS did not expect, it tries to make sense of the operation rather than report an error. For example a string `"1"` could be converted to a number in the following expression: `("1" > 0)` This is said to be weak typing because the data type for a value can change.

### Truthy and Falsy

Due to type coercion, every value in JS can be treated as if it were true or false; and this has some interesting side effects. (page 167)

### Short Circuit Values

Logical operators are processed left to right. They short-circuit (stop) as soon as they have a result - but they return the value that stopped the processing (not necessarily true or false).

### Loops

#### For Loops

For loops are if you need to run a loop of code for a specific number of times.

#### while Loops

While loops are for if you do not know how many times the code should run

#### do while

Do while loops are very similar to while loops but will run the statements inside the curly braces at least once, even if the condition evaluates to false.

```javascript
for (let i = 0; i < 10; i++) {
    document.write(i);
}
```

### Loop counters

#### Initialization

`var i = 0;` Create a variable and set it to 0. this variable is commonly called i and it acts as the counter

#### Condition

`i < 10;` The loop should continue to run until the counter reaches a specified number.

#### Update

`i++` Every time the loop has run the statements in the curly braces, it adds one to the counter.

[back to README](README.md)
