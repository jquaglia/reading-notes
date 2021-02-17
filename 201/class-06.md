# Class 06

## What is an object

Objects group together a set of variables and functions to create a model of something yoy would recognize from the real world. In an object, variables and functions take on new names.

- If a variable is part of an object, it becomes a property.

- In an object, functions become known as methods.

- Properties and Methods have a name and a value. In an object, that nameis called a key.

- An object cannot have two keys with the same name.

- The value of a property can be a string, number, Boolean, array, or even another object.

-The value of a method is always a function.

```javascript
var hotel = {
  name: 'Quay',
  rooms: 40,
  booked: 25,
  checkAvailability: function() {
    return this.rooms - this. booked;
  }
}
```

The object is stored in a variable named hotel. Separate each key from its value with a colon. Separate each property and method with a comma. You can access the properties or methods of an object using dot notation. You can also access properties using square brackets. (page 103)

## Document Object Model

The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JS cna access and update the contents of a web page while it is in the browser window.

As a browser loads a web page, it creates a model of that page. The model is called a DOM tree, and it is stored in the browsers' memory. it consists of four main types of nodes.

### Document Node

The document node represents the entire page.It is the starting point for all visits to the DOM tree.

### Element Nodes

Element nodes are the same as HTML elements. These are how you see where you are/ what you want to find.

### Attribute Nodes

The opening tags of HTML elements can carry attributes and these are represented by attribute nodes in the DOM tree.

### Text Nodes

Once you have accessed an element node, you can then reach the text within that element. This is stored in its own text node.

Each node is an object with methods and properties. Scripts access and update this DOM tree (not the source HTML file) Any changes made to the DOM tree are reflected in the browser.

### Caching DOM Queries

Methods that find elemetns in the DOM tree are called DOM queries. When you need to work with an element more than once, you should use a variable to store the result of this query. When people talk about storing elements in variables, they are really storing the location of the elements within the DOM tree in a variable. The properties and methods of that element node work on the variable.

### Methods that select individual elements

`getElementById()` and `querySelector()` can both search an entire document and return individual elements. both use a similar syntax.

### Nodelists: DOM queries that return more than one element

When a DOm method can return more than one element, it returns a NodeList (even if it only finds one matching element.)

### Selecting an element from a nodelist

There are two ways to select and element from a NodeList: the `item()` method and array syntax. Both require the index number of the element you want. Array syntax is preferred over the `item()` method because it is faster. Before selecting a node from a NodeListm check that it contains nodes. If you repeatedly use the NodeList, store it in a variable.

### Repeating actions for an entire NodeList

When you have a NodeList, you can loop through each node in the collection and apply the same statements to each.

### traversing the DOM

When you have an element node, you can select another element in relation to it using these five properties. This is known as traversing the DOM. `parentNode`, `previousSibling`, `nextSibling`, `firstChild`, `lastChild`.

This can be hard because some browsres add a text node whenever they come across whitespace between elements.

### Adding or removing HTML content

There are two very different approaches to adding and removing content from a DOM tree: the `innerHTML` property and DOM manipulation.

### Attribute Nodesu

Once you have an element node, you can use other properties and methods on that element node to access and change its attributes.

### Summary

- The browser represents the page using a DOM tree

- DOM trees have four types of nodes: document nodes, element nodes, attribute nodes, text nodes.

- You can select element nodes by their id or class attributes, by tag name, or using CSS selector syntax.

- Whenever a DOM query can trturn more than one node, it will always return a NodeList.

- From an element node, you can access and update its content using properties such as `textContent` and `innerHTML` or using DOM manipulation techniques.

- An element node can contain multiple text nodes and child elements that are siblings of each other.

- In older browsers, implememntation of the DOM is inconsistent (and is popular reason for using jQuery)

- Browsers offer tools for viewing the DOM tree.

[back to README](README.md)
