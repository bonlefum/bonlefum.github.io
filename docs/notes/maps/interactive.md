# Rendering maps, presenting geographic data

The wealth of geo-tagged or otherwise location-specific data is extraodinary and consequently gives rise to the desire for methods to rapidly present and interact with such data.

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

* need to have an access key for certain providers, e.g. [mapbox](www.mapbox.com)
* that opens up issues about keeping the key secret... There are various ways to solve that, e.g. 
  https://blog.alexellis.io/swarm-secrets-in-action/
  https://github.com/docker-library/ghost/issues/125#issuecomment-401516088
  https://github.com/StackExchange/blackbox










