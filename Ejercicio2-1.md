# Web de Datos 
# Ejercicio 2-1

- Autor: Juan A. García Cuevas
- Fecha: 06/06/2016

## Creación usando RDFS de las siguientes clases, propiedades e instancias:
- Creación de las clases RDFS: “Tweet” y “User”
- Creación de las propiedades:
    - “content”: Un Tweet tiene un contenido (content) de tipo texto.
    - “creator”: Un Tweet tiene un creador (creator) de tipo User
    - “userAccount”: Un User tiene una cuenta de usuario.
- Creación de los individuos:
    - “tweet111” de la claseTweet
    - “user201” de la clase User

#### Versión 1:
```xml
    <?xml version="1.0" encoding="UTF-8"?>
	<rdf:RDF   
	xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"  
	xmlns:rdfs="http://www.w3.org/2000/01/rdf-schema#"
	xml:base="http://example.org/schemas/mytweeter"
	xmlns="http://example.org/schemas/mytweeter#">

		<rdf:Description rdf:ID="Tweet">
			<rdf:type rdf:resource="http://www.w3.org/2000/01/rdf-schema#Class"/>
		</rdf:Description>

		<rdf:Description rdf:ID="User">
			<rdf:type rdf:resource="http://www.w3.org/2000/01/rdf-schema#Class"/>
		</rdf:Description>

		<rdf:Description rdf:ID="content">
			<rdf:type rdf:resource="http://www.w3.org/1999/02/22-rdf-syntax-ns#Property"/>
			<rdfs:domain rdf:resource="#Tweet"/>
		</rdf:Description>

		<rdf:Description rdf:ID="creator">
			<rdf:type rdf:resource="http://www.w3.org/1999/02/22-rdf-syntax-ns#Property"/>
			<rdfs:domain rdf:resource="#Tweet"/>
			<rdfs:range rdf:resource="#User"/>
		</rdf:Description>

		<rdf:Description rdf:ID="userAccount">
			<rdf:type rdf:resource="http://www.w3.org/1999/02/22-rdf-syntax-ns#Property"/>
			<rdfs:domain rdf:resource="#User"/>
		</rdf:Description>

		<Tweet rdf:about="#tweet111">
			<creator rdf:resource="#user201"></creator>
			<content>Difficile est tenere quae acceperis nis exerceas</content>
		</Tweet>

		<User rdf:about="#user201">
			<userAccount>user201@gmail.com</userAccount>
		</User>

	</rdf:RDF>
```

#### Versión 2:
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
			<rdf:type rdf:resource="http://www.w3.org/1999/02/22-rdf-syntax-ns#Property"/>
			<rdfs:domain rdf:resource="#Tweet"/>
		</rdfs:Property>
	
		<rdfs:Property rdf:about="#creator">
			<rdf:type rdf:resource="http://www.w3.org/1999/02/22-rdf-syntax-ns#Property"/>
			<rdfs:domain rdf:resource="#Tweet"/>
			<rdfs:range rdf:resource="#User"/>
		</rdfs:Property>
	
		<rdfs:Property rdf:about="#userAccount">
			<rdf:type rdf:resource="http://www.w3.org/1999/02/22-rdf-syntax-ns#Property"/>
			<rdfs:domain rdf:resource="#User"/>
		</rdfs:Property>
	
		<Tweet rdf:about="#tweet111">
			<creator rdf:resource="#user201"></creator>
			<content>Difficile est tenere quae acceperis nis exerceas</content>
		</Tweet>

		<User rdf:about="#user201">
			<userAccount>user201@gmail.com</userAccount>
		</User>

	</rdf:RDF>
```

#### Versión 3:
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
			<content>Difficile est tenere quae acceperis nis exerceas</content>
		</Tweet>

		<User rdf:about="#user201">
			<userAccount>user201@gmail.com</userAccount>
		</User>

	</rdf:RDF>
```
