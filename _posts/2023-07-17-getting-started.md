---
title: "01 – Getting started"
---

# 01 – Getting started

A Leaflet map is an interactive map viewer widget in your HTML page. Let's start with a simple HTML document:

``` html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8" />
        <meta name="viewport" content="initial-scale=1.0, user-scalable=no" />        
        <title>My first web map</title>
    </head>
    <body>
        <h1>My first web map</h1>
    </body>
</html>
```

Now we'll need to include the CSS and JavaScript codes of Leaflet. You can either download them or simply link their hosted versions within the HEAD section of your HTML document:
``` html
        <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
        <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
```

The next thing needed is a DIV element which wll contain the map viewer. It can be anywhere in the BODY section of your HTML. Give it an ID to help identifying it:
``` html
        <div id="map"></div>
```

We also need to set the size of this map container element. The easiest way is to do it with CSS styling rules. We'll insert a STYLE element into the HEAD section of the HTML document and set the width and height of the element that has the 'map' ID:
``` html
        <style>
            #map { width: 600px; height: 400px; }
        </style>
```

Finally, we need to add a few lines of JavaScript code that creates the map interface and adds a tiled map layer to it. Place this code into a SCRIPT element to the end of the BODY section of your HTML:
``` html
        <script>
            // create map viewer object
            var map = L.map('map').setView([47.475, 19.061], 15);
            
            // add a tiled map layer with OpenStreetMap tiles
            L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
                attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>'
            }).addTo(map);
        </script>
```

Open the completed HTML document in a browser and you should see something like this:
https://samanbey.github.io/summerschool-leaflet/l0.html
