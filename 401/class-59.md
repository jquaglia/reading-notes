# Class 29

## Review, Research, and Discussion

1. Do child components have direct access to props/state from the parent?

- there is no way to pass props from a child component to a parent component. However, we can always pass around functions from the parent to child component. The child component can then make use of these functions. The function can then update the state in a parent component

1. When a component “wraps” another component, how does the child component’s output get rendered?

- The components that receive state from the higher-order component will function as presentational components. State gets passed to them and they conditionally render UI based on it. They do not bother with the management of state.

1. Can a component, such as `<Content />`, which is a child also be used as a standalone component elsewhere in the application?

- No

1. What trick can a parent use to share all `props` with it’s children

- f you happen to know all of the props, then you could pass them all by just listing them out individually as the new props for the child component.

| Term      | Description |
| ----------- | ----------- |
|props.children|The React docs say that you can use props.children on components that represent ‘generic boxes’ and that don’t know their children ahead of time. For me, that didn’t really clear things up. I’m sure for some, that definition makes perfect sense but it didn’t for me. My simple explanation of what this.props.children does is that it is used to display whatever you include between the opening and closing tags when invoking a component.|
|composition|Composition is the act of combining parts or elements to form a whole.Components are the UI building blocks in React applications, like pure functions are the building blocks of function composition.|
