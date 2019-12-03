# albers

This map applies a dynamic [Albers equal-area conic projection](https://en.wikipedia.org/wiki/Albers_projection) to the Mapzen vector tiles, using the [Tangram](http://mapzen.com/tangram) mapping library.

The Mapzen tiles are first converted from [Web Mercator](https://en.wikipedia.org/wiki/Web_Mercator) to spherical lat/lng coordinates, and then reprojected into Albers.

[Conic projections](https://en.wikipedia.org/wiki/Map_projection#Conic) are specified with a center and two "standard parallels", which are lines of latitude with no distortion - it may be useful to think of these as the intersections of the conic projection with the "sphere" of the earth:

![cone-sphere-intersectionl](https://user-images.githubusercontent.com/459970/70007000-c583a880-1523-11ea-9838-806ac04e3ab6.gif)

This map's code adjusts these two standard parallel parameters in real time with the movement of the map, using a vertex shader inside the scene.yaml file.

I've left the edges of the loaded tiles visible so the map's behavior is more obvious.

Live demo: http://meetar.github.io/albers/

The code for this demo may be found in [scene.yaml](scene.yaml) – this file contains all the styling and projection code in a single scene. Another way to set this up would be to make styles which allow a projection to be imported separately – an example of this setup may be seen in the [base.yaml](base.yaml) and [albers.yaml](albers.yaml) files.

![usa](https://cloud.githubusercontent.com/assets/459970/10209464/83f25b72-67a9-11e5-95d6-ba116b966d04.jpg)

