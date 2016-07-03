***
# Web de Datos - Ejercicio 4-7
***
- Autor: Juan A. García Cuevas
- Fecha: 03/07/2016
***

## Ejercicio 4_7:

- Haciendo uso de las cláusulas FROM/FROM NAMED/ GRAPH obtener la duración las películas ganadoras de algún certament.

> Pistas: en el grafo por defecto se obtendra las peliculas ganadora con “g:bestPicture” y del grafo 1 se obtendra la duracion de las mismas con “g1:duration”

```sparql
    PREFIX foaf:<http://xmlns.com/foaf/0.1/>
    PREFIX g1:<http://example.org/film/g1/>
    PREFIX ex4:<http://example.org/award/>

    SELECT ?titulo ?duracion
    FROM default
    FROM NAMED <http://example.org/film/g1>
    WHERE {
    	?s ex4:bestPicture ?titulo
    GRAPH ?graph1
    	{ ?film foaf:name ?titulo .
    	  ?film g1:duration ?duracion}
    }
```
***
