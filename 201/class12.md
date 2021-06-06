# Chart.js, Canvas

## Charts 
### what is Chart.js?
`Chart.js` is a community maintained open-source library "in gitHub" that helps you easily visualize data using JavaScript. It’s similar to Chartist and Google Charts. It supports 8 different chart types (including bars, lines, & pies), and they’re all responsive. In other words, you set up your chart once, and Chart.js will do the heavy-lifting for you and make sure that it’s always legible (for example by removing some uncritical details if the chart gets smaller).

**In a gist, this is what you need to do to draw a chart with Chart.js:**

- Define where on your page to draw the graph.

- Define what type of graph you want to draw.

- Supply Chart.js with data, labels, and other options.

and you’ll get a beautiful, responsive, graph!

![Image](data:image/png;base64,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)



#### Step 1: Add Chart.js
The first thing we need to do is download `Chart.js.` Copy the Chart.min.js out of the unzipped folder and into the directory you’ll be working in. Then create a new html page and import the script:

```html
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Chart.js demo</title>
        <script src='Chart.min.js'></script>
    </head>
    <body>
    </body>
</html>
```

#### Step 2 :Prepare a place in your HTML to render the chart
For this project, you should prepare a simple playground with a HTML file with only the essentials. Download the starting point and open the folder, and you should see three files:
- `index.html`
- `styles.css`
- `app.js`

#### Step 3: Prepare the data
The data you have and you want to add it into the chart

#### Step 4: Drawing a line chart
To draw a line chart, the first thing we need to do is create a canvas element in our HTML in which `Chart.js` can draw our chart. So add this to the body of our HTML page:

```html
<canvas id="buyers" width="600" height="400"></canvas>
```

The last thing we need to prepare before we can start visualizing our data is to define an area in our HTML where we want to draw the graph. For `Chart.js` you do this by adding a `canvas` element, and setting width and height to define the proportions of your graph.

## Canvas element
Then, using that `canvas element`, we create a line chart `(type: 'line')`, and pass along some of our data. 
- `labels:` years sets our array of years (that we created earlier) for the labels along the x-axis, and 
- `data:` africa uses our africa variable to draw the line.

For every line that we want to create, we add another object to the datasets array. On every object we can make a range of adjustments, we can not only pass the data to draw the line, but we can change the name, change the beavior, and change the looks of the line.

The great things about Chart.js are that it’s simple to use and really very flexible. Plus, once you’ve mastered the basics here, you’ll discover that there are tons of options listed in the documentation.


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
            y: {
                beginAtZero: true
            }
        }
    }
});
</script>
```

#### Drawing a Path
`Drawing a path`: A path is a list of points, connected by segments of lines that can be of different shapes, curved or not, of different width and of different color. A path, or even a subpath, can be closed. To make shapes using paths, we take some extra steps:

1. **_First_, you create the path.**
Then you use drawing commands to draw into the path.Once the path has been created, you can stroke or fill the path to render it.

Colors If we want to apply colors to a shape, there are two important properties we can use:


1. fillText(text, x, y, width, height)
Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.

2. strokeRect(text, x, y, width, height)
Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.

3. clearText(x, y, width, height)
Clears the specified rectangular area, making it fully transparent.


#### Styling text
- `font = value`
The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.
- `textAlign = value`
Text alignment setting. Possible values: start, end, left, right or center. The default value is start.
- `textBaseline = value`
Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.
- `direction = value`
Directionality. Possible values: ltr, rtl, inherit. The default value is inherit.

![Image2](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text/baselines.png)


#### Colors

- `fillStyle = color`
Sets the style used when filling shapes.
- `strokeStyle = color`
Sets the style for shapes' outlines.