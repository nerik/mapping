[« Guía: Mapeo con OpenStreetMap](https://github.com/mapbox/mapping/wiki/Mapeo-con-OpenStreetMap)

La mayoría de los datos de OpenStreetMap o bien es encuestada, trazada a partir de imágenes de satélite o importados de fuentes de terceros.

### Estudios sobre el terreno

Una gran cantidad de datos de OpenStreetMap es original - recogidos por miembros de la comunidad de primera mano. Dicha información se recopila en su mayoría en las encuestas y luego en una etapa distinta cargados en OpenStreetMap con los mismos editores que utilizamos para el mapeo remoto. Estas son las técnicas típicas de la encuesta:

- [Recopilación de rutas GPS](http://wiki.openstreetmap.org/wiki/Recording_GPS_tracks)
- [Recopilar datos con mapas de impresión](http://wiki.openstreetmap.org/wiki/Field_Papers)
- Con ayuda de fotos geolocalizadas por ejemplo a través de [Mapillary](https://www.mapillary.com/osm.html)

Mientras la forma mas facil de empezar es trazar remotamente  imagenes satelitales, los datos de encuesta de campo son altamente valiosos porque son datos de primera mano de lugares mapeados y toma mayor tiempo de recoleccion.

Si bien nuestro enfoque en Mapbox está en mapeo remoto, corremos encuestas sobre el terreno para los entrenamientos del equipo y en los talleres. Recopilación de sus propios datos es divertido y deberías intentarlo. Los datos encuestados en el terreno son muy valiosos ya que es un relato de primera mano del lugar asignado y que se necesita más tiempo para recoger.

![](https://s3.amazonaws.com/f.cl.ly/items/3A232p2m053W3W0m2O3f/Untitled.png)

*Mapping Party con Ônibus Hacker en Río de Janeiro, 2012.*

### Rastreo satelital

La disponibilidad de imágenes satelitales de alta resolución ha permitido que el volumen de datos de OpenStreetMap explote. Es realmente  fácil y rápido entrar en OpenStreetMap y trazar características de las imágenes. En comparación con las encuestas de campo,trazar desde  imágenes de satélite es mucho más rápido. Obviamente, no toda la información se puede trazar a partir de imágenes - nombres de caminos, nombres de lugares, puntos de interés, como las escuelas y cafeterías que no estén visibles a partir de imágenes. De hecho, una gran cantidad de la creación original de datos hoy en OpenStreetMap es una combinación de trazado y encuestas de campo- donde cuanto más posible la información que se traza sea  a partir de imágenes antes que las encuestas de campo agreguen detalles.

![Gifsicle muéstrame el camino](https://s3.amazonaws.com/f.cl.ly/items/2Z081j0E3R452O030o3U/smtw.gif)

### Importaciones de datos de terceros

Hay un gran volumen de datos de terceros disponibles por ahí, en su mayoría de gobierno, como también de otras fuentes. Si tienen licencia de una manera compatible y de calidad suficiente,  pueden ser utilizados para mejorar el mapa. Las importaciones son generalmente complejas ya que implican fusión con datos de OpenStreetMap existentes y limpieza de datos. Si bien los datos de encuesta de campo y los datos satelitales trazados se pueden agregar a OpenStreetMap sin coordinar con otros miembros de la comunidad, las importaciones  requiere una propuesta formal y una revisión  de la comunidad por pares. Un ejemplo para las importaciones son las importaciones de las construcciones y de las direcciones de la Ciudad de Nueva York  que hemos liderado o de la Oficina de Censo [TIGRE datos](http://wiki.openstreetmap.org/wiki/TIGER) que se ha importado en los Estados Unidos . He aquí una animación del progreso [importando edificios en la ciudad de Nueva York](https://www.mapbox.com/blog/nyc-buildings-openstreetmap/):

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
