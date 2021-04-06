# Class 37

## Review, Research, and Discussion

1. Why choose Redux instead of the Context API for global state?

    - Redux helps you stay organized if you are working on a big project

1. What is the purpose of a reducer?

    - to take in the new state data and combine it with the old state data

1. What does an action contain?

    - payload

1. Why do we need to copy the state in a reducer?

    - Redux's state is readonly, so you can't mutate the array and return it. You must send a copy with the mutations otherwise you break the pattern. Same applies if you're reordering arrays.

| Term      | Description |
| ----------- | ----------- |
|immutable state|Immutable state is state that cannot be changed. Immutable objects (for which none of the state can be changed) become important when you are dealing with concurrency, the ability for more than one processor in your computer to operate on that object at the same time.|
|time travel in redux|The Redux DevTools records dispatched actions and the state of the Redux store at every point in time. This makes it possible to inspect the state and travel back in time to a previous application state without reloading the page or restarting the app.|
|action creator|Action: code that causes an update to the state when something happens.|
|reducer|A reducer is a function that determines changes to an application's state. It uses the action it receives to determine this change.|
|dispatch|dispatch is a function of the Redux store. You call store. dispatch to dispatch an action. This is the only way to trigger a state change.|
