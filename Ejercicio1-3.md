# Web de Datos 
# Ejercicio 1-3

- Autor: Juan A. García Cuevas
- Fecha: 09/06/2016

##Hacer una búsqueda de alguna de las principales web de datos publicadas (ej: http://datos.bne.es/) y hacer un análisis sobre los puntos siguientes:

El nuevo catálogo de la Biblioteca Nacional de España (datos.bne.es) integra en una única aplicación recursos que eran hasta ahora independientes (autoridades, biblioteca digital e índice de materias) y los enriquece con datos de otras bibliotecas. 

## Naturaleza de los datos

El catálogo contiene referencias bibliográficas de los documentos conservados en la Biblioteca: libros, manuscritos, prensa, material gráfico, partituras, audiovisuales y registros sonoros.

La información sobre autores, obras y temas ha sido transformada desde la arquitectura tradicional de las bibliotecas en formatos MARC21 a modelos y estructuras de la web semántica, mediante la herramienta Marimba.

## Tecnologías semánticas usadas

El reto de este proyecto es publicar los catálogos bibliográficos y de autoridades empleando dos componentes básicos de la Web Semántica:

- publicar los catálogos en formato RDF (Resource Description Framework), y 
- que éstos sean conformes a los principios de los Datos Enlazados (Linked Data).

El motor de búsqueda permite explotar el modelo de datos (la ontología BNE) para: 

- asignar una relevancia a las distintas entidades en función de sus conexiones con otras entidades, y 
- presentar al usuario resultados relevantes y estructurados de manera que sea más sencillo encontrar la información.

## Dataset con los que se enriquece

La herramienta marimba enriquece los datos de origen con datos externos a través de enlaces generados durante el proceso de enlazado.

Algunos de los datos enlazados proceden de:

- Instituto Geográfico Nacional (GeoLinkedData)
- Agencia Estatal de Meteorología (Aemet)
- Grupo Prisa Digital (El Viajero)
- Consorcio Regional de Transportes de Madrid y Fundeu (Terminesp)
- DBpedia en español
- Bibliothèque nationale de France
- British Library
- Deutsche Nationalbibliothek
- Library of Congress

## Pros y contras frente a una web estándar

**Pros**:

- Permite una mejor organización de la información.
- Permite que los buscadores encuentran la información relevante más fácilmente.
- Permite recuperar información de forma más amplia, intuitiva y comprensible.
- Facilita la realización de modificaciones en el diseño.
- Favorece compartir información.
- La información puede estar distribuida en varios sitios, de modo que no se depende de un solo servicio.

**Contras**:

- El proceso de adaptación y reestructuración de los documentos de Internet para que puedan ser procesados de forma semántica es muy laborioso y costoso, no sólo por los problemas técnicos sino también por consideraciones de otra índole como, por ejemplo, los idiomas.

- El proceso de unificación de los estándares semánticos (la codificación semántica es compleja) es otro proceso laborioso y costoso.

- Censura y privacidad: una implementación avanzada de la Web Semántica haría más fácil para los gobiernos controlar la visualización y creación de información en línea, ya que esta información sería mucho más fácil de entender para una máquina automatizada de bloqueo de contenidos. Por otro lado, el uso de geolocalización de metadatos reduciría mucho el anonimato asociado a la autoría de artículos, por ejemplo en un blog personal.

##Referencias
- [Biblioteca Nacional de España](http://datos.bne.es/)
- [La UPM desarrolla el nuevo portal de acceso al catálogo de la BNE](http://www.upm.es/Investigacion?fmt=detail&prefmt=articulo&id=a6de7380b69eb410VgnVCM10000009c7648a____)
- [Datos enlazados en la BNE](http://www.bne.es/es/Inicio/Perfiles/Bibliotecarios/DatosEnlazados/)
- [FORMATO MARC 21 PARA REGISTROS BIBLIOGRÁFICOS](http://www.bne.es/es/Micrositios/Guias/Marc21/resources/Docs/Marc21.pdf)
- [Web semántica](https://es.wikipedia.org/wiki/Web_sem%C3%A1ntica)
- [Ventajas y desventajas de la web 3.0](http://evoluciondelawebcg.blogspot.com.es/p/ventajas-y-desventajas-web-30.html)

