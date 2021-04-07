# Class 38

## Review, Research, and Discussion

1. How granular should your reducers be?

    - They should each do one thing.

1. Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched

    - This is a pro if you are organized, and a con if un-organized

1. Name a strategy for preventing the above

    - Be organized? Name your action something else?

| Term      | Description |
| ----------- | ----------- |
|store|this is where all state is stored in redux|
|combined reducers|It turns out that Redux lets us combine multiple reducers into one that can be passed into createStore by using a helper function named combineReducers|
