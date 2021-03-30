# Class 32

## Review, Research, and Discussion

1. What does a component’s lifecycle refer to?

    - Lifecycle of a component is series of methods that are invoked in different stages of the component's existence.

1. Why do you sometimes need to “wrap” functions in `useCallback` when called from within `useEffect`

    - Often, effects create resources that need to be cleaned up before the component leaves the screen, such as a subscription or timer ID. To do this, the function passed to useEffect may return a clean-up function

1. Why are functional components preferred over class components?

    - functional components are easier to read once you know how they work. Also, there might some security issues with the older way.

1. What is wrong with the following code?

    - I don't know. If I had to guess, I'd say `useState()` needs an object or array in it and not just a value?

```javascript
import React, {useState, useEffect} from 'react';

function MyComponent(props) {
  const [count, setCount] = useState(0);

  function changeCount(e) {
    setCount(e.target.value);
  }

  let renderedItems = []

  for (let i = 0; i < count; i++) {
    useEffect( () => {
      console.log('component mount/update');
    }, [count]);

    renderedItems.push(<div key={i}>Item</div>);
  }

  return (<div>
     <input type='number' value={count} onChange={changeCount}/>
      {renderedItems}
    </div>);
}
```

| Term      | Description |
| ----------- | ----------- |
|state hook|`useState` The only argument to the `useState()` Hook is the initial state. Unlike with classes, the state doesn’t have to be an object. We can keep a number or a string if that’s all we need.|
|effect hook|This is used in place of life cycle components. Allows you to define properties that will trigger React API features|
|reducer hook|useReducer, which is more suited for managing state objects that contain multiple sub-values. An alternative to useState. Accepts a reducer of type `(state, action) => newState`, and returns the current state paired with a dispatch method.|
