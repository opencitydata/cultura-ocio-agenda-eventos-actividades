
## 1. Eventos cuya audiencia recomendada son los adultos
```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT ?name  ?audience WHERE{
  	?evento rdfs:label ?name .
	?evento <http://schema.org/audience> ?audience .
  		FILTER regex(?audience, "Adultos")
}
```

evento | name | audience

http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413089 | Malvivir | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11579708 | La Perra Blanco - Tetuan | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285151041284 | 'Los mentalistas' (LA CHISTERA MÁGICA) | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285144199175 | 'Cosas nuestras' (KATUA&GALEA TEATRO) | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285140239576 | 'Silencio' (AVANCE PRODUCCIONES TEATRALES) | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285143668478 | 'Muerte de un viajante' (OKAPI PRODUCCIONES) | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139511846 | 'Guitarras de cine' (JESÚS PARRA) | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11625471 | Sesiones de abordaje de la soledad | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285142107385 | "'La Celestina |  un selfie con Melibea' (UN PINGÜINO PRODUCCIONES)" | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285144969202 | 'Los invisibles' (LA CORACHA TEATRO) | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139023785 | 'Danzando por el mundo' (ARTESHOW ESPECTÁCULOS S.L.) | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153632819 | 'Antes muerta que convicta' (BEATRIZ RICO) | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285143675146 | 'Inquietante' (BAMBALUA TEATRO) | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285142985689 | 'El mueble' (HISTRIÓN TEATRO) | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11580799 | "Bengala |  una vida en doce asaltos (Hortaleza)" | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285141564385 | 'ABBA - live in concert - 50 aniversario' (TEATRALMENTE PRODUCCIONES) | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153337815 | 'Desgraciados' (TEATRO ATÓPICO) | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413103 | Là | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413115 | La mirada del avestruz | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285140678968 | '¡Viva la Pepa!' (PENTACIÓN) | Adultos
http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285145381377 | 'Oceanía' (TRASPASOS) | Adultos



## 2. Eventos cuyo modo de asistencia sea presencial

``` 
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT * WHERE{
  	?evento rdfs:label ?name .
	?evento <http://schema.org/eventAttendanceMode> ?eventAttendanceMode.
  	FILTER regex(?eventAttendanceMode, "Presencial")
} 
``` 
**La salida en formato csv es**:


image.png


## Evento que se celebra en el mes de agosto
```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT ?evento ?name ?startDate WHERE{
  	?evento rdfs:label ?name .
	?evento <http://schema.org/startDate> ?startDate .
    	BIND (MONTH(?startDate) AS ?mes) 
  		FILTER (?mes=08)
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
SELECT DISTINCT ?name WHERE {
    ?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion> ?documentacion .
    ?documentacion <http://schema.org/name> ?name .
    ?evento <http://vocab.linkeddata.es/datosabiertos/kos/cultura-ocio/agenda#tipo-evento> <http://vocab.linkeddata.es/datosabiertos/kos/cultura-ocio/agenda/tipo-evento/concierto>
}
```


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



## Eventos que tengan lugar en el municipio del madrid

```
SELECT DISTINCT ?name ?addressLocality WHERE {
	?evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion> ?documentacion .
 	?evento <http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras#equipamiento> ?equipamiento .
	?documentacion <http://schema.org/name> ?name .
    ?equipamiento <http://schema.org/address> ?address .
  ?address <http://schema.org/addressLocality> ?addressLocality .
  FILTER (?addressLocality = "Madrid")
} 
```

![image](https://user-images.githubusercontent.com/39318241/168491193-f2592b0f-5032-4b62-a1e5-c6bf977530e1.png)


## Evento que se celebra el dia 10 de cualquier mes

``` 
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT ?evento ?name ?startDate WHERE{
  	?evento rdfs:label ?name .
	?evento <http://schema.org/startDate> ?startDate .
    	BIND (DAY(?startDate) AS ?dia) 
  		FILTER (?dia=10)
} 
```
