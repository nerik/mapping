[« Mapping with OpenStreetMap](https://github.com/mapbox/mapping/wiki/Mapping-with-OpenStreetMap)

In OpenStreetMap, each feature is described as one or more geometries (think for instance of a river's shape) with attached attribute data (think of the river's name). Geometries are described with three different *elements*: *nodes*, *ways* and *relations*. Attributes are described as *tags* that can be part of a node, a way or a relation.

Nodes are the equivalent of a point, ways are like lines that connect points and relations are collections of points or ways that represent a larger whole. This is easiest to understand with a couple of examples.

### Nodes

Nodes are used to represent any kind of point type feature or just to designate a name for a point of interest in the vicinity. Here's a node representing a café:

![cafe](https://s3.amazonaws.com/f.cl.ly/items/2W2k3J2L1N1q1u3I3N0Y/Screen%20Shot%202014-12-16%20at%204.01.44%20PM.png)

and here's one representing New York City:
    
![new york](https://s3.amazonaws.com/f.cl.ly/items/0G3O051s0S1M3s110L2o/Screen%20Shot%202014-12-12%20at%207.15.58%20PM.png)

### Ways

A way is a line feature *connecting two or more nodes* - like a road here:

![way with highway=residential and a name tag, also show how nodes on way don't have a tag](https://s3.amazonaws.com/f.cl.ly/items/1F2r0Y0M1c0m0J1c371G/Screen%20Shot%202014-12-12%20at%207.24.55%20PM.png)

If you close a way - by connecting its end to its start, you can map area type features like this building here:
 
![](https://s3.amazonaws.com/f.cl.ly/items/1h190m2u0h3N1Q0Q2o1G/Screen%20Shot%202014-12-12%20at%207.28.47%20PM.png)

or this park:
 
![](https://s3.amazonaws.com/f.cl.ly/items/2z0E1H041j0W0E1m0R2u/Screen%20Shot%202014-12-12%20at%207.31.44%20PM.png)

Nodes are usually just the items that define a way. But nodes sitting on a way can have their own significance. In this example the node is part of 14th Street and R Street and it also denotes that there's a traffic light.

![](https://s3.amazonaws.com/f.cl.ly/items/3V262D3F0h1L3J0V2m3B/trafficlight.gif)

### Tags

Before we hop to the third element next to nodes and ways - relations, let's look at tags. You've seen them now already a couple of times in the examples above, like in this café node:

![](https://s3.amazonaws.com/f.cl.ly/items/3h0O2m3Y2c120h1M3p0h/Screen%20Shot%202014-12-16%20at%204.01.44%20PM.png)


Any point type feature is a node. Whether the node designates a café, a school, a fire hydrant, a tree, a park, a mountainpeak is entirely up to how the node is tagged. Any line type feature is a way. Whether the way is a road, a building, a lake, a railway, a cycleway is again, defined by how it is tagged.

Tags can be on any element: on nodes, ways and relations.

### Relations

Relations are used to organize multiple nodes or ways into a larger whole. Take here for instance the bus route 23 running through 3 different ways.

![bus route](https://s3.amazonaws.com/f.cl.ly/items/2J0m3p1O0W1o1o2P3n0O/relations.gif)

The type of relation that you'll probably deal most with describes an area with punched out holes - a so called *multipolygon*.  Here is an example of a multipolygon building with a yard. It consists of 2 ways with each multiple nodes. One way describes the *outer* wall of the building, the other one the *inner* wall. The ways are part of a relation of the type `type=multipolygon`, the outer way has the role `outer` and the and the inner way has the role `inner`. Note: the `building=yes` tag is on the relation (not on the way).

Your OpenStreetMap editor will take care of creating multipolygons for you so don't worry if this seems dense for now. If you need to fix a multipolygon, this is a good section to come back though.

![Multipolygon building, show how there are no tags on the nodes and ways, but on the relation](https://s3.amazonaws.com/f.cl.ly/items/3G292J2S2D310i0t0Q13/multipolygon.gif)

### Further reading

To learn more about the OpenStreetMap data structure, take a look at these resources:

- OpenStreetMap Elements http://wiki.openstreetmap.org/wiki/Elements
- Multipolygons http://wiki.openstreetmap.org/wiki/Relation:multipolygon
