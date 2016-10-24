# Leaflet.LabelTextCollision
Leaflet.LabelTextCollision is a plug-in to display without colliding labels to leaflet.

Supports Leaflet 1.0.0+ branches.

To avoid the label of overlap. Rather than the relocation of the label, it does the preferentially displayed on the data order, overlapping place hides.
That label you want to display preferentially should be arranged in ascending order.

L.LabelTextCollision has drawn inherit the L.Canvas.
This is because the case the text is conflict because overlays item is large and browser becomes heavy.

# demo
Check out the <a href="https://yakitoritabetai.github.io/Leaflet.LabelTextCollision/">demo</a>


# Usage examples
* The value of the Map State Options renderer to set this plug-in (L.LabelTextCollision).

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

* Overlays (Polygon, Polyline, Circle) to add the text to the option, to set the string you want to display as a label.
  * Of course it can not be sure that there is enough space for text do not overlap.

```
L.polyline(
  [ [ 35.695786, 139.749213 ],
          [ 35.696786, 139.748213 ],
          [ 35.695786, 139.747213 ] ], {
      weight : 12,
      color : '#fe57a1',
      text : 'Leaflet.LabelTextCollision!!!!!!!!'
  }).addTo(map);
```

# Future plans
* The font of the label to the variable.
* To control the overlap depending on the zoom level.
* Refactoring...

# License
Copyright (c) 2016 Kenta Hakoishi
Released under the MIT license

However, "copyright notice" should be indicated on the place where the user is visible.

ただし、「著作権表示」はユーザが見える箇所に表記して下さい。
