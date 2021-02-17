# Class 7

## Tables

- The `<table></table>` element is used to add tables to a web page.

- A table is drawn out row by row. Each row is created with the `<tr>` element.

- Inside each row there are a number of cells represetned by the `<td>` element (or `<th>` if it is a header)

- You can make cells of a table span more than one row or column using the rowspan and colspan attributes.

- For long tables you can split the table into a `<thead>`, `<tbody>`, `<tfoot>`.

## Functions, Objects, Methods

### Creating an object

- The `new` keyword and the `object` constructor create a blank object. You can then add propertieds and methods to the object.

```javascript
var hotel = new Object();
hotel.name = 'Quay';
hotel.rooms = 40;
hotel.booked = 25;
hotel.checkAvailability = function() {
  return this.rooms - this.booked;
};
```

### Updating and object

- To update the value of properties, use dot notation or square brackets. They work on objects created using literal or constructor notation. To delete a property, use the `delete` keyword.

### Creating many objects: constructor notation

- Sometimes you will want several objects to represent similar things. Object constructors can use a function as a **template** for creating objects. First, create the template with the objects properties and methods.

```javascript
function Hotel(name, rooms, booked){
  hotel.name = name;
  hotel.rooms = rooms;
  hotel.booked = booked;
  hotel.checkAvailability = function() {
    return this.rooms - this.booked;
  };
}
```

- You create **instances** of the object using the constructor function. The **new** keyword followed by a call to the function creates a new object. The properties of each object are given as arguments to the function.

```javascript
var quayHotel = new Hotel('Quay', 40, 25);
var parkHotel = new Hotel('Park', 120, 77);
```

`this` (it is a keyword) The keyword **this** is commonly used inside funtions and objects. Where the function is declared alters what this means. It always refers to one object, usually the object in which the function operates.

### Arrays are objects

- Arrays are actually a special type of object. They hold a related set of key/value pairs (like all objects), but the key for each value is its index number.

### Arrays of objects and objects in arrays

- You can combine arrays and objects to create complex data structures: Arrays can store a series of objects (and remember their order). Objects can also hold arrays (as values of their properties).

### Three groups of built-in objects

1. Browser object model

1. Document object model

1. Global JavaScript objects

### The DOM

- The topmost object in the Document Object Model is the document object. It represents the web page loaded into the current browser window or tab. You meet its child objects in Chapter 5.

### Global Objects: String Object

- Whenever you have a value that is a string, you can use the properties and methods of the String object on that value. This example stores the phrase "Home sweeet home" in a variable.

`var saying = 'Home sweet home';`

`saying.length;` returns `16` as it counts all characters in the string.

### Data types revisited

In Javascript there are six data types:\
Five of them are described as simple (or primitive) data types.\
The sixth is the object (and is referred to as a complex data type)

1. String
1. Number
1. Boolean
1. Undefined
1. Null

### Global Objects: Number Object

- Whenever you have a value that is a number, you can use the methods and properties of the Number object on it.
  - `isNaN()`
  - `toFixed()`
  - `toPrecision()`
  - `toExponential()`

### Global Objects: Math Object

- The `Math` object has properties and methods for mathematical constants and functions.
  - `Math.PI` Returns pi
  - `Math.round()` rounds to nearest integer
  - `Math.sqrt(`_n_`)` returns square root of positive number
  - `Math.ceil()` rounds number up to nearest integer
  - `Math.floor()` rounds down to nearest integer
  - `Math.random()` generates a random number between 0(inclusive) and 1(not inclusive)

### Creating an instance of the date object

- In order to work with dates, you create an instance of the **Date** object. You can then specify the time and date that you want it to represent. (p. 137)

```javascript
var today = new Date();
```

### Summary

- Functions allow you to group a set of related staements together that represent a single task.

- Functions can take parameters (information requirements to do their job) and may return a value.

- An object is a series of variables and functions that represent something from the world around you.

- In an object, variables are known as properties of the object; functions are known as methods of the object.

- Web browsers implement objects that represent the browser window and the doccument loaded into the browser window.

- JavaScript also has several built-in objects such as `String`, `Number`, `Math`, and `Date`. Their properties and methods offer functionality that help you write scripts.

- Arrays and objects can be used to create complex sets (and both can contain the other).

[back to README](README.md)
