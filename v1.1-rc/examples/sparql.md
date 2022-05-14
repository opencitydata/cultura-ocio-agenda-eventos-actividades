## Evento que se celebra en el mes de agosto
```
SELECT DISTINCT ?name ?mes ?startDate ?string 
WHERE {
	?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion> ?documentacion .
	?documentacion <http://schema.org/name> ?name .
  	?evento <http://schema.org/startDate> ?startDate .
		BIND (str(?startDate) AS ?string) 
  		BIND (substr(?string, 6, 2) AS ?mes)
  		FILTER (?mes = '08')
} 
```

## Evento que se celebra el dia 10 de cualquier mes

``` 
SELECT DISTINCT ?name ?dia ?startDate ?string 
WHERE {
	?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion> ?documentacion .
	?documentacion <http://schema.org/name> ?name .
  	?evento <http://schema.org/startDate> ?startDate .
		BIND (str(?startDate) AS ?string) 
  		BIND (substr(?string, 9, 2) AS ?dia)
  		FILTER (?dia = '10')
} 
```
