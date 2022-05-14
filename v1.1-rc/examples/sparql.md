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
**La salida en formato csv es**:
![imagen](https://user-images.githubusercontent.com/39318241/168403078-2ad1df0b-78b7-4c56-9657-117d45cb8088.png)



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
