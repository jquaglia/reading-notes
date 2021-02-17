# Class 01

## Structure

Websites use similar structure to Newspapers and other types of paper media. HTML describes the structure of pages. HTML uses elements to describe the structure of pages.

-Tags act like containers for each element. Some elements have opening and closing tags while others have only the opening tag. `<h1>This is the header</h1>`

-Attributes tell us more about the elements. Attributes are found inside the tags of an element. `<p lang="en us">Paragraph in English</p>` Attributes require a name and a value. the value being "en us" in the example

### Specific Tags

- `<body></body>` Everything inside this element is show in the main browser window

- `<head></head>` The head element comes before the `<body>` tag. This contains info about the page that isn't shown on the main page.

- `<title></title>` The contents of the title page are shown in the top of the browser or on the tab. This element is found inside the `<head>` tag.

### Extra Markup

- `<!DOCTYPE html>` declares to the browser what type of page this will be (HTML5)

- `<!-- Comment goes here -->` this is how to add a comment to your code that will not be seen by the page.

- `<p id="pullquote"></p>` this is an id attribute. Every HTML element can carry an id attribute.

- `<p class="important"></p>` this is a class attribute. Every HTML element can also carry a class attribute but sometimes you want multiple elements to belong to a class.

- Block elements will always appear to start on a new line in the browser window.

- Inline elements will always appear to continue on the same line as their neighboring elements.

- `<div></div>` This allows you to group a set of elemens together in one block-level box.

- `<span></span>` This element acts like an inline equivalent of the `<div>` element.

- `<iframe></iframe>` (inline frame) This element is like a little window that has been cut into your page --in that window you can see a different page.

- `<meta>` This tag is inside the `<head>` and contains info about the page including a description, keywords, and robots. (These indicate whether a search engine should add this page to search results or not.)

### Escape Characters

There are some characters that are used in and reserved for HTML code. These characters cannot just be typed out for example to write left angle bracket type `&lt;` or `&#60;` &lt; Cheat sheet for this online/page 194.

## HTML Layout

Example layout can be found in the book on page 428.

### Headers and Footers

The `<header>` and `<footer>` tags are used at the top and bottom of a page, respectively. The header has the site name and main navigation while the footer has copyright info.

The `<nav>` tag is used for the navigation section of the site. This is where links to other pages on the site will be.

### Articles

The `<aritcle>` tag acts as a container for any section of a page that could stand alone. ie. blog, news article, forum post. There can be several article elements and they can be nested inside each other as well.

### Asides

The `<aside>` tag has two purposes depending on whether or not it is used inside or outside an article element.

#### Inside

When inside, it should contain info that is related to the article but not essential to the overall meaning.

#### Outside

When outside, it acts as a container for content that is related to the entire page.

### Sections

The `<section>` tag is used to group related content together. This is done using classes for each separate tag.

### Heading Groups

The purpose of the `<hgroup>` tag groups a set of one or more `<h1>` through `<h6>` tags together to be treated as a single heading.

### Figures

The `<figure>` tag is used to contain any content that is referenced from the main flow of an article. it is important the article still functions without this piece in it. A `<figcaption>` tag should also be used to provide context.

### Sectioning Elements

The `<div>` tag will be used when no other suitable element to group a set of elements.

## Process and Design

You can start off the process by thinking about what you want on your site and who you want to visit your site. Once you have figured that out you can make a site map. The site map allows you to plan the structure of a site. Once that is done you can make a wireframe as a rough guidline for each page. Design is about communication. Visual hierarchy helps visitors understand what you are trying to tell them. You can use size, color, and style to differentiate between pieces of information. You can use grouping and similarity to help simplify the information you present.

## The ABC of Programming

### A) What is a script and how do I create one?

Scripts are made up of instructions a computer can follow step-by-step. A browser may use different parts of the script depending on how the user interacts with the web page. Scripts can run different sections of the code in response to the situation around them.

#### Writing a Script

Start with the big picture of what you want to achieve, and break it down into smaller steps.

1. Define the goal

1. Design the script

1. Code each step

#### From steps to code

- **Vocabulary** are the words that the computer understands

- **Syntax** is how you put those words together to create instructions the computer can follow

- Often scripts will need to perform different tasks in different situations. You can use flow charts to work out how the tasks fit together. Flowcharts show the paths between each step.

### B) How do computers fit into the world around them?

- Computers create models of the world using data.

- The models use objects to represent physical things. Objects can have: properties that tell us about the object; methods that perform tasks using the properties of that object; events which are triggered when a user interacts with the computer.

- Programmers can write code to say "When this event occurs, run that code."

- Web browsers use HTML markup to create a model of the web page. Each element creates its own node (which is a kinf of object).

- To make web pages interactive, you write code that uses the browser's model of the web page.

### C) How do I write a script for a web page?

- It is best to keep JavaScript code in its own JS file. JS files are text files (like HTML pages and CSS style sheets), but they have the .js extension.

- The HTML `<script>` element is used in HTML pages to tell the browser to load the JS file (rather like the `<link>` element can be used to load a CSS file).

- If you view the source code of the page in the browser, the JS will not have change the HTML, bvecuase the script works with the model of the web page that the browser has created.

`document.write('Good afternoon!');` "document" is the object which represents the entire web page. All web browsers implement this object. The "." is the member operator. The _document_ object has several methods and properties. They are known **members** of that object. You can access thee members by using a dot in between the object name and the member you want to access. `write('Good afternoon!');` is the method. the _write_ method of the _document_ object allows new content to be written into the page where the `<script>` element sits. `'Good afternoon!'` are the parameters. Whenever a method requires some information in order to work, the data is given inside the parenthesis.

[Back to README](../README.md)
