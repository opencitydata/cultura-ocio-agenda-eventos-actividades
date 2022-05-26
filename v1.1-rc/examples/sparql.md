
## 1. Eventos cuya audiencia recomendada son los adultos
```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT ?name  ?audience WHERE{
  	?evento rdfs:label ?name .
	?evento <http://schema.org/audience> ?audience .
  		FILTER regex(?audience, "Adultos")
}
```

## 2. Eventos cuyo modo de asistencia sea presencial

``` 
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT * WHERE{
  	?evento rdfs:label ?name .
	?evento <http://schema.org/eventAttendanceMode> ?eventAttendanceMode.
  	FILTER regex(?eventAttendanceMode, "Presencial")
} 
``` 


## 3. Evento que se celebra en el mes de agosto
```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT ?evento ?name ?startDate WHERE{
  	?evento rdfs:label ?name .
	?evento <http://schema.org/startDate> ?startDate .
    	BIND (MONTH(?startDate) AS ?mes) 
  		FILTER (?mes=08)
} 
```


## 4. Evento que tiene el acceso gratuito
```
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT * WHERE{
  	?evento rdfs:label ?name .
  	?evento <http://schema.org/isAccessibleForFree> ?isAccessibleForFree.
  	FILTER (?isAccessibleForFree = 	"true"^^xsd:boolean)
} 
```


## 5. Evento que tiene una capacidad máxima establecida 

```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT * WHERE{
  	?evento rdfs:label ?name .
  	?evento <http://schema.org/maximumAttendeeCapacity> ?maximumAttendeeCapacity.
  		# FILTER regex(?maximumAttendeeCapacity, "")
} 
```

## 6. Eventos que todavia están por celebrarse

```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT * WHERE{
  	?evento rdfs:label ?name .
  	?evento <http://schema.org/eventStatus> ?eventStatus.
  		FILTER regex(?eventStatus, "Por empezar")
} 
```


## 7. Evento cuya edad recomendada es a partir de los 18 años

```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT * WHERE{
  	?evento rdfs:label ?name .
  	?evento <http://schema.org/typicalAgeRange> ?typicalAgeRange.
  		#FILTER regex(?typicalAgeRange, "^*-*")
  		FILTER regex(?typicalAgeRange, "18-")
} 
```


## 8. Eventos que son de tipo concierto

```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT * WHERE{
  	?evento rdfs:label ?name .
	?evento <http://vocab.linkeddata.es/datosabiertos/kos/cultura-ocio/agenda#tipo-evento> <http://vocab.linkeddata.es/datosabiertos/kos/cultura-ocio/agenda/tipo-evento/concierto>
} 
```


## 9. Evento que se realiza en un recinto cerrado

```
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT * WHERE{
  	?evento rdfs:label ?name .
	?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#interior> ?interior
    FILTER (?interior= "true"^^xsd:boolean) .
} 
```

## 10. Evento que se celebra en un recinto llamado "Centro Cultural de la Villa"

``` 
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT * WHERE{
  	?evento rdfs:label ?name .
	?evento <http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras#equipamiento> ?equipamiento .
    ?equipamiento <http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras#nombre> ?nombre
  		FILTER regex(?nombre, "Centro Cultural de la Villa") .
} 
```

## 11. Eventos que tengan lugar en la provincia de salamanca

```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT DISTINCT ?name ?addressRegion WHERE{
  	?evento rdfs:label ?name .
	?evento <http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras#equipamiento> ?equipamiento .
  	?equipamiento <http://schema.org/address> ?address .
    ?address <http://schema.org/addressRegion> ?addressRegion .
  	 	FILTER (?addressRegion = "Salamanca")
}
```

## 12. Eventos que tengan lugar en el municipio del madrid

```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT DISTINCT ?name ?addressLocality WHERE{
  	?evento rdfs:label ?name .
	?evento <http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras#equipamiento> ?equipamiento .
  	?equipamiento <http://schema.org/address> ?address .
    ?address <http://schema.org/addressLocality> ?addressLocality .
  	 	FILTER (?addressLocality = "Madrid")
}
```


## 13. Evento que se celebra el dia 10 de cualquier mes

``` 
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT ?evento ?name ?startDate WHERE{
  	?evento rdfs:label ?name .
	?evento <http://schema.org/startDate> ?startDate .
    	BIND (DAY(?startDate) AS ?day) 
  		FILTER (?day=10)
} 
```

## 14. Nombre de los eventos que se realizan en Salamanca
```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT DISTINCT?name  ?addressRegion WHERE{
  	?evento rdfs:label ?name .
	?evento <http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras#equipamiento> ?equipamiento .
  	?equipamiento <http://schema.org/address> ?address .
    ?address <http://schema.org/addressRegion> ?addressRegion .
  	 	FILTER (?addressRegion = "Salamanca")
} 
```
## 15. El nombre de todos los eventos presenciales de Lorca
```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT DISTINCT ?name ?addressLocality ?eventAttendanceMode WHERE{
  	?evento rdfs:label ?name .
	?evento <http://schema.org/eventAttendanceMode> ?eventAttendanceMode
  		FILTER regex(?eventAttendanceMode, "Presencial") .
	?evento <http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras#equipamiento> ?equipamiento .
  	?equipamiento <http://schema.org/address> ?address .
    ?address <http://schema.org/addressLocality> ?addressLocality 
  		FILTER (?addressLocality = "Lorca") .
}
``` 

## 16. Tipo de audiencia de los conciertos que se realizan en Madrid
```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT DISTINCT ?name ?addressLocality ?audience WHERE{
 	?evento rdfs:label ?name .
  	?evento <http://schema.org/audience> ?audience .
  	?evento <http://vocab.linkeddata.es/datosabiertos/kos/cultura-ocio/agenda#tipo-evento> <http://vocab.linkeddata.es/datosabiertos/kos/cultura-ocio/agenda/tipo-evento/concierto> .
	?evento <http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras#equipamiento> ?equipamiento .
  	?equipamiento <http://schema.org/address> ?address .
    ?address <http://schema.org/addressLocality> ?addressLocality 
  		FILTER (?addressLocality = "Madrid") .
} 
```



## 17. Todos lo eventos gratuitos que se celebren en Madrid en el mes de junio
```
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT DISTINCT ?name ?addressLocality ?isAccessibleForFree ?startDate WHERE{
 	?evento rdfs:label ?name .
  	?evento <http://schema.org/isAccessibleForFree> ?isAccessibleForFree .
  		FILTER (?isAccessibleForFree = "true"^^xsd:boolean)
  	?evento <http://schema.org/startDate> ?startDate .
    	BIND (MONTH(?startDate) AS ?mes) 
  		FILTER (?mes=06)
	?evento <http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras#equipamiento> ?equipamiento .
  	?equipamiento <http://schema.org/address> ?address .
    ?address <http://schema.org/addressLocality> ?addressLocality 
  		FILTER (?addressLocality = "Madrid") .
}
```
