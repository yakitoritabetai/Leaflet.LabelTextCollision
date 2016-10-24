# Leaflet.LabelTextCollision
Leaflet.LabelTextCollision is a plug-in to display without colliding labels to leaflet.

Supports Leaflet 1.0.0+ branches.

To avoid the label of overlap. Rather than the relocation of the label, it does the preferentially displayed on the data order, overlapping place hides.

That label you want to display preferentially should be arranged in ascending order.

# demo
Check out the <a href="https://yakitoritabetai.github.io/Leaflet.LabelTextCollision/">demo</a>


# Usage examples
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

# Future plans
* The font of the label to the variable.
* To control the overlap depending on the zoom level.
* Refactoring...

# License
Copyright (c) 2016 Kenta Hakoishi
Released under the MIT license

However, "copyright notice" should be indicated on the place where the user is visible.

ただし、「著作権表示」はユーザが見える箇所に表記して下さい。
