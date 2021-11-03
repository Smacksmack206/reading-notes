#Cedric's Notes for code-201n24 course

# <cite> Reading from Chart.js API article & docs </cite>

Chart.js allows you to quickly create charts with a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page.

## Drawing a line chart
To draw a line chart, the first thing we need to do is create a canvas element in our HTML in which Chart.js can draw our chart. So add this to the body of our HTML page:

```
<canvas id="buyers" width="600" height="400"></canvas>
Next, we need to write a script that will retrieve the context of the canvas, so add this to the foot of your body element:

<script>
    var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData);
</script>
```

## Drawing a pie chart
Our line chart is complete, so let’s move on to our pie chart. First, we need the canvas element:

<canvas id="countries" width="600" height="400"></canvas>
Next, we need to get the context and to instantiate the chart:

```
var countries= document.getElementById("countries").getContext("2d");
new Chart(countries).Pie(pieData, pieOptions);


## Drawing a pie chart
Our line chart is complete, so let’s move on to our pie chart. First, we need the canvas element:

<canvas id="countries" width="600" height="400"></canvas>
Next, we need to get the context and to instantiate the chart:

var countries= document.getElementById("countries").getContext("2d");
new Chart(countries).Pie(pieData, pieOptions);
```