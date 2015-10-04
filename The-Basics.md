[« Mapping with OpenStreetMap](https://github.com/mapbox/mapping/wiki/Mapping-with-OpenStreetMap)

This section is about where OpenStreetMap data is from (Sources) and how it is modeled in OpenStreetMap (The OpenStreetMap Data Model).

Consider a *feature* a real world entity like a road, a river, a house or a city. Each feature on OpenStreetMap stems from a real world observation. Observations can be made in ground surveys, through sensors like GPS, from satellite imagery, from photos or they can be copied from third party data. Once in OpenStreetMap, each feature is described as one or more geometries (think for instance of a river's shape) with attached attribute data (think of the river's name). Geometries are described as nodes, ways and relations and attributes are described as tags that can be part of a node, a way or a relation.

## Sources

Most OpenStreetMap data is either surveyed, traced from Satellite imagery or imported from third party sources.

### Ground Surveys

A lot of OpenStreetMap data is original - collected by community members first hand. This data is mostly gathered in surveys and then in a separate step entered into OpenStreetMap with the same editors we use for remote mapping. Here are typical survey techniques:

- [collecting GPS tracks](http://wiki.openstreetmap.org/wiki/Recording_GPS_tracks)
- [collect data with print maps](http://wiki.openstreetmap.org/wiki/Field_Papers)
- using geolocated photos for instance through [Mapillary](https://www.mapillary.com/osm.html)

While the easiest way to get started is to trace remotely off satellite imagery, ground surveyed data is highly valuable as it's a first hand account from the mapped place and it takes longest to collect.

![](https://s3.amazonaws.com/f.cl.ly/items/3A232p2m053W3W0m2O3f/Untitled.png)

*Mapping party with Ônibus Hacker in Rio de Janeiro, 2012.*

### Satellite tracing

The availability of high resolution satellite imagery has allowed OpenStreetMap's data volume to explode. It's really easy and fast to go into OpenStreetMap and trace features from imagery. Compared to ground surveys, tracing from satellite imagery is much faster. Obviously, not all information can be traced from imagery - road names, place names, points of interests like schools and cafés aren't visibile from imagery. In fact, a lot of original data creation today in OpenStreetMap is a combination of tracing and surveying - where as much as possible information is traced from imagery before subsequent ground surveys add detail. 

![Gifsicle show me the way](https://s3.amazonaws.com/f.cl.ly/items/2Z081j0E3R452O030o3U/smtw.gif)

### Imports of third party data

There is a large volume of third party data available out there, mostly from government but also other sources. If they are licensed in a compatible way and of high enough quality, they can be used to improve the map. Imports are usually complex as they involve conflation with existing OpenStreetMap data and data cleaning. While ground survey data and satellite traced data can be added to OpenStreetMap without coordinating with other community members, imports do require a formal proposal and a community peer review. An example for imports are the New York City building and address import that we've led or the US Census Bureau [TIGER data](http://wiki.openstreetmap.org/wiki/TIGER) that has been imported in the United States. Here's an animation of the progress [importing buildings in New York City](https://www.mapbox.com/blog/nyc-buildings-openstreetmap/):

![NYC buildings progress](https://i.imgur.com/2kl2ENl.gif)

### GPS probe data

We've already mentioned collecting GPS tracks as a ground surveying techniques. Large bodies of GPS data collected for instance systematically from cars can be used for more than that. They can be bundled and processed to compute missing roads, misaligned roads, wrong oneways, average speed and speed limits. This is a fairly advanced technique but it should be mentioned here as it's not a direct data import but rather an indirect process of creating a derived data set that can be used to improve OpenStreetMap.

### Appropriate sources

When mapping, it's absolutely important to make sure that the information we add to the map is properly sourced - no matter whether the source is traced like imagery or imported. There's no use at all to add information to the map that we cannot appropriately source. If you're not sure whether a source is fine to add, don't add it.

Here are examples from what sources it is appropriate to add to OpenStreetMap:

- Your firsthand **local knowledge** for instance from a ground survey
- **Satellite imagery** explicitly available to OpenStreetMap for tracing - for example Bing or Mapbox Satellite
- **GPS tracks** explicitly available for OpenStreetMap - for example GPS tracks you collected yourself or the GPS tracks available from OpenStreetMap.org 
- **[Mapillary](http://mapillary.com/)** photos 
- **Original information** on web sites such as a store's address on the store's web site
- **Permissively licensed datasets** such as [Wikidata](http://www.wikidata.org/wiki/Wikidata:Main_Page) - a permissive license would be [CC0](https://creativecommons.org/publicdomain/zero/1.0/) or any terms of use that would pass the [open definition](http://opendefinition.org/) _and_ do not require share-alike.

**Do NOT use these sources:**

- Proprietary maps - most paper maps or for example Google Maps, including Google Street View
- Any source data without clear permissive terms
- Whenever you're not sure whether a source is appropriate to use

## The OpenStreetMap Data Model

OpenStreetMap is made up of three different *elements*: *nodes*, *ways* and *relations*. Each of them can have one or more *tags* giving them some specific significance. Nodes are the equivalent of a point, ways are like lines that connect points and relations are collections of points or ways that represent a larger whole. This is easiest to understand with a couple of examples.

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
