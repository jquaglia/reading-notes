# Class 09

## Functional Programming

### What is functional programming?

functional programming is a programming paradigm that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.

### Pure Functions

- it returns the same result if given the same arguments

- it does not cause any observable side effects

```javascript

let PI = 3.14;

const calculateArea = (radius) => radius * radius * PI;

calculateArea(10); // returns 314.0
```

impure^^

```javascript
let PI = 3.14;

const calculateArea = (radius, pi) => radius * radius * pi;

calculateArea(10, PI); // returns 314.0
```

pure^^

The second example is pure because we are no longer accessing an external object.

- If our function reads external files, it's not pure --the files could change.

- Any function that relies on a random number generator cannot be pure.

- If our function modifies a global object or a parameter passed by reference --it's not pure.

- pure functions are easier to test.

### Immutability

When data is immutable, its state cannot change after it's created. If you want to change an immutable object, you can't. Instead, you create a new object with the new value.

```javascript
var values = [1, 2, 3, 4, 5];
var sumOfValues = 0;

for (var i = 0; i < values.length; i++) {
  sumOfValues += values[i];
}

sumOfValues // 15
```

How do we handle mutability in iteration? Recursion!

```javascript
let list = [1, 2, 3, 4, 5];
let accumulator = 0;

function sum(list, accumulator) {
  if (list.length == 0) {
    return accumulator;
  }

  return sum(list.slice(1), accumulator + list[0]);
}

sum(list, accumulator); // 15
list; // [1, 2, 3, 4, 5]
accumulator; // 0
```

So here we have the `sum` function that receives a vector of numerical values. The function calls itself until we get the list empty (our recursion base case). For each 'iteration' we weill add the value to the `total` accumulator. With recursion we keep our variables immutable.

### Referential Transparency

- If a function consistently yields the same result for the same input, it is referentially transparent.

- `pure functions + immutable data = referential transparency`

With this concept, a cool thing we can do is to memoize the function. Imagine we have this function:

```javascript
const sum = (a, b) => a + b;
```

And we call it with these parameters:

```javascript
sum(3, sum(5, 8));
```

The sum(5, 8) equals 13. This function will always result in 13. So we can do this:

```javascript
sum(3, 13);
```

And this expression will always result in 16. We can replace the entire expression with a numerical constant and memoize it.

### Functions as first-class entities

The idea of functions as first-class entities is that functions are also treated as values and used as data. they can:

- refer to it from constants and variables

- pass it as a parameter to other functions

- return it as a result from other functions

[back to README](README.md)
