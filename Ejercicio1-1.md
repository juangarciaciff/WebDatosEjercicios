# Web de Datos 
# Ejercicio 1-1

- Autor: Juan A. García Cuevas
- Fecha: 05/06/2016

### Dado el RDF documento del ejercicio 1, identificar los siguientes elementos: 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<rdf:RDF
xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
xmlns:dc="http://purl.org/dc/elements/1.1/"
xmlns:region="http://www.country-regions.fake/">

<rdf:Description rdf:about="http://en.wikipedia.org/wiki/Oxford">
	<dc:title>Oxford</dc:title>
	<dc:coverage>Oxfordshire</dc:coverage>
	<dc:publisher>Wikipedia</dc:publisher>
	<region:population>10000</region:population>
	<region:principaltown rdf:resource="http://www.country-regions.fake/oxford"/>
</rdf:Description>
 
</rdf:RDF>
```

### Numero de resources referenciados: 
```
	1
```

### Nombre del sujeto de la descripción: 
```
    Oxford
```

### URI del sujeto de la descripción:
```
    http://en.wikipedia.org/wiki/Oxford
```

### Nombre de predicados o propiedades para describir el sujeto: 
```
    title
    coverage
    publisher
    population
    principaltown
```

### Objetos de tipo Literales referenciados por los predicados: 
```
    title: Oxford
    coverage: Oxfordshire
    publisher: Wikipedia
    population: 10000
```

### Objetos de tipo resource referenciados por los predicados:
```
    principaltown: http://www.country-regions.fake/oxford
```

### Vocabularios reutilizados: URI y namespace: 
```
    http://purl.org/dc/elements/1.1/
    http://www.country-regions.fake/
```

### Tag utilizado para describir el documento: 
```
    about
```

### Tag RDF utlizado para describir el recurso: 
```
    resource
```
