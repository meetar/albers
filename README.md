# albers

This map applies dynamic [Albers equal-area conic projection](https://en.wikipedia.org/wiki/Albers_projection) to the Mapzen vector tiles, using the Tangram JavaScript mapping library.

Usually, an Albers map is specified with a particular center, and one or two "standard parallels", which are lines of latitude which have no shape distortion – this map adjusts all of these parameters with the movement of the map, using a vertex shader inside the scene.yaml file.

I've left the tile borders visible so the distortion is more obvious here.

Live demo: http://meetar.github.io/albers/

![usa](https://cloud.githubusercontent.com/assets/459970/10209464/83f25b72-67a9-11e5-95d6-ba116b966d04.jpg)

