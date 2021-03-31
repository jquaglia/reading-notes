# Class 33

## Review, Research, and Discussion

1. Describe use cases for `useMemo()` and `useReducer()`

    - `useReducer` is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.

    - `useMemo` will only recompute the memoized value when one of the dependencies has changed. This optimization helps to avoid expensive calculations on every render.

1. Why do custom hooks need the `use` prefix?

    - Its name should always start with use so that you can tell at a glance that the rules of Hooks apply to it.

1. What do custom hooks usually do?

    - Custom hooks allow you to create functionality that can be reused across different components. You can of course just have functions to reuse functionality, but hooks come with the advantage of being able to 'hook' into things like component lifecycle and state.

1. Using any list of custom hooks, research and name one that you think will be useful in your applications

    - react-fetch-hook

1. Describe how a hook that fetches API data might work

  ```javascript
  import React from "react";
  import useFetch from "react-fetch-hook";

  const Component = () => {
    const { isLoading, data } = useFetch("https://swapi.co/api/people/1");

    return isLoading ? (
      <div>Loading...</div>
    ) : (
      <UserProfile {...data} />
    );
  };
  ```

| Term      | Description |
| ----------- | ----------- |
|reducer|the benefit of the state reducer pattern is in the fact that it allows "inversion of control" which is basically a mechanism for the author of the API to allow the user of the API to control how things work internally.|
