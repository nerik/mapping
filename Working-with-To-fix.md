[To-fix](http://osmlab.github.io/to-fix/) is a QA tool and tasking manager for OpenStreetMap. Systematic issues in the map geometries and inconsistent tags are processed regularly and loaded into to-fix as simple tasks that can be quickly cycled through and corrected by mappers if possible.

#### Tasks
- Unconnected major: Unconnected geometries in motorable roads
- Unconnected minor: Unconnected geometries in paths and tracks
- Impossible oneway: Oneways with no corresponding entry or exit
- Broken polygons: Unclosed areas
- Highway intersects highway: Highways that overlap without an intersection
- Highway intersects water: Highways that overlap with water features without an intersection

#### Settings
- After signing in using your OSM id, you can configure the OSM editor to use. It is recommended to use JOSM.
- If using JOSM, try the [to-fix josm plugin]() for direct editor integration.

#### Instructions
* Once an area has been improved on OSM, mark the issue as Fixed to remove it from the queue
* If you feel the area is unclear and would like a different issue, hit Skip
* You can also add a note to get clarity from contributors on the ground
* If the issue was incorrectly marked as an error, hit Not an error to remove it from the queue



## Fixing common issues
### Impossible oneways
Incorrectly tagged oneways and direction can break routing if it results in a oneway trap from where it is not possible to exit to the main road network.

**Reverse incorrect oneway**
Verify the direction from the cars or road marking from the imagery and reverse the one way
![untitled](https://cloud.githubusercontent.com/assets/126868/8327474/5b4d587c-1a86-11e5-9831-f93172b6d1e9.gif)