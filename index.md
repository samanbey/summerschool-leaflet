# Developing open source interactive web maps using Leaflet

## Outcomes
- HTML and JavaScript basics needed for developing Leaflet-based web maps
- embedding a Leaflet map viewer into HTML pages
- adding tile map layers
- displaying markers and vector features
- adding mouse event handlers
- loading geojson data
- adding a geocoder
- styling vectors

## Suggested background materials
[HTML basics](https://www.w3schools.com/html/)

[CSS basics](https://www.w3schools.com/css/)

[JavaScript basics](https://www.w3schools.com/js/)

[Leaflet documentation](https://leafletjs.com/)

## Software requirements
- A code editor is required for creating HTML/JavaScript codes. Suggestions:
    - [Notepad++](https://notepad-plus-plus.org/)
    - [Visual Studio Code](https://code.visualstudio.com/)
- A web browser for displaying the web maps created.
- A public web storage where you can host your web map. (This is not required for the first few examples but becomes important when fetching data files (e.g. GeoJSON data). Alternatively you can also set up a webserver to localhost or use Firefox with special settings to let it reach your local drive for data files
    - Visual Studio Code has an extension called Live Server (find it in File/Preferences/Extensions)
    - In Mozilla Firefox type ```about:config``` to the address bar, then find the ```security.fileuri.strict_origin_policy``` setting and set it to ```false```

## Lessons
{% for post in site.posts reversed %}
 - [{{ post.title }}]({{ site.baseurl }}{{ post.url }})
{% endfor %}

## Examples for tasks
{% for f in site.static_files %}
{% if f.path contains 'examples/t' %} - [{{ f.name }}]({{ site.baseurl }}{{ f.path }})
{% endif %}
{% endfor %}

