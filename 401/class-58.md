# Class 28

## Review, Research, and Discussion

1. Can a parent component access the state of a child component?

- In case that you really need to access to a child state that is declared as a functional component (hooks) you can declare a ref in the parent component, then pass it as a ref attribute to the child but you need to use React.

1. What can be passed along in a prop variable?

- data can be passed along in a prop.

1. How can a child component "know" the state of another component?

- via passing data in a prop

| Term      | Description |
| ----------- | ----------- |
|component props|“Props” is a special keyword in React, which stands for properties and is being used for passing data from one component to another. But the important part here is that data with props are being passed in a uni-directional flow. ( one way from parent to child)|
|component state|React components has a built-in state object. The state object is where you store property values that belongs to the component. When the state object changes, the component re-renders.|
|application state|In an application, state is the interface between your data from any kind of backend or local change and the representation of this data with UI-elements in the frontend. State is able to keep the data of different components in sync because each state update will rerender all relevant components.|