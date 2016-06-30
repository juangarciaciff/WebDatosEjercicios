***
# Web de Datos - Ejercicio 5-1
***
- Autor: Juan A. García Cuevas
- Fecha: 24/06/2016
***

Navegar en los siguiente datasets introduciendo la URI de ejemplo:


- BBPedia_ES
    - SPARQL: http://es.dbpedia.org/sparql
    - Ejemplo: http://www.dbpedia.org/page/Alicia_Keys
    - Respuesta:
```txt
La página del ejemplo describe la cantante, autora, productora y actriz Alicia Keys. En la tabla siguiente se muestra el título o nombre de las entidades y el vocabulario empleado para ello:
```
| Vocabulario | Título de entidad |
|-------------|-------------------|
| dbp:name    | Alicia Keys (en)  |
| rdfs:label  | Alicia Keys (en)  |
| foaf:name   | Alicia Keys (en)  |


- MusicBrainz
    - SPARQL: http://dbtune.org/musicbrainz/sparql
    - Ejemplo: http://dbtune.org/musicbrainz/resource/artist/704acdbb-1415-4782-b0b6-0596b8c55e46
    - Respuesta:
```txt
El servicio no está disponible (Service Temporarily Unavailable)

```
- Web n+1 el viajero
    - SPARQL: http://webenemasuno.linkeddata.es/sparql)
    - Ejemplo: http://webenemasuno.linkeddata.es/page/elviajero/resource/Guide/20060513ELPVIALBV_5.TES
    - Respuesta:
```txt
La página del ejemplo trata sobre un vino
```

- MDB:
    - SPARQL: http://data.linkedmdb.org/sparql
    - Ejemplo: http://data.linkedmdb.org/page/film/300
    - Respuesta:
```txt
```

Y determinar los siguiente:

- Que tipo de entidades esta describiendo
- titulo o name que tiene las entidades
- vocabulario usado para indicar el titulo o name
