# Class 39

## Review, Research, and Discussion

1. Compare and Contrast Redux Toolkit with Redux “Ducks”

    - Ducks is essentially a proposal for bundling reducers, action types, and actions all into the same file.

    - Ducks seeks to solve the issue of the toggled back and forth repetitive nature of organizing by type. With Ducks, rather than splitting up all related code, I can package it into redux modules

    - Redux state is typically organized into "slices", defined by the reducers that are passed to combineReducers

    - The common approach is to define a slice's reducer function in its own file, and the action creators in a second file.

1. What is the principle advantage of Redux Toolkit

    - It allows us to write more efficient code, speed up the development process, and automatically apply the best-recommended practices. It was mainly created to solve the THREE MAJOR ISSUES with Redux:

      - Configuring a Redux store is too complicated

      - Have to add a lot of packages to build a large scale application

      - Redux requires too much boilerplate code which makes it cumbersome to write efficient and clean code.

| Term      | Description |
| ----------- | ----------- |
|redux toolkit slices|A Redux Slice is a collection of reducer logic and actions for a single feature of our app. The name “slice” comes from the idea that we're splitting up the root Redux state object into multiple “slices” of slate.|
|namespace|In computing, a namespace is a set of signs that are used to identify and refer to objects of various kinds. A namespace ensures that all of a given set of objects have unique names so that they can be easily identified.|
