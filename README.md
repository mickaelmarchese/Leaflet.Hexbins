# Leaflet.Hexbins

This plugin provides fully customizable Hexagonal Binning functionality for Leaflet, a JS library for interactive maps.

It requires Leaflet, D3.hexbin and D3.scale.

![](/img/hexbins_illustration.png)

Two new functions are provided:
* `L.hexagon`: an extension of L.Polygon that allows creating a simple hexagon by specifying the position of its center and its radius in pixels
* `L.hexbins`: an Layer group that automatically calculate hexagonal binning of a set of coordinates and create an L.hexagon for each bin.

## Using the plugin
Download Leaflet.hexbins.js and include it in your HTML page.

To use `L.hexbins`, include D3-hexbin (https://d3js.org/d3-hexbin.v0.2.min.js) and D3-scale (https://d3js.org/d3-scale.v3.min.js) as well.

### Demo
Find a live demo here.


### Usage examples

To create a new hexagon, use:
```javascript
L.hexagon([200,200]).addTo(map); // position in pixels
L.hexagon(L.LatLng([46.954825, 0.603445])).addTo(map); //position in Lat,Long
```


To create a new hexagonal binning, use:
```javascript
L.hexbins([[46.952134, 0.604905],[ 46.954825, 0.603445],…]).addTo(map); 
```

## L.hexagon reference
A class for drawing hexagons overlays on a map. Extends Polygon.

### Creation
Factory | Description
------------ | -------------
L.hexagon(\<LatLng \| Number[] \| Point> center, \<Polyline options> options?)  | Center can be either  an array [x,y] in pixels, or a \<Point> or a \<LatLng>

### Options
Option | Type | 	Default | Description
------------ | ------------- | ------------- | -------------
radius | Number | 10 | The radius of the hexagon in pixels.
 



