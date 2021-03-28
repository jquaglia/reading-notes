# Class 28

## Review, Research, and Discussion

1. Why do we not need more .html pages in a multi-page React app?

    - You can use react router to 'create' new html pages and routes

1. If we wanted a component to show up on every page, where would we put it and why?

    - Inside the `<BrowserRouter />`, outside a `<Route />`

    - This will allow something to render on all pages regardless of the route.

1. What does props.children contain?

    - is used to display whatever you include between the opening and closing tags when invoking a component.

| Term      | Description |
| ----------- | ----------- |
|Composition|Composition is the act of combining parts or elements to form a whole.|
|Children / Child Components|child components are components that are nested inside of another jsx tag|
|Hash Routing|Routing means doing something in response to a change in the browser’s current URL. hash-based routing, using the portion of the page’s URL starting with #, i.e. the hash.|
|Link Routing|Provides declarative, accessible navigation around your application through the route exact route name.|
