# Geometric.js
A JavaScript library with geometric functions. [See a live demo](https://bl.ocks.org/harrystevens/c4eddfb97535e8e01643325cb43175ff).

[![Build Status](https://travis-ci.org/HarryStevens/geometric.svg?branch=master)](https://travis-ci.org/HarryStevens/geometric)

## Installation

### Web browser
In vanilla, a `geometric` global is exported. You can use the latest version from unpkg.
```html
<script src="https://unpkg.com/geometric@0.0.15/build/geometric.js"></script>
<script src="https://unpkg.com/geometric@0.0.15/build/geometric.min.js"></script>
```
If you'd rather host it yourself, download the latest release from the [`build` directory](https://github.com/HarryStevens/geometric/tree/master/build).

### npm

```bash
npm i geometric -S
```
```js
var geometric = require("geometric");
```

## API

In Geometric.js, there are <b>points</b>, <b>lines</b>, <b>polygons</b>, <b>angles</b>, and <b>distances</b>.
* <b>Points</b> are represented as arrays of two numbers, such as [0, 0].
* <b>Lines</b> are represented as arrays of two points, such as [[0, 0], [1, 0]].
* <b>Polygons</b> are represented as arrays of vertices, each of which is a point, such as [[0, 0], [1, 0], [1, 1], [0, 1]].
* <b>Angles</b>, <b>areas</b> and <b>distances</b> are represented as numbers. Angles are measured in [degrees](https://en.wikipedia.org/wiki/Degree_(angle)) or [radians](https://en.wikipedia.org/wiki/Radian), depending upon the function, while areas and distances are measured in pixels.

<hr />

<a name="angleDegrees" href="#angleDegrees">#</a> geometric.<b>angleDegrees</b>(<em>pointA</em>, <em>pointB</em>) [<>](https://github.com/HarryStevens/geometric/blob/master/src/angleDegrees.js "Source")

Returns the angle between <em>pointA</em> and <em>pointB</em> in degrees. [See it in action](https://bl.ocks.org/harrystevens/b212d3166a85aecb9d5fc61cf660de23).

<a name="angleRadians" href="#angleRadians">#</a> geometric.<b>angleRadians</b>(<em>pointA</em>, <em>pointB</em>) [<>](https://github.com/HarryStevens/geometric/blob/master/src/angleRadians.js "Source")

Returns the angle between <em>pointA</em> and <em>pointB</em> in radians.

<a name="area" href="#area">#</a> geometric.<b>area</b>(<em>polygon</em>) [<>](https://github.com/HarryStevens/geometric/blob/master/src/area.js "Source")

Returns the area of a <em>polygon</em>. [See it in action](https://bl.ocks.org/harrystevens/37287b23b345f394f8276dc87a9c2bc6).

<a name="centroid" href="#centroid">#</a> geometric.<b>centroid</b>(<em>polygon</em>) [<>](https://github.com/HarryStevens/geometric/blob/master/src/centroid.js "Source")

Returns the weighted centroid of a <em>polygon</em>. Not to be [confused](https://github.com/Turfjs/turf/issues/334) with a mean center. [See it in action](https://bl.ocks.org/harrystevens/37287b23b345f394f8276dc87a9c2bc6).

<a name="convexHull" href="#convexHull">#</a> geometric.<b>convexHull</b>(<em>points</em>) [<>](https://github.com/HarryStevens/geometric/blob/master/src/convexHull.js "Source")

Returns the convex hull, represented as a <em>polygon</em> of an array of <em>point</em>s using [Andrew’s monotone chain algorithm](https://en.wikibooks.org/wiki/Algorithm_Implementation/Geometry/Convex_hull/Monotone_chain#JavaScript). Returns null if the input array contains fewer than three points.

<a name="distance" href="#distance">#</a> geometric.<b>distance</b>(<em>pointA</em>, <em>pointB</em>) [<>](https://github.com/HarryStevens/geometric/blob/master/src/distance.js "Source")

Returns the distance between <em>pointA</em> and <em>pointB</em>. [See it in action](https://bl.ocks.org/harrystevens/c4eddfb97535e8e01643325cb43175ff).

<a name="meanCenter" href="#meanCenter">#</a> geometric.<b>meanCenter</b>(<em>polygon</em>) [<>](https://github.com/HarryStevens/geometric/blob/master/src/meanCenter.js "Source")

Returns the arithmetic mean of the vertices of a polygon. Not to be [confused](https://github.com/Turfjs/turf/issues/334) with a centroid. [See it in action](https://bl.ocks.org/harrystevens/37287b23b345f394f8276dc87a9c2bc6).

<a name="midpoint" href="#midpoint">#</a> geometric.<b>midpoint</b>(<em>pointA</em>, <em>pointB</em>) [<>](https://github.com/HarryStevens/geometric/blob/master/src/midpoint.js "Source")

Returns the midpoint between <em>pointA</em> and <em>pointB</em>. [See it in action](https://bl.ocks.org/harrystevens/c4eddfb97535e8e01643325cb43175ff).

<a name="pointInPolygon" href="#pointInPolygon">#</a> geometric.<b>pointInPolygon</b>(<em>point</em>, <em>polygon</em>) [<>](https://github.com/HarryStevens/geometric/blob/master/src/pointInPolygon.js "Source")

Returns a boolean representing whether a <em>point</em> is inside of a <em>polygon</em>. Uses [ray casting](https://en.wikipedia.org/wiki/Point_in_polygon#Ray_casting_algorithm).

<a name="pointLeftOfLine" href="#pointLeftOfLine">#</a> geometric.<b>pointLeftOfLine</b>(<em>point</em>, <em>line</em>) [<>](https://github.com/HarryStevens/geometric/blob/master/src/pointOnLine.js#L8 "Source")

Returns a boolean representing whether a <em>point</em> is to the left of a <em>line</em>. [See it in action](https://bl.ocks.org/HarryStevens/e6b53f48aff3a2bea1f99604cde1a99f).

<a name="pointOnLine" href="#pointOnLine">#</a> geometric.<b>pointOnLine</b>(<em>point</em>, <em>line</em>) [<>](https://github.com/HarryStevens/geometric/blob/master/src/pointOnLine.js#L16 "Source")

Returns a boolean representing whether a <em>point</em> is collinear with a <em>line</em>.

<a name="pointRightOfLine" href="#pointRightOfLine">#</a> geometric.<b>pointRightOfLine</b>(<em>point</em>, <em>line</em>) [<>](https://github.com/HarryStevens/geometric/blob/master/src/pointOnLine.js#L12 "Source")

Returns a boolean representing whether a <em>point</em> is to the right of a <em>line</em>. [See it in action](https://bl.ocks.org/HarryStevens/e6b53f48aff3a2bea1f99604cde1a99f).

<a name="polygonInPolygon" href="#polygonInPolygon">#</a> geometric.<b>polygonInPolygon</b>(<em>polygonA</em>, <em>polygonB</em>) [<>](https://github.com/HarryStevens/geometric/blob/master/src/polygonInPolygon.js "Source")

Returns a boolean representing whether <em>polygonA</em> is contained by <em>polygonB</em>.

<a name="polygonsIntersect" href="#polygonsIntersect">#</a> geometric.<b>polygonsIntersect</b>(<em>polygonA</em>, <em>polygonB</em>) [<>](https://github.com/HarryStevens/geometric/blob/master/src/pointsIntersect.js "Source")

Returns a boolean representing whether <em>polygonA</em> intersects but is not contained by <em>polygonB</em>.

<a name="rotateDegrees" href="#rotateDegrees">#</a> geometric.<b>rotateDegrees</b>(<em>point</em>, <em>angle</em>[, <em>origin</em>]) [<>](https://github.com/HarryStevens/geometric/blob/master/src/rotateDegrees.js "Source")

Returns the coordinates resulting from rotating a <em>point</em> about an origin by an <em>angle</em> in degrees. If <em>origin</em> is not specified, the origin is set to [0, 0]. [See it in action](https://bl.ocks.org/harrystevens/5fe49df19892c04dfb9883c217571409).

<a name="rotateRadians" href="#rotateRadians">#</a> geometric.<b>rotateRadians</b>(<em>point</em>, <em>angle</em>[, <em>origin</em>]) [<>](https://github.com/HarryStevens/geometric/blob/master/src/rotateRadians.js "Source")

Returns the coordinates resulting from rotating a <em>point</em> about an origin by an <em>angle</em> in radians. If <em>origin</em> is not specified, the origin is set to [0, 0].

<a name="translateDegrees" href="#translateDegrees">#</a> geometric.<b>translateDegrees</b>(<em>point</em>, <em>angle</em>, <em>distance</em>) [<>](https://github.com/HarryStevens/geometric/blob/master/src/translateDegrees.js "Source")

Returns the coordinates resulting from translating a point by an <em>angle</em> in degrees and a <em>distance</em>. [See it in action](https://bl.ocks.org/harrystevens/c4eddfb97535e8e01643325cb43175ff).

<a name="translateRadians" href="#translateRadians">#</a> geometric.<b>translateRadians</b>(<em>point</em>, <em>angle</em>, <em>distance</em>) [<>](https://github.com/HarryStevens/geometric/blob/master/src/translateRadians.js "Source")

Returns the coordinates resulting from translating a point by an <em>angle</em> in radians and a <em>distance</em>.