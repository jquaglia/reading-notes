# Class 12

## Charts.js

- Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool. They're easier to look at and convey data quickly but they're not always easy to create.

```html
<canvas id="myChart" width="400" height="400"></canvas>
<script>
var ctx = document.getElementById('myChart').getContext('2d');
var myChart = new Chart(ctx, {
    type: 'bar',
    data: {
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
        datasets: [{
            label: '# of Votes',
            data: [12, 19, 3, 5, 2, 3],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255, 99, 132, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        scales: {
            yAxes: [{
                ticks: {
                    beginAtZero: true
                }
            }]
        }
    }
});
</script>
```

This is an example of a bar chart for a single dataset using Chart.js.

### The canvas element

- At first sight a `<canvas>` element looks like the `<img>` element, with the only clear difference being that it doesn't have the `src` and `alt` attributes.

### Fallback Content

- The `<canvas>` element differs from `<img>` tag in that it is easy to define some fallback content, to be displayed in older browsers not supporting it.

- As a a consequence of the way fallback is provided, the `<canvas>` element requires a closing tag.

### The rendering context

- The `<canvas>` element creates a fixed-size drawing surface that exposes one or more __rendering contexts__, which are used to create and manipulate the content shown.

### Checking for support

- The fallback content is displayed in browsers which do not support `<canvas>`. Scripts can also check for support programmatically by simply testing for the presence of the `getContext()` method.

### The grid

- The canvas grid or __coordinate space__ is just like a graph wiht coordinates (x, y)

### Drawing Paths

- `beginPath()` creates a new path. once created, future drawing commands are directed into the path and used to build the path up.

- `Path methods` Methods to set different paths for objects.

- `closePath()` adds a straight line to the path, going to the start of the current sub-path.

- `stroke()` draws the shape by stroking its outline.

- `fill()` draws a solid shape by filling the paths content area.

### Line Styles

- `lineWidth = value` sets the width of lines drawn in the future

- `lineCap = type` sets the appearance of the ends of lines.

- `lineJoin = type` sets the appearance of the "corners" where lines meet

- `miterLimit = value` establishes a limit on the miter when two lines joing at a sharp angle, to let you control how thick the junction becomes.

- `getLineDash()` returns the current line dash pattern array containing an even number of non-negative numbers.

- `lineDash(segments)` sets the current line dash pattern

- `lineDashOffset = value` specifies where to start a dash array on a line.

### Drawing text

- `fillText(text, x, y [, maxWidth])` fills a given text at the given (x, y) position. Optionally with a maximum width to draw.

- `strokeText(text, x, y [, maxWidth])` strokes a given text at the given (x, y) position. Optionally with a maximum width to draw.

[back to REAME](../README.md)
