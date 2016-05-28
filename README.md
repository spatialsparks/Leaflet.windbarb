# Leaflet.windbarb
A small Leaflet plugin to generate wind barbs / wind arrows

Leaflet.idw generates wind barbs according to the wind barb standard shown [here] (https://commons.wikimedia.org/wiki/Wind_speed).

Demos
* [Example](http://www.geonet.ch/leaflet-windbarb/) *(Mobile: Working on Samsung Galaxy s4)*
    
Examples
![Image of wind barbs](https://github.com/JoranBeaufort/Leaflet.windbarb/blob/master/example/example.png)


#### Basic Usage

```
var icon = L.WindBarb.icon({deg: 90, speed: 20, pointRadius: 5, strokeLength: 20});
var marker = L.marker([lat,long], {icon: icon}).addTo(map);

```

To include the plugin, just use leaflet-windbarb.js from the src folder:

```<script src="leaflet-windbarb.js"></script>```

#### Options

Generates a wind barb / wind arrow icon with the following options:

    pointRadius - Radius of point in the middle; Default = 8,
    strokeWidth - Stroke width; Default = 2,
    strokeLength - Length of the main stroke, to which the barbs are connected; Default = 15,
    barbSpaceing - Spacing between the barbs; Default = 5,
    barbHeight - Height of 10kn adn 50kn barbs, 5kn barbs will be 50%; Default = 15
            
#### Changelog


0.0.1 — May 28, 2016

    Initial release.
