[« Mapping with OpenStreetMap](https://github.com/mapbox/mapping/wiki/Mapping-with-OpenStreetMap)

Think of real world features like streets, rivers, houses and cities. Each feature on OpenStreetMap stems from a real world observation. Observations can be made in ground surveys, through sensors like GPS, from satellite imagery, from photos or they can be copied from third party data. Selecting the _appropriate_ source and translating it _correctly_ into OpenStreetMap is immensely important - it's the definition of great mapping.

*Appropriate sources*

When mapping, it's absolutely important to make sure that the information we add to the map is properly sourced - no matter whether the source is traced like imagery or imported. There's no use at all to add information to the map that we cannot appropriately source. If you're not sure whether a source is fine to add, don't add it.

Here are examples from what sources it is appropriate to add to OpenStreetMap:

- Your firsthand **local knowledge** for instance from a ground survey
- **Satellite imagery** explicitly available to OpenStreetMap for tracing - for example Bing or Mapbox Satellite
- **GPS tracks** explicitly available for OpenStreetMap - for example GPS tracks you collected yourself, or GPS tracks uploaded and available from OpenStreetMap.org 
- **[Mapillary](http://mapillary.com/)** photos 
- **Original information** on web sites such as a store's address on the store's web site
- **Permissively licensed datasets** such as [Wikidata](http://www.wikidata.org/wiki/Wikidata:Main_Page) - a permissive license would be [CC0](https://creativecommons.org/publicdomain/zero/1.0/) or any terms of use that would pass the [open definition](http://opendefinition.org/) _and_ do not require share-alike.

**Do NOT use these sources:**

- Proprietary maps - most paper maps or for example Google Maps, including Google Street View
- Any source data without clear permissive terms
- Whenever you're not sure whether a source is appropriate to use

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
