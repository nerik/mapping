Here is a quick-intro to what you need to know about tagging places, condensed from various pages on the OSM wiki and postings to the mailing list. For further information consult [taginfo](http://taginfo.openstreetmap.org/).

Top-level places:

- __place=city__: Typically has a population of over 100,000. If you are mapping a city, please take a minute to check if its population tag is present and accurate. We use population as part of the label priority logic in the stylesheet.
- __place=town__: Rough population range of 10,000 to 100,000, or smaller/less important than the cities in the area.
- __place=village__: Rough population range of 1,000 to 10,000, or smaller/less important than the towns in the area.
- __place=hamlet__: Rough population of (well) under 1,000. Usually rural.

Places-within-places:

- __place=suburb__: For neighborhoods in cities, or large neighborhoods/sectors within towns. Note that this tag has little to do with the common North American concept of suburbia and is perfectly acceptable within a city center.
- __place=neighbourhood__: For small neighborhoods within cities (including neighborhoods within neighborhoods), or neighborhoods within towns. Note the non-American spelling.
- __place=hamlet__: This should generally not be used as a place within a larger city or town, but it still happens a lot. It's likely that something tagged place=hamlet within a city or a town should be tagged as a suburb or neighborhood instead. Thanks to imports, some apartment buildings or housing complexes are also tagged as hamlets. They should be converted to landuse=residential unless they are rather large, in which case leaving them as a hamlet is fine.
- __landuse=residential__: For apartment buildings, apartment complexes, or groups of houses. Can be an area or a node, and combined with a name tag if applicable.