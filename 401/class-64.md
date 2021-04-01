# Class 34

## Review, Research, and Discussion

1. Why is the Context API useful?

    - Context API is a way to enable components to share some data without explicitly passing via each component manually. Context is like a global object to the React component sub-tree. This is useful for managing things that need to keep state globally like dark mode or themes in an app.

1. Can a component outside of a provider get its context?

    - you can use context in functional components by making use of useContext hook

1. What are some common use cases for using the Context API?

    - dark mode/themes, user settings, filters

1. Describe “Context Hell”

    - When we’re working with the React Context API it’s not hard to find ourselves in a situation where we’re using multiple Context Providers and creating a Provider Hell like this:

```javascript
const Main = () => (
  <ProviderA>
    <ProviderB>
      <ProviderC>
        <ProviderD>
          <ProviderE>
            <App />
          </ProviderE>
        </ProviderD>
      </ProviderC>
    </ProviderB>
  </ProviderA>
)
```

| Term      | Description |
| ----------- | ----------- |
|global state|A global state would solve this by keeping a state at the top level and provide access methods to all child levels without the need to pass props.|
|global context|Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language.|
|provider|Every Context object comes with a Provider React component that allows consuming components to subscribe to context changes. The Provider component accepts a value prop to be passed to consuming components that are descendants of this Provider. One Provider can be connected to many consumers. Providers can be nested to override values deeper within the tree. |
|consumer|A React component that subscribes to context changes. Using this component lets you subscribe to a context within a function component. |
