# Leaflet.windbarb
A small Leaflet plugin to generate wind barbs / wind arrows

Leaflet.idw generates wind barbs according to the wind barb standard shown [here] (https://commons.wikimedia.org/wiki/Wind_speed).

### Requirements
This plugin needs Leaflet version v1.0.0beta2 or above.

Demos
* [Example](http://www.geonet.ch/leaflet-windbarb/) *(Mobile: Working on Samsung Galaxy s4)*
    
Examples

![Image of wind barbs](https://github.com/JoranBeaufort/Leaflet.windbarb/blob/master/example/example.png)

Example of changed colour (Kudos Rickyars):

![Image of wind barbs with colour change](https://github.com/JoranBeaufort/Leaflet.windbarb/blob/master/example/example%20colour.png)

#### Basic Usage

```
var icon = L.WindBarb.icon({lat: 40, deg: 90, speed: 20, pointRadius: 5, strokeLength: 20});
var marker = L.marker([lat,long], {icon: icon}).addTo(map);

```

#### Example of how to mirror velocity indication on southern hemisphere
```
            if(latitude<0){
              var icon = L.WindBarb.icon({mirrorVel: true, deg: p[3], speed: p[2]});  
            }else{
              var icon = L.WindBarb.icon({lat: p[0], deg: p[3], speed: p[2]});
            }
```
            
* The lat is used to see if point is on north or south hemisphere

To include the plugin, just use leaflet-windbarb.js from the src folder:

```<script src="leaflet-windbarb.js"></script>```

#### Options

Generates a wind barb / wind arrow icon with the following options:

    pointRadius - Radius of point in the middle; Default = 8
    strokeWidth - Stroke width; Default = 2
    strokeLength - Length of the main stroke, to which the barbs are connected; Default = 15
    barbSpaceing - Spacing between the barbs; Default = 5
    barbHeight - Height of 10kn adn 50kn barbs, 5kn barbs will be 50%; Default = 15
    forceDir - If set to "true" the direction will always be shown, even if speed < 2.5kn; Default = false
    fillColor - Set the fill colour of the circle - Default = #2B85C7 (Thanks  Rickyars (https://github.com/rickyars))
    mirrorVel - mirrors velocity indication; default = false        
#### Changelog

0.0.5 - March 30, 2017

    Velocity indication should always point to equator

0.0.4 - March 30, 2017

    Rickyars kindly added option to change fill colour

0.0.3 - January 30, 2017
    
    Updated to current Leaflet version (1.0.3). Fixed marker offset issue.
    
0.0.1 — May 28, 2016

    Initial release.
