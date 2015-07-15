[«Guía de OpenStreetMap] (https://github.com/mapbox/data/wiki/OpenStreetMap-Guide)

Esta es una introducción a mapear características del mundo real en OpenStreetMap como calles, edificios, parques, ciudades, cafés y escuelas. Habla de donde se toma la información y cómo se modela en OpenStreetMap. Esta sección se ocupa de los fundamentos de la cartografía.

## Fuentes

La mayoría de los datos de OpenStreetMap o bien es encuestada, trazada a partir de imágenes de satélite o importados de fuentes de terceros.

### Estudios sobre el terreno

Una gran cantidad de datos de OpenStreetMap es original - recogidos por miembros de la comunidad de primera mano. Dicha información se recopila en su mayoría en las encuestas y luego en una etapa distinta cargados en OpenStreetMap con los mismos editores que utilizamos para el mapeo remoto. Estas son las técnicas típicas de la encuesta:

- [Recopilación de rutas GPS](http://wiki.openstreetmap.org/wiki/Recording_GPS_tracks)
- [Recopilar datos con mapas de impresión](http://wiki.openstreetmap.org/wiki/Field_Papers)
- Con ayuda de fotos geolocalizadas por ejemplo a través de [Mapillary](https://www.mapillary.com/osm.html)

Mientras la forma mas facil de empezar es trazar remotamente  imagenes satelitales, los datos de encuesta de campo son altamente valiosos porque son datos de primera mano de lugares mapeados y toma mayor tiempo de recoleccion.

Si bien nuestro enfoque en Mapbox está en mapeo remoto, corremos encuestas sobre el terreno para los entrenamientos del equipo y en los talleres. Recopilación de sus propios datos es divertido y deberías intentarlo. Los datos encuestados en el terreno son muy valiosa ya que es un relato de primera mano del lugar asignado y que se necesita más tiempo para recoger.

![](https://s3.amazonaws.com/f.cl.ly/items/3A232p2m053W3W0m2O3f/Untitled.png)

*Mapping Party con Ônibus Hacker en Río de Janeiro, 2012.*

### Rastreo satelital

La disponibilidad de imágenes satelitales de alta resolución ha permitido que el volumen de datos de OpenStreetMap explote. Es realmente  fácil y rápido entrar en OpenStreetMap y trazar características de las imágenes. En comparación con las encuestas de campo,trazar desde  imágenes de satélite es mucho más rápido. Obviamente, no toda la información se puede trazar a partir de imágenes - nombres de caminos, nombres de lugares, puntos de interés, como las escuelas y cafeterías que no estén visibles a partir de imágenes. De hecho, una gran cantidad de la creación original de datos hoy en OpenStreetMap es una combinación de trazado y encuestas de campo- donde cuanto más posible la información que se traza sea  a partir de imágenes antes que las encuestas de campo agreguen detalles.

![Gifsicle muéstrame el camino](https://s3.amazonaws.com/f.cl.ly/items/2Z081j0E3R452O030o3U/smtw.gif)

### Importaciones de datos de terceros

Hay un gran volumen de datos de terceros disponibles por ahí, en su mayoría de gobierno, sino también de otras fuentes. Si tienen licencia de una manera compatible y de calidad suficiente, que pueden ser utilizados para mejorar el mapa. Las importaciones son generalmente complejas ya que implican fusión con datos de OpenStreetMap existentes y limpieza de datos. Si bien los datos de encuesta de campo y los datos satelitales trazado se pueden agregar a OpenStreetMap sin coordinar con otros miembros de la comunidad, las importaciones  requiere una propuesta formal y una revisión por pares de la comunidad. Un ejemplo para las importaciones son las importaciones de las construcciones y de las direcciones de la Ciudad de Nueva York  que hemos liderado o de la Oficina de Censo [TIGRE datos](http://wiki.openstreetmap.org/wiki/TIGER) que se ha importado en los Estados Unidos . He aquí una animación del progreso [importando edificios en la ciudad de Nueva York](https://www.mapbox.com/blog/nyc-buildings-openstreetmap/):

![Edificios NYC progresan](https://i.imgur.com/2kl2ENl.gif)

### Datos GPS probados 

Ya hemos mencionado la recolección de rutas GPS como una técnica de encuesta de campo. Las grandes cantidades de datos GPS recogidos por ejemplo sistemáticamente de los coches pueden ser utilizados para más que eso. Ellos pueden ser agrupados y procesados para calcular caminos perdidos, carreteras mal alineadas, caminos de una sola via equivocadas, velocidad media y los límites de velocidad. Esta es una técnica bastante avanzada, pero se debe mencionar aquí, ya que no es una importación directa de datos, sino más bien un proceso indirecto de crear un conjunto de datos deducidos que se puede utilizar para mejorar OpenStreetMap.

### Fuentes apropiadas

Cuando se mapea, es absolutamente importante asegurarse de que la información que se añade al mapa esta apropiadamente conseguida - no importa si la fuente se traza como imágenes o importados. No sirve de nada en absoluto agregar información al mapa que no podemos conseguir apropiadamente. Si usted no está seguro que la fuente no es buena para añadir, no lo agregue.

Estos son algunos ejemplos de qué fuentes, es conveniente añadir a OpenStreetMap:

- Su **conocimiento local** de primera mano por ejemplo de una encuesta de campo
- **imágenes satelitales** a trazar explícitamente disponibles en OpenStreetMap  - por ejemplo, Bing o Mapbox Satélite
- **Los trazos GPS** explícitamente disponible para OpenStreetMap - por ejemplo rastreo GPS que has recogido por ud mismo o las rutas GPS disponibles de OpenStreetMap.org
- **[Mapillary](http://mapillary.com/)** photos
- **Informacion Original** en los sitios web, como la dirección de una tienda en el sitio web de la tienda
- **Conjuntos de datos permisivamente licenciados** como [Wikidata](http://www.wikidata.org/wiki/Wikidata:Main_Page)
- una licencia permisiva sería [CC0](https://creativecommons.org/publicdomain/zero/1.0/) o cualquiera de los términos de uso que pasarían la [definición abierta](http://opendefinition.org/) y no requieren   compartir.

**NO utilice estas fuentes:**

- Mapas privados - la mayoría de los mapas de papel o por ejemplo los mapas de Google, incluyendo Google Street View
- Cualquier fuente de datos sin términos claros permisivos
- Cada vez que usted no está seguro si una fuente es apropiado utilizar

## El modelo de datos de OpenStreetMap

OpenStreetMap se compone de tres **elementos** diferentes: *nodos*, *caminos* y *relaciones*. Cada uno de ellos puede tener una o más *etiquetas* dándoles un significado específico. Los nodos son el equivalente a un punto, los caminos son como las líneas que conectan los puntos y las relaciones son colecciones de puntos o caminos que representan un todo más grande. Esto es más fácil de entender con un par de ejemplos.

### Nodos 

Los nodos se utilizan para representar cualquier tipo de caracteristica de punto  o simplemente para designar un nombre para un punto de interés en la vecindad. He aquí un nodo que representa una cafetería:

![cafe](https://s3.amazonaws.com/f.cl.ly/items/2W2k3J2L1N1q1u3I3N0Y/Screen%20Shot%202014-12-16%20at%204.01.44%20PM.png)

y aquí está uno que representa a la ciudad de Nueva York:
    
![nueva york](https://s3.amazonaws.com/f.cl.ly/items/0G3O051s0S1M3s110L2o/Screen%20Shot%202014-12-12%20at%207.15.58%20PM.png)

### Caminos

Un camino es una caracteristica de línea *que conecta dos o más nodos* - como un camino aquí:

![camino con la carretera = residencial y una etiqueta con su nombre, también muestran la manera cómo los nodos en caminos  no tienen una etiqueta](https://s3.amazonaws.com/f.cl.ly/items/1F2r0Y0M1c0m0J1c371G/Screen%20Shot%202014-12-12%20at%207.24.55%20PM.png)

Si cierra un camino - mediante la conexión de su fin a su inicio, puedes mapear caracteristicas de tipo area  como este edificio aquí:
 
![](https://s3.amazonaws.com/f.cl.ly/items/1h190m2u0h3N1Q0Q2o1G/Screen%20Shot%202014-12-12%20at%207.28.47%20PM.png)

o este parque:
 
![](https://s3.amazonaws.com/f.cl.ly/items/2z0E1H041j0W0E1m0R2u/Screen%20Shot%202014-12-12%20at%207.31.44%20PM.png)

Los nodos son por lo general sólo los elementos que definen un camino. Pero nodos que se sientan en un camino pueden tener su propio significado. En este ejemplo, el nodo es parte de la calle 14 y R  y esto también denota que hay un semáforo.

![](https://s3.amazonaws.com/f.cl.ly/items/3V262D3F0h1L3J0V2m3B/trafficlight.gif)

### Etiquetas

Antes de que nos saltemos al tercer elemento al lado de los nodos y formas - relaciones, echemos un vistazo a las etiquetas. Usted los ha visto ahora ya un par de veces en los ejemplos anteriores, como en este nodo de café:

![](https://s3.amazonaws.com/f.cl.ly/items/3h0O2m3Y2c120h1M3p0h/Screen%20Shot%202014-12-16%20at%204.01.44%20PM.png)


Cualquier caracteristica de tipo de punto es un nodo. Ya sea que un nodo designe una cafetería, una escuela, una fuente de incendios, un árbol, un parque, un pico de montaña depende enteramente de cómo se etiqueta el nodo. Cualquier caracteristica de tipo de línea es un camino. Ya sea que el camino sea una carretera, un edificio, un lago, un ferrocarril, un ciclovia es de nuevo, definido por la forma en que se etiqueta.

Las etiquetas pueden estar en cualquier elemento: en nodos, caminos y relaciones.

### Relaciones

Las relaciones se utilizan para organizar múltiples nodos o caminos en un todo más grande. Tome aquí, por ejemplo, la ruta del autobús 23 que corre a través de 3 caminos diferentes.

![autobús](https://s3.amazonaws.com/f.cl.ly/items/2J0m3p1O0W1o1o2P3n0O/relations.gif)

El tipo de relación que  probablemente  lidiarás más  describen un área con agujeros perforados  - uno llamado *multipolígono*. He aquí un ejemplo de un edificio multipolígono con un patio. Consta de 2 caminos cada uno con multiples nodos. Una camino  describe la pared *exterior del edificio*, el otro *la pared interior*. Los caminos son parte de una relación del tipo `type = multipolygon`, la camino exterior tiene la función` outer` y el camino interno tiene la función `inner`. Nota: la etiqueta `edificio=yes` está en la relación (no en el camino).

Su editor de OpenStreetMap se encargará de crear multipolígonos para usted así que no te preocupes si esto parece denso por ahora. Si usted necesita  corregir un multipolígono, esta es una buena sección a regresar.

![Edificio Multipoligono, muestran cómo no hay etiquetas en los nodos y los caminos, sino en la relación] (https://s3.amazonaws.com/f.cl.ly/items/3G292J2S2D310i0t0Q13/multipolygon.gif)

### Lecturas adicionales

Para aprender más sobre la estructura de datos de OpenStreetMap, eche un vistazo a los siguientes recursos:

- Elementos OpenStreetMap http://wiki.openstreetmap.org/wiki/Elements
- Multipolígonos http://wiki.openstreetmap.org/wiki/Relation:multipolygon