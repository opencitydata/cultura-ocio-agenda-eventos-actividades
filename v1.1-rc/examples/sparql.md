# Cosas a mejorar
- La de agosto se puede hacer más sencilla, pues hayfunción en SPARQL para sacar el mes de una fecha. Lo. Mismo la del día 10 de cada mes.
- Evento tipo concierto veo que está mal, y será problema del RDF. El kos no puede ser una propiedad, debería ser el objeto. Si está así en la onto o datos hay que retocarlo
- Además, me gustaría no abusar del FILTER, sino marcar en algunos el SKOS concept correspondiente.
- ¿Por qué el nombre de un evento se devuelve a partir de su documentación? Quizás es fallo mío al revisar, pero me parece muy raro que no sea un rdfs:label asociado directamente al evento.
- El Retiro no es un municipio!!!!



## Eventos cuya audiencia recomendada son los adultos
```
SELECT DISTINCT ?name ?audience WHERE {
	?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion> ?documentacion .
	?documentacion <http://schema.org/name> ?name .
  	?evento <http://schema.org/audience> ?audience .
  FILTER regex(?audience, "Adultos")
} 
```
**La salida en formato csv es**:


![image](https://user-images.githubusercontent.com/39318241/168426304-f77f8692-c451-4a1b-a0c9-ad4e20c63299.png)


## Eventos cuyo modo de asistencia sea presencial

``` 
SELECT DISTINCT ?name ?eventAttendanceMode WHERE {
	?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion> ?documentacion .
	?documentacion <http://schema.org/name> ?name .
  	?evento <http://schema.org/eventAttendanceMode> ?eventAttendanceMode.
  FILTER regex(?eventAttendanceMode, "Presencial")
} 
``` 
**La salida en formato csv es**:


![image](https://user-images.githubusercontent.com/39318241/168426459-9a86775e-5f8d-44a7-af86-ac63855d1c7b.png)


## Evento que se celebra en el mes de agosto
```
SELECT DISTINCT ?name ?startDate ?mes
WHERE {
	?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion> ?documentacion .
	?documentacion <http://schema.org/name> ?name .
  	?evento <http://schema.org/startDate> ?startDate .
    	BIND (MONTH(?startDate) AS ?mes) 
  		FILTER (?mes = '08')
} 
```


## Evento que tiene el acceso gratuito
```
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
SELECT DISTINCT ?name ?isAccessibleForFree WHERE {
	?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion> ?documentacion .
	?documentacion <http://schema.org/name> ?name .
  	?evento <http://schema.org/isAccessibleForFree> ?isAccessibleForFree.
  	FILTER (?isAccessibleForFree = 	"true"^^xsd:boolean)
} 
```
**La salida del formato CSV es**:


![image](https://user-images.githubusercontent.com/39318241/168488036-9a5bf2c4-14a9-4e1c-8875-7d2117b55639.png)

## Evento que tiene una capacidad máxima establecida 

```
SELECT DISTINCT ?name ?maximumAttendeeCapacity WHERE {
	?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion> ?documentacion .
	?documentacion <http://schema.org/name> ?name .
  	?evento <http://schema.org/maximumAttendeeCapacity> ?maximumAttendeeCapacity.
  		# FILTER regex(?maximumAttendeeCapacity, "")
} 
```
**La salida del CSV es***:


![image](https://user-images.githubusercontent.com/39318241/168427100-441f9212-7675-47f4-9ab8-25de464148e9.png)


## Eventos que todavia están por celebrarse

```
SELECT DISTINCT ?name ?eventStatus WHERE {
	?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion> ?documentacion .
	?documentacion <http://schema.org/name> ?name .
  	?evento <http://schema.org/eventStatus> ?eventStatus.
  		FILTER regex(?eventStatus, "Por empezar")
} 
```


![image](https://user-images.githubusercontent.com/39318241/168427171-e462fbc2-0587-4b73-b185-00f892b22296.png)


## Evento cuya edad recomendada es a partir de los 18 años

```
SELECT DISTINCT ?name ?typicalAgeRange WHERE {
	?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion> ?documentacion .
	?documentacion <http://schema.org/name> ?name .
  	?evento <http://schema.org/typicalAgeRange> ?typicalAgeRange.
  		#FILTER regex(?typicalAgeRange, "^*-*")
  		FILTER regex(?typicalAgeRange, "18-")
} 
```

![image](https://user-images.githubusercontent.com/39318241/168427444-f8622fb4-cb0b-48a9-beb2-d0dae87ddcb5.png)


## Eventos que son de tipo concierto

```
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
SELECT DISTINCT ?name ?tipoEvento ?tipo WHERE {
	?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion> ?documentacion .
	?documentacion <http://schema.org/name> ?name .
  	?evento <http://vocab.linkeddata.es/datosabiertos/kos/cultura-ocio/agenda#tipo-evento> ?tipoEvento.
  FILTER (datatype(?tipoEvento)= xsd:anyURI)
  FILTER (?tipoEvento = "http://vocab.linkeddata.es/datosabiertos/kos/cultura-ocio/agenda/tipo-evento/teatro"^^xsd:anyURI)
}  
```


![image](https://user-images.githubusercontent.com/39318241/168427719-8b7845e2-177f-4414-a625-5607dc00d7c9.png)


## Evento que se realiza en un recinto cerrado

```
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>

SELECT DISTINCT ?name ?interior WHERE {
	?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion> ?documentacion .
	?documentacion <http://schema.org/name> ?name .
  	?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#interior> ?interior
    FILTER (?interior= "true"^^xsd:boolean) .
} 
```

![image](https://user-images.githubusercontent.com/39318241/168427791-e87b63a6-07a5-4aac-b311-5f82593147fb.png)


## Evento que se celebra en un recinto llamado "Centro Cultural de la Villa"

``` 
SELECT DISTINCT ?name ?nombre WHERE {
	?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion> ?documentacion .
 	?evento <http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras#equipamiento> ?equipamiento .
	?documentacion <http://schema.org/name> ?name .
    ?equipamiento <http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras#nombre> ?nombre
  FILTER regex(?nombre, "Centro Cultural de la Villa") .
}
```

![image](https://user-images.githubusercontent.com/39318241/168428122-1bbea049-6902-4904-ae7f-2e8a014b1fe8.png)


## Eventos que tengan lugar en la provincia de salamanca

```
SELECT DISTINCT ?name ?addressRegion WHERE {
	?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion> ?documentacion .
 	?evento <http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras#equipamiento> ?equipamiento .
	?documentacion <http://schema.org/name> ?name .
    ?equipamiento <http://schema.org/address> ?address .
  ?address <http://schema.org/addressRegion> ?addressRegion .
  FILTER (?addressRegion = "Salamanca")
} 
```

![image](https://user-images.githubusercontent.com/39318241/168428271-e58d4ff7-8116-43cf-8092-a4df15e598e6.png)



## Eventos que tengan lugar en el municipio del retiro

```
SELECT DISTINCT ?name ?addressLocality WHERE {
	?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion> ?documentacion .
 	?evento <http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras#equipamiento> ?equipamiento .
	?documentacion <http://schema.org/name> ?name .
    ?equipamiento <http://schema.org/address> ?address .
  ?address <http://schema.org/addressLocality> ?addressLocality .
  FILTER (?addressLocality = "Retiro")
} 
```

![image](https://user-images.githubusercontent.com/39318241/168428356-2c19e1b3-2bca-48c3-acae-f9fff6ec9695.png)


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
