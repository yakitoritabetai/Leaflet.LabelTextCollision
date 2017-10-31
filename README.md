# Leaflet.LabelTextCollision

Leaflet.LabelTextCollision is a [LeafletJS](http://www.leafletjs.com) plug-in to display labels on vector data while avoiding label collisions.

Supports Leaflet 1.2.0+ branches.

To avoid label overlapping, this plugin hides some labels. Labels defined first will have preference over labels defined last, so arrange your labels from the most important to the least important.

`L.LabelTextCollision` implements a `L.Renderer` based on `L.Canvas`, as to not create an excess of DOM elements which might slow down rendering in the browser.

# demo
Check out the <a href="https://yakitoritabetai.github.io/Leaflet.LabelTextCollision/">demo</a>

# Usage examples

* Create a new instance of `L.LabelTextCollision` specifying the collision flag option.
* Use the map's `renderer` option to force rendering of vector data with that instance

```
var labelTextCollision = new L.LabelTextCollision({
  collisionFlg : true
});

var map = new L.Map('map', {
  layers : [ osm ],
  center : new L.LatLng(35.695786, 139.749213),
  zoom : 10,
  renderer : labelTextCollision
});
```

* Instances of `L.Path` (`L.Polyline`s, `L.Polygon`s, `L.Circle`s, `L.CircleMarker`s) have a new `text` option. Use it to specify the label contents.
* The label will only be displayed if it doesn't collide with an existing label

```
var p = L.polyline([[35.695786, 139.749213], [35.696786, 139.748213], [35.695786, 139.747213]], {
    weight: 12,
    color: '#fe57a1',

    text: 'polylineText',
    textStyle: {
        stroke: true,
        color: '#ff0000',
        font: "16px 'Microsoft Yahei'",
        offsetX: 0,
        offsetY: 0,
    }
}).addTo(map);
```

# Future plans
* Add options to control styling of the labels (including font face)
* Fine tuning of overlap depending on zoom level
* Refactoring...

 