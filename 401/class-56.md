# Class 26

## Review, Research, and Discussion

1. Name 5 Javscript UI Frameworks (other than react)

    - Angular

    - Vue

    - Ember

    - Svelte 3

    - Electron?

1. What's the difference between a framework and a library?

    - The difference between a framework and library lies in a term called inversion of control. When you use a library, you are in charge of the flow of the application. You are choosing when and where to call the library. When you use a framework, the framework is in charge of the flow. It provides some places for you to plug in your code, but it calls the code you plugged in as needed.

| Term      | Description |
| ----------- | ----------- |
|Rendering|Rendering refers to showing the output in the browser|
|Templates|A template is a chunk of HTML that you need to inject onto the page. Often templates are created “server side” – in that they come to the JavaScript fully formed and just need to be put into the DOM|
|State|State describes the status of the entire program or an individual object.|

## Component Based UI

### JSX

```javascript
const element = <h1>Hello, world!</h1>;
```

This tag syntax is called JSX, and it is a syntax extension to JavaScript.

- JSX produces React 'elements'.

- After compilation, JSX expressions become regular JavaScript function calls and evaluate to JavaScript objects.

- You may use quotes to specify string literals as attributes

- You may also use curly braces to embed a JavaScript expression in an attribute

- If a tag is empty, you may close it immediately with `/>`, like XML

- JSX prevents injection attacks. It is safe to embed user input in jsx.

- JSX represents objects. Babel compiles JSX down to React.createElement() calls. These two examples are identical:

```javascript
const element = (
  <h1 className="greeting">
    Hello, world!
  </h1>
);
```

```javascript
const element = React.createElement(
  'h1',
  {className: 'greeting'},
  'Hello, world!'
);
```

These objects are called “React elements”.

### Rendering Elements

- Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.

- To render a React element into a root DOM node, pass both to `ReactDOM.render()`:

```javascript
const element = <h1>Hello, world</h1>;
ReactDOM.render(element, document.getElementById('root'));
```

- React elements are immutable. Once you create an element, you can't change its children or attributes.

- React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.

- thinking about how the UI should look at any given moment, rather than how to change it over time, eliminates a whole class of bugs.
