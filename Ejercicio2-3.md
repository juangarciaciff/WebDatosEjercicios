# Web de Datos 
# Ejercicio 2-3

- Autor: Juan A. García Cuevas
- Fecha: 10/06/2016

## Para el ejercicio 2_1 reutilizar en la medida que sea posible las siguientes propiedades:
- “sioc:content” del vocabulario SIOC para la propiedad “content”
- “sioc:has_creator” del vocabulario SIOC para la propiedad “creator”

```xml
    <?xml version="1.0" encoding="UTF-8"?>

	<rdf:RDF   
	xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"  
	xmlns:rdfs="http://www.w3.org/2000/01/rdf-schema#"
	xmlns:sioc="http://rdfs.org/sioc/spec/"
	xml:base="http://example.org/schemas/mytweeter"
	xmlns="http://example.org/schemas/mytweeter#">

		<rdfs:Class rdf:about="#Tweet"/>
	
		<rdfs:Class rdf:about="#User"/>
	
		<rdfs:Property rdf:about="#userAccount">
			<rdfs:domain rdf:resource="#User"/>
		</rdfs:Property>

		<Tweet rdf:about="#tweet111">
			<sioc:has_creator rdf:resource="#user201"></sioc:has_creator>
			<sioc:content>Un tweet</sioc:content>
		</Tweet>

		<User rdf:about="#user201">
			<userAccount>@pepe</userAccount>
		</User>

	</rdf:RDF>
```


