# EJEMPLOS ONTOLOGIA ESAGENDA

Con la finalidad de facilitar la comprensión del uso de algunas clases y propiedades de este vocabulario se proporcionarán a continuación algunos ejemplos.

En primer lugar podemos observar la representacion de la clase **esagenda:Evento** que recoge las caracteristicas que no pueden ser encontradas en otras ontologias pero se consideran necesarias para un despliegue correcto.
Esta clase tiene como dato una lista skos que identifica los tipos de evento que se le pueden asignar (**esagenda:tipo-evento**); la ubicacion que tendra el elemento (**esageda:ubicacion**); documentacion asociada al evento (**esagenda:documentacion**); localizacion del evento para conocer su codigo postal (**schema:location**); un evento que forma parte del evento que esta sucediento (**schema:subEvent**); o un evento del que forma parte el evento que esta sucediendo (**schema:superEvent**) y conocer si un evento se va a realizar en un espacio cerrado y techado (**esagenda:interior**).
Ademas, de la clase **esagenda:Evento** se forma una subclase llamada **schema:Event** que nos proporciona las caracteristicas que deben ser encontradas en la ontologia pero que ya han sido recogidas por schema.org. Las propiedades que añadimos de esta clase son el publico objetivo (**schema:audience**); la hora de adminsion (**schema:doorTime**); la fecha de finalizacion (**schema:endDate**); el modo de asistencia (**schema:eventAttendanceMode**); el estado del evento (**schema:eventStatus**); saber si es accesible de forma gratuita (**schema:isAccessibleForFree**); la capacidad maxima (**schema:maximumAttendeeCapacity**); la fecha de inicio (**schema:startDate**); el rango de edad (**schema:typicalAgeRange**) y el trabajo realizado (**schema:workPerformed**).
```
<http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/Evento/123456> a esagenda:Evento ;
    esagenda:interior "false"^^xsd:boolean ;
    esagenda:tipo-evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/tipo-evento/futbol> ;
    esagenda:ubicacion <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/ubicacion/L123456> ;
    esagenda:documentacion <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/documentacion/123456> ;
    schema:location <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/location/123456> ; 
    schema:audience "-"^^xsd:string ;
    schema:doorTime "2022-05-25T15:30:00"^^xsd:dateTime ;
    schema:endtDate "2022-05-25T19:30:00"^^xsd:dateTime ;
    schema:eventAttendanceMode "presencial"^^xsd:string ;
    schema:isAccessibleForFree "no"^^xsd:string ;
    schema:maximumAttendeeCapacity "11.111"^^xsd:string ;
    schema:eventStatus "Por realizar"^^xsd:string ;
    schema:startDate "2022-05-35T17:30:00"^^xsd:dateTime ;
    schema:typicalAgeRange "3-99"^^xsd:string ;
    schema:workPerformed "Partido de futobol de la competicion de LaLiga"^^xsd:string .
```

A traves de la propiedad esagenda:ubicacion se establece una relacion con la clase **dbo:GovernmentalAdministrativeRegion** que nos va a servir para poder ubicar donde se va a realizar el evento. Para ello, se van a usar las clases derivadas de la ontologia dbpedia.org y de la ontologia territorio de ciudades abiertas. De estas ontologias vamos a añadir las clases de  **dbo:Province**, **dbo:District**, **dbo:Municipaly**, **dbo:Neighborhoods**, **esadm:Provincia**, **esadm:Distrito**, **esadm:Municipio**, y **esadm:Barrio**.
```
<http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/ubicacion/123456> a dbo:GovernmentalAdministrativeRegion ;
    esadm:Provincia "Comunidad de Madrid" ;
    esadm:Distrito "San Nicasio" ;
    esadm:Municipio "Leganés" ;
    esadm:Barrio "San Nicasio" .
 ```   
A traves de la propiedad esagenda:documentacion se establece una relacion con la clase **schema:CreativeWork** que nos va a servir para poder documentar la informacion relacionada con el evento. Para ello se tiene la subclase llamada **schema:DigitalDocument** con las que se añaden las propiedades que sirven para identificar a los eventos con un ID (**schema:identifier**), el nombre del evento (**schema:name**), la descripcion del evento (**schema:description**), una imagen para el evento (**schema:image**), y un enlace del evento (**schema:url**).
```
<http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/documentacion/123456> a  schema:CreativeWork ;
    schema:identifier "123456"^^xsd:string ;
    schema:name "CD Leganes - Valencia CF"^^xsd:string ;
    schema:description "Partido de semifinales de la Copa del Rey"^^xsd:string ;
    schema:image "https://www.google.com/url?sa=i&url=https%3A%2F%2Fas.com%2Ffutbol%2F2020%2F07%2F12%2Fprimera%2F1594571717_735226.html&psig=AOvVaw1CcXttttYDI8PYWnh3h-d2&ust=1648832906359000&source=images&cd=vfe&ved=0CAsQjRxqFwoTCKC_7a_r8PYCFQAAAAAdAAAAABAJ"^^xsd:string ;
    schema:url "https://www.cdleganes.com/info-partido/temporada-2016-2017/laliga-santander/6/leganes_valencia"^^xsd:string .
 ```  
A traves de la propiedad schema:location se establece una relacion con la clase schema:location que nos sirve para poder identificar la direccion en la que se va a realizar el evento. Para ello se usa la clase **esequip:Equipamiento** de la ontologia equipamiento de datos abiertos para conocer el establecimiento en el que se realiza el evento; y para saber la direccion de este se usa **esagenda:direccion**.
```
<http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/location/0758> a schema:location ;
    esequip:nombre "Estadio Municipal de Butarque" ;
    esagenda:direccion <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/direccion/123456> .
```
A traves de la propiedad schema:address se establece una relacion con la clase **schema:PostalAddress** que es la emcargada de darnos su direccion con **schema:address** y su codigo postal con **schema:postalCode**.
```
<http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/direccion/123456> a esagenda:direccion
    schema:address "C. Arquitectura, s/n,"^^xsd:string ;
    schema:postalCode "28918"^^xsd:string .
```

Finalmente, un ejemplo completo de la ontologia podria ser 
```
<http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/Evento/123456> a esagenda:Evento ;
    esagenda:interior "false"^^xsd:boolean ;
    esagenda:tipo-evento <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/tipo-evento/futbol> ;
    esagenda:ubicacion <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/ubicacion/123456> ;
    esagenda:documentacion <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/documentacion/123456> ;
    schema:location <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/location/123456> ; 
    schema:audience "-"^^xsd:string ;
    schema:doorTime "2022-05-25T15:30:00"^^xsd:dateTime ;
    schema:endtDate "2022-05-25T19:30:00"^^xsd:dateTime ;
    schema:eventAttendanceMode "presencial"^^xsd:string ;
    schema:isAccessibleForFree "no"^^xsd:string ;
    schema:maximumAttendeeCapacity "11.111"^^xsd:string ;
    schema:eventStatus "Por realizar"^^xsd:string ;
    schema:startDate "2022-05-35T17:30:00"^^xsd:dateTime ;
    schema:typicalAgeRange "3-99"^^xsd:string ;
    schema:workPerformed "Partido de futobol de la competicion de LaLiga"^^xsd:string .
    
<http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/ubicacion/123456> a dbo:GovernmentalAdministrativeRegion ;
    esadm:Provincia "Comunidad de Madrid" ;
    esadm:Distrito "San Nicasio" ;
    esadm:Municipio "Leganés" ;
    esadm:Barrio "San Nicasio" .
    
<http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/documentacion/123456> a  schema:CreativeWork ;
    schema:identifier "123456"^^xsd:string ;
    schema:name "CD Leganes - Valencia CF"^^xsd:string ;
    schema:description "Partido de semifinales de la Copa del Rey"^^xsd:string ;
    schema:image "https://www.google.com/url?sa=i&url=https%3A%2F%2Fas.com%2Ffutbol%2F2020%2F07%2F12%2Fprimera%2F1594571717_735226.html&psig=AOvVaw1CcXttttYDI8PYWnh3h-d2&ust=1648832906359000&source=images&cd=vfe&ved=0CAsQjRxqFwoTCKC_7a_r8PYCFQAAAAAdAAAAABAJ"^^xsd:string ;
    schema:url "https://www.cdleganes.com/info-partido/temporada-2016-2017/laliga-santander/6/leganes_valencia"^^xsd:string .

<http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/location/123456> a schema:location ;
    esequip:nombre "Estadio Municipal de Butarque" ;
    esagenda:direccion <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/direccion/123456> .
    
<http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/direccion/123456> a esagenda:direccion
    schema:address "C. Arquitectura, s/n,"^^xsd:string ;
    schema:postalCode "28918"^^xsd:string .
```
