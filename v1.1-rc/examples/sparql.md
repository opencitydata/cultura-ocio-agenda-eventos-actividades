
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


|evento|name|startDate|
|:---:|:---:|:---:|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153654373|'Monólogos con JJ Vaquero' (GORI PRODUCIONES)|2022-08-10T23:00:00+01:00|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153785025|'Caravana escape room - Houdini experience'' (HÉCTOR SANSEGUNDO)|2022-08-12T22:00:00+01:00|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153632819|'Antes muerta que convicta' (BEATRIZ RICO)|2022-08-07T22:00:00+01:00|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153337815|'Desgraciados' (TEATRO ATÓPICO)|2022-08-02T22:30:00+01:00|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153751569|'Payasos de Risolandia' (PANDORA ANIMACIÓN)|2022-08-10T12:00:00+01:00|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153756368|'Tributo a Manolo Escobar' (LUIS ESCUDERO)|2022-08-11T23:00:00+01:00|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153352052|'Colores mágicos' (MAGIA Y CUENTACUENTOS)|2022-08-04T20:00:00+01:00|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153724090|'Versiones Pop Rock años 60, 70, 80, 90' (BACK TO THE COVERS)|2022-08-09T22:00:00+01:00|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153767042|'Circo mágico' (CRISPÍN D'OLOT)|2022-08-11T22:00:00+01:00|


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


|evento|name|isAccessibleForFree|
|:----|:----|:----|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413089|Malvivir|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285141799341|'Cuentacuentos el libro mágico de Kolumelah' (KOLUMELAH CUENTACUENTOS)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413107|Dystopie|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11591790|Ari Tavares - Villa de Vallecas|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11637392|Las desventuras de Don Quijote|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3317|Visita teatralizada: EL SECRETO DEL IRLANDÉS|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11634548|Hechos luctuosos del Madrid Antiguo|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11579708|La Perra Blanco - Tetuan|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3360|AUTOMOVILISMO|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11637393|Abalconados 2020|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11578054|Antonio Lizana (Latina)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11577835|Lichis (Puente de Vallecas)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11625471|Sesiones de abordaje de la soledad|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11514185|Espacio de crianza y juego libre|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11593905|Taller de Beatbox - Villa de Vallecas|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/7644875|Jueves de Hability|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11637390|Homenaje a Sara Montiel|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11611820|Taller de poesía y narrativa|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11587808|Degustación de felicidad|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11483995|Las aventuras del Doctor Dolittle|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11643484|Ludens Cía. La potínguele|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11643150|En un muelle de Normandía|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11643194|Josefina|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11636800|El libro que se sentía solo|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11566482|Círculo de mujeres: autodescubrimiento y autoestima|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11644457|Mica Mita Cía. por humor al arte  TEATRO PARA BEBÉS|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153632819|'Antes muerta que convicta' (BEATRIZ RICO)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3403|EXPOSICIÓN CARTELES DE SEMANA SANTA LORCA|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11645067|Taller de ansiedad y estrés|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11580736|GET NO - Latina|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11580799|Bengala, una vida en doce asaltos (Hortaleza)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11640435|Cavernícola|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11642687|Mica Mita  Cía. por humor al arte|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153751569|'Payasos de Risolandia' (PANDORA ANIMACIÓN)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11643216|Las cosas que decimos, las cosas que hacemos|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3421|SILVESTRISMO|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413103|Là|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413111|En un sol amarillo. Memorias de un temblor|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285137724159|'La Chimba' (INNOVARTE CREACIONES ARTISTICAS)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3328|Visita guiada: EL CASCO ANTIGUO DE LORCA|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153352052|'Colores mágicos' (MAGIA Y CUENTACUENTOS)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11637388|Amores en Quequén|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11598526|Maliang y el pincel mágico (Tetuán)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11642694|Porque Do, porque Si Cía. Teatro Tyl Tyl|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11640419|Salvando al planeta|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11638469|El profesor chiflado|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11588309|Masculinidades y sexualidad consciente|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413115|La mirada del avestruz|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11566487|Creciendo juntas|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413096|La vida es sueño|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11566513|Batucada feminista|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153724090|'Versiones Pop Rock años 60, 70, 80, 90' (BACK TO THE COVERS)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11615773|Asesoría informática|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153767042|'Circo mágico' (CRISPÍN D'OLOT)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/10621974|Dance Studio 23|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11578004|Somos la guerra (Puente de Vallecas)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3302|Visita guiada: LORCA MONUMENTAL Y SU BORDADO|true|


## 5. Evento que tiene una capacidad máxima establecida 

```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT * WHERE{
  	?evento rdfs:label ?name .
  	?evento <http://schema.org/maximumAttendeeCapacity> ?maximumAttendeeCapacity.
  		# FILTER regex(?maximumAttendeeCapacity, "")
} 
```


|evento|name|maximumAttendeeCapacity|
|:----|:----|:----|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153785025|'Caravana escape room - Houdini experience'' (HÉCTOR SANSEGUNDO)|301|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/7644875|Jueves de Hability|12|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139023785|'Danzando por el mundo' (ARTESHOW ESPECTÁCULOS S.L.)|301|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153767042|'Circo mágico' (CRISPÍN D'OLOT)|303|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/10621974|Dance Studio 23|15|



## 6. Eventos que todavia están por celebrarse

```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT * WHERE{
  	?evento rdfs:label ?name .
  	?evento <http://schema.org/eventStatus> ?eventStatus.
  		FILTER regex(?eventStatus, "Por empezar")
} 
```


|evento|name|eventStatus|
|:----|:----|:----|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413089|Malvivir|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413107|Dystopie|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11591790|Ari Tavares - Villa de Vallecas|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3317|Visita teatralizada: EL SECRETO DEL IRLANDÉS|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11634548|Hechos luctuosos del Madrid Antiguo|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11579708|La Perra Blanco - Tetuan|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285151041284|'Los mentalistas' (LA CHISTERA MÁGICA)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11578054|Antonio Lizana (Latina)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153654373|'Monólogos con JJ Vaquero' (GORI PRODUCIONES)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11577835|Lichis (Puente de Vallecas)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153785025|'Caravana escape room - Houdini experience'' (HÉCTOR SANSEGUNDO)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11625471|Sesiones de abordaje de la soledad|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11514185|Espacio de crianza y juego libre|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11593905|Taller de Beatbox - Villa de Vallecas|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11611820|Taller de poesía y narrativa|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11587808|Degustación de felicidad|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11643484|Ludens Cía. La potínguele|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11643150|En un muelle de Normandía|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11643194|Josefina|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11566482|Círculo de mujeres: autodescubrimiento y autoestima|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153632819|'Antes muerta que convicta' (BEATRIZ RICO)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11645067|Taller de ansiedad y estrés|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11580736|GET NO - Latina|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11580799|Bengala, una vida en doce asaltos (Hortaleza)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153337815|'Desgraciados' (TEATRO ATÓPICO)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285152058227|'A su servicio' (TIRITIRANTES CIRCO TEATRO)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153751569|'Payasos de Risolandia' (PANDORA ANIMACIÓN)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285150475149|'¡El gran Cáliban! (las locas historias de un circo en miniatura)' (TEATRO ALÚA)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11643216|Las cosas que decimos, las cosas que hacemos|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413103|Là|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413111|En un sol amarillo. Memorias de un temblor|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153756368|'Tributo a Manolo Escobar' (LUIS ESCUDERO)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3328|Visita guiada: EL CASCO ANTIGUO DE LORCA|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153352052|'Colores mágicos' (MAGIA Y CUENTACUENTOS)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285150149603|'El circo de las ranas' (JUAN CATALINA)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11598526|Maliang y el pincel mágico (Tetuán)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285149591405|'La vida es un cuento y los cuentos sueños son' (POPY VEGAS)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11588309|Masculinidades y sexualidad consciente|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413115|La mirada del avestruz|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11566487|Creciendo juntas|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11566513|Batucada feminista|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153724090|'Versiones Pop Rock años 60, 70, 80, 90' (BACK TO THE COVERS)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11615773|Asesoría informática|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285152029237|'El bosque de cuentos' (CHARO JAULAR)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153767042|'Circo mágico' (CRISPÍN D'OLOT)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11578004|Somos la guerra (Puente de Vallecas)|Por empezar|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3302|Visita guiada: LORCA MONUMENTAL Y SU BORDADO|Por empezar|



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

|evento|name|typicalAgeRange|
|:----|:----|:----|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413089|Malvivir|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285151041284|'Los mentalistas' (LA CHISTERA MÁGICA)|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285144199175|'Cosas nuestras' (KATUA&GALEA TEATRO)|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285140239576|'Silencio' (AVANCE PRODUCCIONES TEATRALES)|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285143668478|'Muerte de un viajante' (OKAPI PRODUCCIONES)|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139511846|'Guitarras de cine' (JESÚS PARRA)|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285142107385|'La Celestina, un selfie con Melibea' (UN PINGÜINO PRODUCCIONES)|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11587808|Degustación de felicidad|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285144969202|'Los invisibles' (LA CORACHA TEATRO)|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11566482|Círculo de mujeres: autodescubrimiento y autoestima|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139023785|'Danzando por el mundo' (ARTESHOW ESPECTÁCULOS S.L.)|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153632819|'Antes muerta que convicta' (BEATRIZ RICO)|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285143675146|'Inquietante' (BAMBALUA TEATRO)|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285142985689|'El mueble' (HISTRIÓN TEATRO)|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11580799|Bengala, una vida en doce asaltos (Hortaleza)|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285141564385|'ABBA - live in concert - 50 aniversario' (TEATRALMENTE PRODUCCIONES)|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153337815|'Desgraciados' (TEATRO ATÓPICO)|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413103|Là|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413115|La mirada del avestruz|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11566487|Creciendo juntas|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11566513|Batucada feminista|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11615773|Asesoría informática|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285140678968|'¡Viva la Pepa!' (PENTACIÓN)|18-|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285145381377|'Oceanía' (TRASPASOS)|18-|



## 8. Eventos que son de tipo concierto

```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT * WHERE{
  	?evento rdfs:label ?name .
	?evento <http://vocab.linkeddata.es/datosabiertos/kos/cultura-ocio/agenda#tipo-evento> <http://vocab.linkeddata.es/datosabiertos/kos/cultura-ocio/agenda/tipo-evento/concierto>
} 
```

|evento|name|
|:----|:----|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11637390|Homenaje a Sara Montiel|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/7644875|Jueves de Hability|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11578054|Antonio Lizana (Latina)|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11591790|Ari Tavares - Villa de Vallecas|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285145014610|'Ópera para rock para niños: Rapunzel' (FERRO TEATRO)|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139511846|'Guitarras de cine' (JESÚS PARRA)|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153724090|'Versiones Pop Rock años 60, 70, 80, 90' (BACK TO THE COVERS)|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11579708|La Perra Blanco - Tetuan|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153756368|'Tributo a Manolo Escobar' (LUIS ESCUDERO)|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11637388|Amores en Quequén|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285143361309|'Abrojo folk - El sueño que sobrevive' (ETNO SONIDO PRODUCCIONES)|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285141564385|'ABBA - live in concert - 50 aniversario' (TEATRALMENTE PRODUCCIONES)|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11577835|Lichis (Puente de Vallecas)|


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

|evento|name|interior|
|:----|:----|:----|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139069288|'Vinum' (ARVINE DANZA)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413089|Malvivir|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285141799341|'Cuentacuentos el libro mágico de Kolumelah' (KOLUMELAH CUENTACUENTOS)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413107|Dystopie|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11591790|Ari Tavares - Villa de Vallecas|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11637392|Las desventuras de Don Quijote|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11634548|Hechos luctuosos del Madrid Antiguo|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11579708|La Perra Blanco - Tetuan|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285151041284|'Los mentalistas' (LA CHISTERA MÁGICA)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3360|AUTOMOVILISMO|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11637393|Abalconados 2020|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11578054|Antonio Lizana (Latina)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153654373|'Monólogos con JJ Vaquero' (GORI PRODUCIONES)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11577835|Lichis (Puente de Vallecas)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285144199175|'Cosas nuestras' (KATUA&GALEA TEATRO)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139195165|'Y tú, ¿qué sabes?... de Miguel de Cervantes' (ARAWAKE)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285140239576|'Silencio' (AVANCE PRODUCCIONES TEATRALES)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285143668478|'Muerte de un viajante' (OKAPI PRODUCCIONES)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139511846|'Guitarras de cine' (JESÚS PARRA)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285141535187|'A vueltas con Lorca' (DOS HERMANAS CATORCE)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11625471|Sesiones de abordaje de la soledad|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11514185|Espacio de crianza y juego libre|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11593905|Taller de Beatbox - Villa de Vallecas|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/7644875|Jueves de Hability|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11637390|Homenaje a Sara Montiel|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11611820|Taller de poesía y narrativa|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285142107385|'La Celestina, un selfie con Melibea' (UN PINGÜINO PRODUCCIONES)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11587808|Degustación de felicidad|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11483995|Las aventuras del Doctor Dolittle|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11643484|Ludens Cía. La potínguele|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11643150|En un muelle de Normandía|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11643194|Josefina|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11636800|El libro que se sentía solo|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285144969202|'Los invisibles' (LA CORACHA TEATRO)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11566482|Círculo de mujeres: autodescubrimiento y autoestima|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11644457|Mica Mita Cía. por humor al arte  TEATRO PARA BEBÉS|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139023785|'Danzando por el mundo' (ARTESHOW ESPECTÁCULOS S.L.)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153632819|'Antes muerta que convicta' (BEATRIZ RICO)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/3403|EXPOSICIÓN CARTELES DE SEMANA SANTA LORCA|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285143675146|'Inquietante' (BAMBALUA TEATRO)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11645067|Taller de ansiedad y estrés|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285142985689|'El mueble' (HISTRIÓN TEATRO)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11580736|GET NO - Latina|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11580799|Bengala, una vida en doce asaltos (Hortaleza)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11640435|Cavernícola|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285143361309|'Abrojo folk - El sueño que sobrevive' (ETNO SONIDO PRODUCCIONES)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285141564385|'ABBA - live in concert - 50 aniversario' (TEATRALMENTE PRODUCCIONES)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153337815|'Desgraciados' (TEATRO ATÓPICO)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285152058227|'A su servicio' (TIRITIRANTES CIRCO TEATRO)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285144835353|'Con la cabeza en las nubes' (EUGENIA MANZANERA DE LA FUENTE)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285137762140|'Con la cabeza en las nubes' (EUGENIA MANZANERA DE LA FUENTE)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11642687|Mica Mita  Cía. por humor al arte|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153751569|'Payasos de Risolandia' (PANDORA ANIMACIÓN)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285150475149|'¡El gran Cáliban! (las locas historias de un circo en miniatura)' (TEATRO ALÚA)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11643216|Las cosas que decimos, las cosas que hacemos|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413103|Là|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413111|En un sol amarillo. Memorias de un temblor|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285141280557|'La red' (KAMARU TEATRO)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153756368|'Tributo a Manolo Escobar' (LUIS ESCUDERO)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285145047183|'Con beee!! de oveja' (KAMARU TEATRO)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153352052|'Colores mágicos' (MAGIA Y CUENTACUENTOS)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11637388|Amores en Quequén|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11598526|Maliang y el pincel mágico (Tetuán)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11642694|Porque Do, porque Si Cía. Teatro Tyl Tyl|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285142371124|'Un sibarita con varita' (HÉCTOR SAN SEGUNDO)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11640419|Salvando al planeta|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285149591405|'La vida es un cuento y los cuentos sueños son' (POPY VEGAS)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285143854976|'Soliluna' (HILANDO TITERES)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285138670602|'El sótano encantado' (TEATRO MUTIS)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11638469|El profesor chiflado|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11588309|Masculinidades y sexualidad consciente|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285142194935|'La bruja Kalambres' (INNOVARTE CREACIONES ARTISTICAS)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413115|La mirada del avestruz|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11566487|Creciendo juntas|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11413096|La vida es sueño|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11566513|Batucada feminista|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153724090|'Versiones Pop Rock años 60, 70, 80, 90' (BACK TO THE COVERS)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11615773|Asesoría informática|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285152029237|'El bosque de cuentos' (CHARO JAULAR)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285145014610|'Ópera para rock para niños: Rapunzel' (FERRO TEATRO)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153767042|'Circo mágico' (CRISPÍN D'OLOT)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/10621974|Dance Studio 23|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285140678968|'¡Viva la Pepa!' (PENTACIÓN)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/11578004|Somos la guerra (Puente de Vallecas)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139492165|'Los zapateros y otras fábulas' (CUENTACUENTOS KELLER)|true|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285145381377|'Oceanía' (TRASPASOS)|true|



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

|evento|name|equipamiento|nombre|
|:----|:----|:----|:----|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153785025|'Caravana escape room - Houdini experience'' (HÉCTOR SANSEGUNDO)|http://vocab.linkeddata.es/datosabiertos/recurso/urbanismo-infraestructuras/equipamiento-municipal/equipamiento/1284236227322|Centro Cultural de la Villa (Lumbrales)|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285139023785|'Danzando por el mundo' (ARTESHOW ESPECTÁCULOS S.L.)|http://vocab.linkeddata.es/datosabiertos/recurso/urbanismo-infraestructuras/equipamiento-municipal/equipamiento/1284236227322|Centro Cultural de la Villa (Lumbrales)|



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

|name|addressRegion|
|:----|:----|
|'Vinum' (ARVINE DANZA)|Salamanca|
|Malvivir|Salamanca|
|'Cuentacuentos el libro mágico de Kolumelah' (KOLUMELAH CUENTACUENTOS)|Salamanca|
|Dystopie|Salamanca|
|Ari Tavares - Villa de Vallecas|Salamanca|
|Las desventuras de Don Quijote|Salamanca|
|Visita teatralizada: EL SECRETO DEL IRLANDÉS|Salamanca|
|Hechos luctuosos del Madrid Antiguo|Salamanca|
|La Perra Blanco - Tetuan|Salamanca|
|'Los mentalistas' (LA CHISTERA MÁGICA)|Salamanca|
|AUTOMOVILISMO|Salamanca|
|Abalconados 2020|Salamanca|
|Antonio Lizana (Latina)|Salamanca|
|'Monólogos con JJ Vaquero' (GORI PRODUCIONES)|Salamanca|
|Lichis (Puente de Vallecas)|Salamanca|
|'Caravana escape room - Houdini experience'' (HÉCTOR SANSEGUNDO)|Salamanca|
|'Cosas nuestras' (KATUA&GALEA TEATRO)|Salamanca|
|'Y tú, ¿qué sabes?... de Miguel de Cervantes' (ARAWAKE)|Salamanca|
|'Silencio' (AVANCE PRODUCCIONES TEATRALES)|Salamanca|
|'Muerte de un viajante' (OKAPI PRODUCCIONES)|Salamanca|
|'Guitarras de cine' (JESÚS PARRA)|Salamanca|
|'A vueltas con Lorca' (DOS HERMANAS CATORCE)|Salamanca|
|El Rey Sabio para niños: el ajedrez y la Torre Alfonsina |Salamanca|
|Sesiones de abordaje de la soledad|Salamanca|
|Espacio de crianza y juego libre|Salamanca|
|Taller de Beatbox - Villa de Vallecas|Salamanca|
|Jueves de Hability|Salamanca|
|Homenaje a Sara Montiel|Salamanca|
|Taller de poesía y narrativa|Salamanca|
|'La Celestina, un selfie con Melibea' (UN PINGÜINO PRODUCCIONES)|Salamanca|
|Degustación de felicidad|Salamanca|
|Las aventuras del Doctor Dolittle|Salamanca|
|Ludens Cía. La potínguele|Salamanca|
|En un muelle de Normandía|Salamanca|
|Josefina|Salamanca|
|El libro que se sentía solo|Salamanca|
|Paquete especial Semana Santa. Entradas a espacios interiores del Castillo de Lorca. (Del 14 al 17 de Abril)|Salamanca|
|'Los invisibles' (LA CORACHA TEATRO)|Salamanca|
|Círculo de mujeres: autodescubrimiento y autoestima|Salamanca|
|Mica Mita Cía. por humor al arte  TEATRO PARA BEBÉS|Salamanca|
|'Danzando por el mundo' (ARTESHOW ESPECTÁCULOS S.L.)|Salamanca|
|'Antes muerta que convicta' (BEATRIZ RICO)|Salamanca|
|EXPOSICIÓN CARTELES DE SEMANA SANTA LORCA|Salamanca|
|'Inquietante' (BAMBALUA TEATRO)|Salamanca|
|Taller de ansiedad y estrés|Salamanca|
|'El mueble' (HISTRIÓN TEATRO)|Salamanca|
|GET NO - Latina|Salamanca|
|Bengala, una vida en doce asaltos (Hortaleza)|Salamanca|
|Cavernícola|Salamanca|
|'Abrojo folk - El sueño que sobrevive' (ETNO SONIDO PRODUCCIONES)|Salamanca|
|'ABBA - live in concert - 50 aniversario' (TEATRALMENTE PRODUCCIONES)|Salamanca|
|'Desgraciados' (TEATRO ATÓPICO)|Salamanca|
|'A su servicio' (TIRITIRANTES CIRCO TEATRO)|Salamanca|
|'Con la cabeza en las nubes' (EUGENIA MANZANERA DE LA FUENTE)|Salamanca|
|Mica Mita  Cía. por humor al arte|Salamanca|
|'Payasos de Risolandia' (PANDORA ANIMACIÓN)|Salamanca|
|'¡El gran Cáliban! (las locas historias de un circo en miniatura)' (TEATRO ALÚA)|Salamanca|
|Las cosas que decimos, las cosas que hacemos|Salamanca|
|SILVESTRISMO|Salamanca|
|Là|Salamanca|
|En un sol amarillo. Memorias de un temblor|Salamanca|
|'La red' (KAMARU TEATRO)|Salamanca|
|'La Chimba' (INNOVARTE CREACIONES ARTISTICAS)|Salamanca|
|'Tributo a Manolo Escobar' (LUIS ESCUDERO)|Salamanca|
|'Con beee!! de oveja' (KAMARU TEATRO)|Salamanca|
|Visita guiada: EL CASCO ANTIGUO DE LORCA|Salamanca|
|'Colores mágicos' (MAGIA Y CUENTACUENTOS)|Salamanca|
|Amores en Quequén|Salamanca|
|'El circo de las ranas' (JUAN CATALINA)|Salamanca|
|Maliang y el pincel mágico (Tetuán)|Salamanca|
|Porque Do, porque Si Cía. Teatro Tyl Tyl|Salamanca|
|'Un sibarita con varita' (HÉCTOR SAN SEGUNDO)|Salamanca|
|Salvando al planeta|Salamanca|
|'La vida es un cuento y los cuentos sueños son' (POPY VEGAS)|Salamanca|
|'Soliluna' (HILANDO TITERES)|Salamanca|
|'El sótano encantado' (TEATRO MUTIS)|Salamanca|
|El profesor chiflado|Salamanca|
|Masculinidades y sexualidad consciente|Salamanca|
|'La bruja Kalambres' (INNOVARTE CREACIONES ARTISTICAS)|Salamanca|
|La mirada del avestruz|Salamanca|
|Creciendo juntas|Salamanca|
|La vida es sueño|Salamanca|
|Batucada feminista|Salamanca|
|'Versiones Pop Rock años 60, 70, 80, 90' (BACK TO THE COVERS)|Salamanca|
|Asesoría informática|Salamanca|
|'El bosque de cuentos' (CHARO JAULAR)|Salamanca|
|'Ópera para rock para niños: Rapunzel' (FERRO TEATRO)|Salamanca|
|'Circo mágico' (CRISPÍN D'OLOT)|Salamanca|
|Dance Studio 23|Salamanca|
|'¡Viva la Pepa!' (PENTACIÓN)|Salamanca|
|Somos la guerra (Puente de Vallecas)|Salamanca|
|Visita guiada: LORCA MONUMENTAL Y SU BORDADO|Salamanca|
|'Los zapateros y otras fábulas' (CUENTACUENTOS KELLER)|Salamanca|
|'Oceanía' (TRASPASOS)|Salamanca|




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

|name|addressLocality|
|:----|:----|
|Asesoría informática|Madrid|
|Bengala, una vida en doce asaltos (Hortaleza)|Madrid|
|Là|Madrid|
|La vida es sueño|Madrid|
|Malvivir|Madrid|
|La mirada del avestruz|Madrid|
|Dystopie|Madrid|
|En un sol amarillo. Memorias de un temblor|Madrid|
|Maliang y el pincel mágico (Tetuán)|Madrid|
|Mica Mita  Cía. por humor al arte|Madrid|
|Porque Do, porque Si Cía. Teatro Tyl Tyl|Madrid|
|Mica Mita Cía. por humor al arte  TEATRO PARA BEBÉS|Madrid|
|Ludens Cía. La potínguele|Madrid|
|Somos la guerra (Puente de Vallecas)|Madrid|
|Lichis (Puente de Vallecas)|Madrid|
|La Perra Blanco - Tetuan|Madrid|
|Cavernícola|Madrid|
|El profesor chiflado|Madrid|
|Salvando al planeta|Madrid|
|Degustación de felicidad|Madrid|
|Círculo de mujeres: autodescubrimiento y autoestima|Madrid|
|Creciendo juntas|Madrid|
|Masculinidades y sexualidad consciente|Madrid|
|Batucada feminista|Madrid|
|Homenaje a Sara Montiel|Madrid|
|Abalconados 2020|Madrid|
|Las desventuras de Don Quijote|Madrid|
|Amores en Quequén|Madrid|
|Hechos luctuosos del Madrid Antiguo|Madrid|
|Jueves de Hability|Madrid|
|Dance Studio 23|Madrid|
|Las aventuras del Doctor Dolittle|Madrid|
|En un muelle de Normandía|Madrid|
|Las cosas que decimos, las cosas que hacemos|Madrid|
|Josefina|Madrid|
|Sesiones de abordaje de la soledad|Madrid|
|Taller de ansiedad y estrés|Madrid|
|Antonio Lizana (Latina)|Madrid|
|GET NO - Latina|Madrid|
|Ari Tavares - Villa de Vallecas|Madrid|
|Taller de Beatbox - Villa de Vallecas|Madrid|
|Taller de poesía y narrativa|Madrid|
|El libro que se sentía solo|Madrid|
|Espacio de crianza y juego libre|Madrid|



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

|evento|name|startDate|
|:----|:----|:----|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153654373|'Monólogos con JJ Vaquero' (GORI PRODUCIONES)|2022-08-10T23:00:00+01:00|
|http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153751569|'Payasos de Risolandia' (PANDORA ANIMACIÓN)|2022-08-10T12:00:00+01:00|








------------------------------------------------------------------------------------------
## Nombre de los eventos que se realizan en Salamanca
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
