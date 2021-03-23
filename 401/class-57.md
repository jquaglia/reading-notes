# Class 27

## Review, Research, and Discussion

1. Does a deployed React application require a server?

Node is not required in order to use React. ... npx itself is a Node tool which allows you to run a package, in this case with Create React App, which allows you to easily start a new React project. The server that you see is simply to allow for the reloading of the app in response to file changes in real time.

1. Why do we prefer to test a React application at the behavior rather than the unit level?

With components, the distinction between a “unit” and “integration” test can be blurry. If you’re testing a form, should its test also test the buttons inside of it? Or should a button component have its own test suite? Should refactoring a button ever break the form test?

1. What does `npm run build` do?

npm run build does nothing unless you specify what "build" does in your package.json file. It lets you perform any necessary building/prep tasks for your project, prior to it being used in another project.

npm build is an internal command and is called by link and install commands, according to the documentation for build:

This is the plumbing command called by npm link and npm install.

You will not be calling npm build normally as it is used internally to build native C/C++ Node addons using node-gyp.

1. Describe the actual composition / architecture of a React application

The key feature of React is composition of components.

| Term      | Description |
| ----------- | ----------- |
|BDD|Behaviour-Driven Development (BDD) is a collaborative approach to software development that bridges the communication gap between business and IT. BDD helps teams communicate requirements with more precision, discover defects early and produce software that remains maintainable over time.|
|Acceptance Tests|In engineering and its various subdisciplines, acceptance testing is a test conducted to determine if the requirements of a specification or contract are met.|
|mounting|Mounting is the process of outputting the virtual representation of a component into the final UI representation (e.g. DOM or Native Components).|
|build|this is the `build` of your app. It is essentially the completely compiled version of all of your code.|

## setState

- `setState()` is the only legit way to update the state after the intial state setup.

- `setState()` should be treated asynchronously — in other words, do not always expect that the state has changed after calling `setState()`.

## Handling Events

Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:

- React events are named using camelCase, rather than lowercase.

- With JSX you pass a function as the event handler, rather than a string.

- Another difference is that you cannot return false to prevent default behavior in React. You must call preventDefault explicitly.

## Forms

HTML form elements work a little bit differently from other DOM elements in React, because form elements naturally keep some internal state. For example, this form in plain HTML accepts a single name:

```jsx
<form>
  <label>
    Name:
    <input type="text" name="name" />
  </label>
  <input type="submit" value="Submit" />
</form>
```

- In HTML, form elements such as `<input>`, `<textarea>`, and `<select>` typically maintain their own state and update it based on user input.

- In React, mutable state is typically kept in the state property of components, and only updated with `setState()`.

- In React, a `<textarea>` uses a value attribute instead. This way, a form using a `<textarea>` can be written very similarly to a form that uses a single-line input:

```jsx
class EssayForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      value: 'Please write an essay about your favorite DOM element.'
    };

    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  handleChange(event) {
    this.setState({value: event.target.value});
  }

  handleSubmit(event) {
    alert('An essay was submitted: ' + this.state.value);
    event.preventDefault();
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Essay:
          <textarea value={this.state.value} onChange={this.handleChange} />
        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```

React, instead of using this selected attribute, uses a value attribute on the root select tag. This is more convenient in a controlled component because you only need to update it in one place. For example:

```jsx
class FlavorForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {value: 'coconut'};

    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  handleChange(event) {
    this.setState({value: event.target.value});
  }

  handleSubmit(event) {
    alert('Your favorite flavor is: ' + this.state.value);
    event.preventDefault();
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Pick your favorite flavor:
          <select value={this.state.value} onChange={this.handleChange}>
            <option value="grapefruit">Grapefruit</option>
            <option value="lime">Lime</option>
            <option value="coconut">Coconut</option>
            <option value="mango">Mango</option>
          </select>
        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```

When you need to handle multiple controlled input elements, you can add a name attribute to each element and let the handler function choose what to do based on the value of event.target.name.

```jsx
class Reservation extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      isGoing: true,
      numberOfGuests: 2
    };

    this.handleInputChange = this.handleInputChange.bind(this);
  }

  handleInputChange(event) {
    const target = event.target;
    const value = target.type === 'checkbox' ? target.checked : target.value;
    const name = target.name;

    this.setState({
      [name]: value
    });
  }

  render() {
    return (
      <form>
        <label>
          Is going:
          <input
            name="isGoing"
            type="checkbox"
            checked={this.state.isGoing}
            onChange={this.handleInputChange} />
        </label>
        <br />
        <label>
          Number of guests:
          <input
            name="numberOfGuests"
            type="number"
            value={this.state.numberOfGuests}
            onChange={this.handleInputChange} />
        </label>
      </form>
    );
  }
}
```

## State and Lifecycle

- We can declare special methods on the component class to run some code when a component mounts and unmounts

- These methods are called “lifecycle methods”.

- 3 Things to know about `setState()`

  - Do Not Modify State Directly

  - State Updates May Be Asynchronous

  - State Updates are Merged

### The Data Flows Down

- Neither parent nor child components can know if a certain component is stateful or stateless, and they shouldn’t care whether it is defined as a function or a class

- This is why state is often called local or encapsulated. It is not accessible to any component other than the one that owns and sets it.

## Components and Props

- Components let you split the UI into independent, reusable pieces, and think about each piece in isolation.

- The simplest way to define a component is to write a JavaScript function:

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

- Components can refer to other components in their output. This lets us use the same component abstraction for any level of detail. A button, a form, a dialog, a screen: in React apps, all those are commonly expressed as components.

- Don’t be afraid to split components into smaller components:

```jsx
function Comment(props) {
  return (
    <div className="Comment">
      <div className="UserInfo">
        <img className="Avatar"
          src={props.author.avatarUrl}
          alt={props.author.name}
        />
        <div className="UserInfo-name">
          {props.author.name}
        </div>
      </div>
      <div className="Comment-text">
        {props.text}
      </div>
      <div className="Comment-date">
        {formatDate(props.date)}
      </div>
    </div>
  );
}
```

- Whether you declare a component as a function or a class, it must never modify its own props. Consider this sum function:

```jsx
function sum(a, b) {
  return a + b;
}
```

Such functions are called “pure” because they do not attempt to change their inputs, and always return the same result for the same inputs.

In contrast, this function is impure because it changes its own input:

```jsx
function withdraw(account, amount) {
  account.total -= amount;
}
```

React is pretty flexible but it has a single strict rule:

__All React components must act like pure functions with respect to their props.__
