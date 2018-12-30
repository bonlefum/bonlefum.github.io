# Rendering maps, presenting geographic data

The wealth of geo-tagged or otherwise location-specific data is extraodinary and consequently gives rise to the desire for methods to rapidly present and interact with such data.

## Show a map, with custom setup

This basic javascript + html tool looks very clean, being able to add layers onto google maps: [jhawes@codepen](https://codepen.io/jhawes/pen/ujdgK)

Unfortunately, trying to repurpose this, we discover that the google api has become more fussy and requires users to sign up (complete with credit card) to obtain an API key and use the maps.

On codepen a key doesn't seem to be needed, but elsewhere (including a local
session) without a key, the session will serve up greyed-out tiles with a "development" label; moreover, the pages produce a popup "this page can't load maps". 

## Can we switch to openmaps?

[OSM wiki example](https://wiki.openstreetmap.org/wiki/Google_Maps_Example)

The idea here is to use the google JS api, but present OSM tiles.

This renders tiles ok, but still generates that annoying popup on initial load.

## Other OSM options

Leaflet is a nice library that interfaces cleanly to openstreetmap data layers;
it seems to be quite easy to get up and running.

* Here are some [syles available via leafletjs](http://leaflet-extras.github.io/leaflet-providers/preview/)

* need to have an access key for certain providers, e.g. [mapbox](www.mapbox.com)
* that opens up issues about keeping the key secret... There are various ways to solve that, e.g. 
  [blog post](https://blog.alexellis.io/swarm-secrets-in-action/)
  [example docker](https://github.com/docker-library/ghost/issues/125#issuecomment-401516088)
  [example "safe"](https://github.com/StackExchange/blackbox)

* But a different workaround is instead to switch tile provider, to one whose access is not based on keys. [Big list](https://wiki.openstreetmap.org/wiki/Tiles#Servers) here, including one nice choice, [stamen](maps.stamen.com/).  Just playing here but commercial use would need more attention to licensing. 



# Adding novel data.

Now that the basic underlying map is presented (in one or more layers), how do we go about adding data, and can we do this in an interactive way? 


## Data sources

* geojson format
* shp files
* converting one to the other...


# What next?

* toggling between different map providers
* presenting different layers by selection
* 






