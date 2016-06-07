# Web de Datos 
# Ejercicio 2-2

- Autor: Juan A. García Cuevas
- Fecha: 06/06/2016

## Partiendo de las clases, propiedades e individuos definido en el Ejercicio 2_1, describir los siguientes elementos haciendo uso de RDFS:
- el tweet111 tiene el creador user201
- el tweet111 tiene el contenido "Un tweet“
- el user201 tiene una cuenta de usaurio "@pepe"

```xml
    <?xml version="1.0" encoding="UTF-8"?>

	<rdf:RDF   
	xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"  
	xmlns:rdfs="http://www.w3.org/2000/01/rdf-schema#"
	xml:base="http://example.org/schemas/mytweeter"
	xmlns="http://example.org/schemas/mytweeter#">

		<rdfs:Class rdf:about="#Tweet"/>
	
		<rdfs:Class rdf:about="#User"/>
	
		<rdfs:Property rdf:about="#content">
			<rdfs:domain rdf:resource="#Tweet"/>
		</rdfs:Property>
	
		<rdfs:Property rdf:about="#creator">
			<rdfs:domain rdf:resource="#Tweet"/>
			<rdfs:range rdf:resource="#User"/>
		</rdfs:Property>
	
		<rdfs:Property rdf:about="#userAccount">
			<rdfs:domain rdf:resource="#User"/>
		</rdfs:Property>

		<Tweet rdf:about="#tweet111">
			<creator rdf:resource="#user201"></creator>
			<content>Un tweet</content>
		</Tweet>

		<User rdf:about="#user201">
			<userAccount>@pepe</userAccount>
		</User>

	</rdf:RDF>
```
