# Web de Datos - SPARQL Básico
***
- Autor: Juan A. García Cuevas
- Fecha: 01/07/2016
***


## 1) Ejercicio 4_1: SELECT
Dame aquellas personas que tengan nombre y email (grafo personas)
```sparql
    PREFIX foaf:<http://xmlns.com/foaf/0.1/>

    SELECT ?s ?nombre ?email
    WHERE {  
        ?s foaf:name ?nombre.
        ?s foaf:mbox ?email
    }
```

![Ejercicio 4.1](images/Sparql_4_1.png)

## 2) Ejercicio 4_2: OPTIONAL
Saca el nombre de las personas y si se puede su email (grafo personas)
```sparql
    PREFIX foaf:<http://xmlns.com/foaf/0.1/>
    SELECT ?s ?nombre ?email
    WHERE {
        ?s foaf:name ?nombre.
        OPTIONAL {?s foaf:mbox ?email}
    }
```
![Ejercicio 4.2](images/Sparql_4_2.png)

## 3) Ejercicio 4_3: FILTROS
Cuales son los países que tienen una población superior a 40,000 habitantes (grafo países)
```sparql
    PREFIX dc:<http://purl.org/dc/elements/1.1/>
    PREFIX ex:<http://example.org/country/>
    PREFIX geo:<http://www.w3.org/2003/01/geo/wgs84_pos#>
    PREFIX rdf:<http://www.w3.org/1999/02/22-rdf-syntax-ns#>

    SELECT ?s ?poblacion
    WHERE {
        ?s ex:poblacion ?poblacion.
        ?s rdf:type geo:Country
        FILTER (?poblacion > "40,000")
    }
```

![Ejercicio 4.3](images/Sparql_4_3.png)

## 4) Ejercicio 4_4: ASK/FILTERS
Crea una query para preguntar “Tiene mas población Francia que Canadá? (grafo países)
```sparql
    PREFIX dc:<http://purl.org/dc/elements/1.1/>
    PREFIX ex:<http://example.org/country/>
    PREFIX geo:<http://www.w3.org/2003/01/geo/wgs84_pos#>
    PREFIX rdf:<http://www.w3.org/1999/02/22-rdf-syntax-ns#>

    ASK {
        ex:Francia ex:poblacion ?v
        .....
    }
```

![Ejercicio 4.4](images/Sparql_4_4.png)

## 5) Ejercicio 4_5: UPDATE (CLEAR, CREATE, LOAD): (grafo Award)

### 5.1) Añade una nueva película al grafo por defecto
```sparql
    PREFIX foaf:<http://xmlns.com/foaf/0.1/>
    PREFIX g1:<http://example.org/film/g1/>

    INSERT DATA {
    	g1:m foaf:name "Mi pelicula";
    	     g1:duration "120";
    	     g1:country "Spain";
    	     g1:music "Pepito Perez" .
    }
```

![Ejercicio 4.5.1](images/Sparql_4_5_1.png)

### _5.1.B Para añadir una nueva película al grafo g1_:
```sparql
    PREFIX foaf:<http://xmlns.com/foaf/0.1/>
    PREFIX g1:<http://example.org/film/g1/>

    INSERT DATA {
    	GRAPH <http://example.org/film/g1> {
    		g1:e foaf:name "Mi pelicula";
    		     g1:duration "120";
    		     g1:country "Spain";
    		     g1:music "Pepito Perez" .
    	}
    }
```
![Ejercicio 4.5.1B](images/Sparql_4_5_1B.png)

### 5.2) Elimina el grafo 1 (uri: http://example.org/film/g1) del dataset de award (clear graph)

![Ejercicio 4.5.2](images/Sparql_4_5_2.png)
