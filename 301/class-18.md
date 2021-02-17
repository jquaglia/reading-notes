# Class 03

## Javascript Templating Language and Engine - Mustache.js with Node and Express

### Javascript Templating

- is a jast and efficient technique to render client-side view templates with JS by using JSON data source.

### Mustache

- is a logic-less template syntax.

- "logic-less" because there are no if statements, else clauses, or for loops.

- instead there are only tags

```javascript
Mustache.render(“Hello, {{name}}”, { name: “Sherlynn” });
// returns: Hello, Sherlynn
```

- two braces around {{name}}. this is mustache syntax to show that it is a placeholder

### Mustache-Express

- if you intend to use mustache with Node and Express, you can use mustache-express.

[back to README](README.md)
