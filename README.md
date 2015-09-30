# albers

This map applies a dynamic [Albers equal-area conic projection](https://en.wikipedia.org/wiki/Albers_projection) to the Mapzen vector tiles, using the Tangram JavaScript mapping library.

The Mapzen tiles are first converted from [Web Mercator](https://en.wikipedia.org/wiki/Web_Mercator) to spherical lat/lng coordinates, and then reprojected into Albers.

Usually, a [conic projection](https://en.wikipedia.org/wiki/Map_projection#Conic) is specified with a specific center and two "standard parallels", which are lines of latitude with no distortion – this map adjusts all of these parameters in real time with the movement of the map, using a vertex shader inside the scene.yaml file.

I've left the edges of the loaded tiles visible so the map's behavior is more obvious.

Live demo: http://meetar.github.io/albers/

![usa](https://cloud.githubusercontent.com/assets/459970/10209464/83f25b72-67a9-11e5-95d6-ba116b966d04.jpg)

