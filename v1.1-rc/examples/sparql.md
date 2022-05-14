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
name,startDate
'Colores mágicos' (MAGIA Y CUENTACUENTOS),2022-08-04T20:00+01:00
'Monólogos con JJ Vaquero' (GORI PRODUCIONES),2022-08-10T23:00+01:00
'Desgraciados' (TEATRO ATÓPICO),2022-08-02T22:30+01:00
'Caravana escape room - Houdini experience'' (HÉCTOR SANSEGUNDO),2022-08-12T22:00+01:00
'Circo mágico' (CRISPÍN D'OLOT),2022-08-11T22:00+01:00
"'Versiones Pop Rock años 60, 70, 80, 90' (BACK TO THE COVERS)",2022-08-09T22:00+01:00
'Antes muerta que convicta' (BEATRIZ RICO),2022-08-07T22:00+01:00
'Tributo a Manolo Escobar' (LUIS ESCUDERO),2022-08-11T23:00+01:00
'Payasos de Risolandia' (PANDORA ANIMACIÓN),2022-08-10T12:00+01:00


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
