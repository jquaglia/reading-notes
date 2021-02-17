# Class 09

## Forms

### Why Forms

- The best known form on the web is probably the search box that sits right in the middle of Google's homepage.

### Form Controls

- There are several types of form controls that you can use to collect information from visitors to your site.

### Summary

- Whenever you want to collect information from visiotrs you will need a form, which lives inside a `<form></form>` element.

- Information from a form is sent in name/value pairs.

- Each form control is given a name, and the text the user types in or the values of the options they select are sent to the server.

- HTML5 introduces new form elements which make it easier for visitors to fill in forms.

## Lists, Tables, and Forms

- In addition to the CSS properties covered in other chapters which work with the contents of all elements, there are several others that are specifically used to control the appearance of lists, tables, and forms.

- List markers can be given different appearances using the list-style-type and list-style image properties.

- Table cells can have different borders and spacing in different browsers, but there are properties you can use to control them and make them more consistent.

- Forms are easier to use if the form controls are vertically aligned using CSS.

- Forms benefit from styles that make them feel more interactive.

## Events

### How events trigger javascript code

- When the user interacts with the HTML on a web page, there are three steps involved in getting it to trigger some JavaScript code. Together these steps are known as __event handling__.

### Three ways to bind an event to an element

- Event handlers let you indicate which event you are waiting for on any particular element. There are three types of event handlers:

  - HTML Event handlers (wrong way to do things)

  - Traditional DOM event handlers

  - DOM level 2 event listeners

### Traditional DOM event handlers

- All modern browsers understand this way of creating an event handler, but you can only attach one function to each even handler.

### Event Listeners

- Event listeners are a more recent approach to handling events. They can deal with more than one function at a time but they are not supported in older browsers.

### Using parameters with event handlers and listeners

- Because you cannot have parentheses after the functino names in event handlers or listeners, passing arguments requires a work around.

### Supporting older versions of ie

- IE5-8 had a different event model and did not support `addEventListener()` but you can provide fallback code to make event listeners work with older versions of IE.

### The event object

- When an event occurs, the event object tells you information about the event, and the element it happened to.

### Event delegation

- Creating event listeners for a lot of elements can slow down a page, but event flow allows you to listen for an event on a parent element.

### Changing default behavior

- The event object has methods that change: the default behavior of an element and how the elements ancestors respond to the event.

### User Interface events

- UI events occur as a result of interaction with the browser window rather than the HTML page contained within it, e.g., a page having loaded or the browser window being resized.

### Focus and Blur events

- The HTML elements you can interact with, such as links and form elements, can gain focus. These events fire when they gain or lose focus.

### Mouse events

- The mouse events are fired when the mouse is moved and when its buttons are clicked

### Keyboard events

- The keyboard events are fired when a user interacts with the keyboard.

### Form events

- There are two events used commonly with forms. In particular you are likely to see submit used in form validation.

### Mutation events and observers

- Whenever elements are added to or removed from the DOM, its structure changes. This change triggers a mutation event.

### HTML5 events

- Here are three page-level events that have been included in versions of the HTML5 spec that have become popular very quickly.

### Summary 2

- Events are the browsers way of indicating when something has happened (such as when a page has finished loading or a button has been clicked).

- Binding is the process of stating which event you are waiting to happen, and which element you are waiting for that event to happen upon.

- When an event occurs on an element, it can trigger a JS function. When this function then changes the web page in some way, it feels interactive because it has responded to the user.

- You can use event delegation to monitor for events that happen on all of the children of an element.

- The most commonly used events are W3C DOM events, although there are others in the HTML5 specifications as well as browser-specific events.

[back to README](../README.md)
