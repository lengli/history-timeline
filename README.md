# history-timeline

The objective here is to create simple history timeline based on [visjs](https://github.com/visjs/vis-timeline).


## Example

A basic example on loading a Timeline is shown below. More examples can be
found in the [examples directory](https://github.com/visjs/vis-timeline/tree/master/examples/)
of the project.

```html
<!doctype html>
<html>
<head>
  <title>Network</title>
  <script type="text/javascript" src="//unpkg.com/vis-timeline@latest/dist/vis-timeline-graph2d.min.js"></script>
  <link href="//unpkg.com/vis-timeline@latest/dist/vis-timeline-graph2d.min.css" rel="stylesheet" type="text/css" />
  <style type="text/css">
    #mynetwork {
      width: 600px;
      height: 400px;
      border: 1px solid lightgray;
    }
  </style>
</head>
<body>
<div id="visualization"></div>
<script type="text/javascript">
  // DOM element where the Timeline will be attached
  var container = document.getElementById('visualization');

  // Create a DataSet (allows two way data-binding)
  var items = new vis.DataSet([
    {id: 1, content: 'item 1', start: '2014-04-20'},
    {id: 2, content: 'item 2', start: '2014-04-14'},
    {id: 3, content: 'item 3', start: '2014-04-18'},
    {id: 4, content: 'item 4', start: '2014-04-16', end: '2014-04-19'},
    {id: 5, content: 'item 5', start: '2014-04-25'},
    {id: 6, content: 'item 6', start: '2014-04-27', type: 'point'}
  ]);

  // Configuration for the Timeline
  var options = {};

  // Create a Timeline
  var timeline = new vis.Timeline(container, items, options);
</script>
</body>
</html>
```
