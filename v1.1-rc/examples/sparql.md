
## 1. Eventos cuya audiencia recomendada son los adultos
```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT ?name  ?audience WHERE{
  	?evento rdfs:label ?name .
	?evento <http://schema.org/audience> ?audience .
  		FILTER regex(?audience, "Adultos")
}
```


|evento|name|audience|
|:----|:----|:----|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413089|Malvivir|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11579708|La Perra Blanco - Tetuan|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285151041284|'Los mentalistas' (LA CHISTERA MÁGICA)|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285144199175|'Cosas nuestras' (KATUA&GALEA TEATRO)|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285140239576|'Silencio' (AVANCE PRODUCCIONES TEATRALES)|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285143668478|'Muerte de un viajante' (OKAPI PRODUCCIONES)|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139511846|'Guitarras de cine' (JESÚS PARRA)|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11625471|Sesiones de abordaje de la soledad|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285142107385|'La Celestina, un selfie con Melibea' (UN PINGÜINO PRODUCCIONES)|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285144969202|'Los invisibles' (LA CORACHA TEATRO)|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139023785|'Danzando por el mundo' (ARTESHOW ESPECTÁCULOS S.L.)|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153632819|'Antes muerta que convicta' (BEATRIZ RICO)|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285143675146|'Inquietante' (BAMBALUA TEATRO)|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285142985689|'El mueble' (HISTRIÓN TEATRO)|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11580799|Bengala, una vida en doce asaltos (Hortaleza)|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285141564385|'ABBA - live in concert - 50 aniversario' (TEATRALMENTE PRODUCCIONES)|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153337815|'Desgraciados' (TEATRO ATÓPICO)|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413103|Là|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413115|La mirada del avestruz|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285140678968|'¡Viva la Pepa!' (PENTACIÓN)|Adultos|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285145381377|'Oceanía' (TRASPASOS)|Adultos|




## 2. Eventos cuyo modo de asistencia sea presencial

``` 
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT * WHERE{
  	?evento rdfs:label ?name .
	?evento <http://schema.org/eventAttendanceMode> ?eventAttendanceMode.
  	FILTER regex(?eventAttendanceMode, "Presencial")
} 
``` 


|evento|name|eventAttendanceMode|
|:---:|:---:|:---:|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139069288|'Vinum' (ARVINE DANZA)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413089|Malvivir|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285141799341|'Cuentacuentos el libro mágico de Kolumelah' (KOLUMELAH CUENTACUENTOS)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413107|Dystopie|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11591790|Ari Tavares - Villa de Vallecas|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11637392|Las desventuras de Don Quijote|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3317|Visita teatralizada: EL SECRETO DEL IRLANDÉS|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11634548|Hechos luctuosos del Madrid Antiguo|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11579708|La Perra Blanco - Tetuan|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285151041284|'Los mentalistas' (LA CHISTERA MÁGICA)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3360|AUTOMOVILISMO|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11637393|Abalconados 2020|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11578054|Antonio Lizana (Latina)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153654373|'Monólogos con JJ Vaquero' (GORI PRODUCIONES)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11577835|Lichis (Puente de Vallecas)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153785025|'Caravana escape room - Houdini experience'' (HÉCTOR SANSEGUNDO)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285144199175|'Cosas nuestras' (KATUA&GALEA TEATRO)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139195165|'Y tú, ¿qué sabes?... de Miguel de Cervantes' (ARAWAKE)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285140239576|'Silencio' (AVANCE PRODUCCIONES TEATRALES)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285143668478|'Muerte de un viajante' (OKAPI PRODUCCIONES)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139511846|'Guitarras de cine' (JESÚS PARRA)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285141535187|'A vueltas con Lorca' (DOS HERMANAS CATORCE)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3426|El Rey Sabio para niños: el ajedrez y la Torre Alfonsina |Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11625471|Sesiones de abordaje de la soledad|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11514185|Espacio de crianza y juego libre|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11593905|Taller de Beatbox - Villa de Vallecas|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/7644875|Jueves de Hability|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11637390|Homenaje a Sara Montiel|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11611820|Taller de poesía y narrativa|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285142107385|'La Celestina, un selfie con Melibea' (UN PINGÜINO PRODUCCIONES)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11587808|Degustación de felicidad|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11483995|Las aventuras del Doctor Dolittle|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11643484|Ludens Cía. La potínguele|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11643150|En un muelle de Normandía|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11643194|Josefina|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11636800|El libro que se sentía solo|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3423|Paquete especial Semana Santa. Entradas a espacios interiores del Castillo de Lorca. (Del 14 al 17 de Abril)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285144969202|'Los invisibles' (LA CORACHA TEATRO)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11566482|Círculo de mujeres: autodescubrimiento y autoestima|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11644457|Mica Mita Cía. por humor al arte  TEATRO PARA BEBÉS|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139023785|'Danzando por el mundo' (ARTESHOW ESPECTÁCULOS S.L.)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153632819|'Antes muerta que convicta' (BEATRIZ RICO)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3403|EXPOSICIÓN CARTELES DE SEMANA SANTA LORCA|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285143675146|'Inquietante' (BAMBALUA TEATRO)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11645067|Taller de ansiedad y estrés|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285142985689|'El mueble' (HISTRIÓN TEATRO)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11580736|GET NO - Latina|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11580799|Bengala, una vida en doce asaltos (Hortaleza)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11640435|Cavernícola|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285143361309|'Abrojo folk - El sueño que sobrevive' (ETNO SONIDO PRODUCCIONES)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285141564385|'ABBA - live in concert - 50 aniversario' (TEATRALMENTE PRODUCCIONES)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153337815|'Desgraciados' (TEATRO ATÓPICO)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285152058227|'A su servicio' (TIRITIRANTES CIRCO TEATRO)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285144835353|'Con la cabeza en las nubes' (EUGENIA MANZANERA DE LA FUENTE)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285137762140|'Con la cabeza en las nubes' (EUGENIA MANZANERA DE LA FUENTE)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11642687|Mica Mita  Cía. por humor al arte|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153751569|'Payasos de Risolandia' (PANDORA ANIMACIÓN)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285150475149|'¡El gran Cáliban! (las locas historias de un circo en miniatura)' (TEATRO ALÚA)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11643216|Las cosas que decimos, las cosas que hacemos|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3421|SILVESTRISMO|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413103|Là|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413111|En un sol amarillo. Memorias de un temblor|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285141280557|'La red' (KAMARU TEATRO)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285137724159|'La Chimba' (INNOVARTE CREACIONES ARTISTICAS)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153756368|'Tributo a Manolo Escobar' (LUIS ESCUDERO)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285145047183|'Con beee!! de oveja' (KAMARU TEATRO)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3328|Visita guiada: EL CASCO ANTIGUO DE LORCA|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153352052|'Colores mágicos' (MAGIA Y CUENTACUENTOS)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11637388|Amores en Quequén|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285150149603|'El circo de las ranas' (JUAN CATALINA)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11598526|Maliang y el pincel mágico (Tetuán)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11642694|Porque Do, porque Si Cía. Teatro Tyl Tyl|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285142371124|'Un sibarita con varita' (HÉCTOR SAN SEGUNDO)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11640419|Salvando al planeta|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285149591405|'La vida es un cuento y los cuentos sueños son' (POPY VEGAS)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285143854976|'Soliluna' (HILANDO TITERES)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285138670602|'El sótano encantado' (TEATRO MUTIS)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11638469|El profesor chiflado|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11588309|Masculinidades y sexualidad consciente|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285142194935|'La bruja Kalambres' (INNOVARTE CREACIONES ARTISTICAS)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413115|La mirada del avestruz|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11566487|Creciendo juntas|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413096|La vida es sueño|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11566513|Batucada feminista|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153724090|'Versiones Pop Rock años 60, 70, 80, 90' (BACK TO THE COVERS)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11615773|Asesoría informática|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285152029237|'El bosque de cuentos' (CHARO JAULAR)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285145014610|'Ópera para rock para niños: Rapunzel' (FERRO TEATRO)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153767042|'Circo mágico' (CRISPÍN D'OLOT)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/10621974|Dance Studio 23|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285140678968|'¡Viva la Pepa!' (PENTACIÓN)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11578004|Somos la guerra (Puente de Vallecas)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3302|Visita guiada: LORCA MONUMENTAL Y SU BORDADO|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139492165|'Los zapateros y otras fábulas' (CUENTACUENTOS KELLER)|Presencial|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285145381377|'Oceanía' (TRASPASOS)|Presencial|


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
