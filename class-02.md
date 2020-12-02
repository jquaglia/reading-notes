# Class 02

## Text

HTML Elements are used to describe the structure of the page. They also provide sematnic information (e.g. where emphasis should be placed, the difinition of any acronyms used, when given text is a quotation)

### Headings

HTML has 6 levels of headings. `<h1></h1>.....<h6></h6>` The `<h1>` tag is used for main headings and the others are for smaller and smaller sub-headings.

### Paragraphs

`<p></p>` By default each paragraph will be shown on a new line with some space between.

### Bold and Italic

By enclosing words in the `<b></b>` tags, we can make words **bold**. We can also make words *italic* by enclosing them in the `<i></i>` tags.

### Superscript and Subscript

The `<sup></sup>` element is used to contain characters that should be superscript such as the suffixes of dates or mathematical concepts like raising a number to a power such as `2<sup>2</sup>`. The `<sub></sub>` element is used to contain characters that should be subscript. It is commonly used with foot notes or chemical formulas such as `H<sub>2</sub>O`.

### White Space

White space is added in to code to make it easier to read. The browser treats all extra white space as only 1 space. This is known as white space collapsing.

### Line Breaks and Horizontal Rules

`<br />` inserts a line break into the page. `<hr />` inserts a break with a horizontal line. Perfect for using when changing themes completely on a page. (Both of these are empty elements which only have 1 tag)

### Strong and Emphasis

The use of the `<strong></strong>` element indicates that its content has strong importance. By default, browsers will show the contents in bold. The `<em></em>` element indicates emphasis that subtly changes the meaning of a sentence. By default, browsers will show the contents in italic.

### Quotations

There are two elements used for marking up quotations: `<blockquote></blockquote>` is used for longer quotes that take up an entire paragraph. Browsers tend to inden the contents of this element. The `<q></q>` element is used for shorter quotes that sit within a paragraph. Both elements may use the *cite attribute* to indicate where the quote is form. Its value should be a URL with more info about the source of the quote.

### Abbreviations and Acronyms

If you use an abbreviation or acronym, then the `<abbr></abbr>` element can be used. The title *attribute* can be used to spell out the full form of both.

### Citations and Definitions

When referencing a piece of work such as a book, the `<cite></cite>` element can be used. The first time you explain some new terminology in a document, it is known as the defining instance of it. The `<dfn></dfn>` element is used to indicate this. (some browsers show this in italics, some do not.)

### Author Details

The `<address></address>` element contains contact info for the author of the page.

### Changes to Content

`<ins></ins>` shows content that has been inserted(usually underlined) `<del></del>` shows content that has been removed(~~usually with a line through it~~) `<s></s>` element indicates something that is no longer relevant(but that should not be deleted) This will usually show with a line through the center.

## Introducing CSS

CSS allows you to create rules that control the way that each individual box is presented.

### Some Example styles include

#### Boxes

- width and height

- borders (color, width, style)

- background colors and images

- position in browser window

#### Text style

- typeface

- size

- color

- italics, bold, uppercase

- lowercase, small-caps

### CSS Associates rules with HTML Elements

 CSS rule contains two parts: a selector and a declaration.

`p{'font-family': Arial;}` The `p` is the selector while the rest is the declaration.

### CSS Properties affect how elements are displayed

CSS declarations sit insde curly brackets and are also made of two parts: a property and a value, separated by a colon. you can use several properties in one declaration, separated by a semi-colon.

`h1, h2, h3 {
    font-family: Arial;
    color: yellow;
}` In this case, the `font-family` and `color` are the properties, while the things that specify what they are, are the values.

### CSS can be used internally or externally

Css can be used internally right in the html code on a page using the `<style>` tag, or it can be used on an external style sheet that the html page links to.

### CSS Selectors

Many common selectors in CSS are as follows below. They determine what the style applies to.

- `* {}` universal selector targets all elements

- `h1, h2, h3 {}` targets heading tags

- `.note {}` targets and element whose class attribute has a value of note

- `p.note {}` targets only `<p>` elements with class attribute of note

- `#introduction {}` targets element whose id attribute has a value of introduction

- `li>a {}` targets any `<a>` elements that are children of an `<li>` element but not other `<a>` elements on the page

- `p a {}` targets any `<a>` elements that are insdide a `<p>` element

- `h1+p {}` targets first `<p>` element after any `<h1>` element but not other `<p>` elements

- `h1~p {}` If you had any two `<p>` elements that are siblings of an `<h1>` element, this rule would apply to both

### CSS Importance and Inheritance

#### CSS Importance

The closest and most specific rule that applies is the one that takes presedence. You can add `!` after any property value to declare that rule to be important.

#### CSS Inheritance

You can specify the font-family or color on the `<body>` element, they will apply to most child elements. This does not work with background-color as that would get messy. However, you can make things inherit by using `inherit` in the value.

## Basic JavaScript Instructions

A script is a series of instructions that a computer can follow one by one. Each individual instruction is known as a statement. Statements end with a semicolon.

## Variables

`var quantity;` The var is the variable keyword (use `let` more now) and the quantity is the variable name. `quantity = 3;`  "`=`" is the assignment operator, 3 is the variable value. It is possible to use a variable to store a number or string for later use.

### Data Types

1. Numeric data type (0.75)

1. String datat type ('Hi, Ivy!')

1. Boolean data type (true)

Variables can store all of these types of data.

### Rules for naming a Variable

1. the name must begin with a letter, dollar sign, or an underscore. It must not start with a number

1. the name can contain letters, numbers, dollar sign or an underscore. do not use a . or a -

1. you cannot use keywords or reserved words

1. all variables are case sensitive so _score_ and _Score_ would be different variables.

1. Use a name that describes what info the variable stores

1. if your variable name is made up of more than 1 word, use a capital letter for the first letter of every word after the first word ie `lastName`

### Arrays

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

### Operators

Expressions rely on things called **operators**; they allow programmers to create a single vallue from one or more values. (=,+,*,<,>)

#### Arithmetic Operators

JS contains the following mathematical operators which you can use with mumbers:

- `+` adds

- `-` subtracts

- `/` divides

- `*` multiplies

- `++` adds one to the current number

- `--` subtracts one from the current number

- `%` divides two values and returns the remainder

#### String operator

There is just one string operator: the `+` symbol. it is used to joing the strings on either side of it.

## Decisions and Loops

### Comparison Operators: Evaluating Conditions

`==` is equal to

`!=` is not equal to

`===` strict equals to

`!==` strict not equals to

`>` greater than

`<` less than

`>=` greater than or equal to

`<=` less than or equal to

#### Structuring Comparison Operators

```javascript
(score >= pass)
```

#### Using expressions with comparison operators

```javascript
((score1 + score2) > (highScore1 + highScore2))
```

The operand does not have to be a single value or variable.

### Logical Operators

`&&` logical and

`||` logical or

`!` logical not

```javascript
((5 < 2) && (2 >= 3))
```

Tests more than one condition to make sure both are true. both sides above are `false` and `false`

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

[back to README](README.md)
