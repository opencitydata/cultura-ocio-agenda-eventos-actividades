# Ejemplo USO

Con la finalidad de facilitar la comprensión del uso de algunas clases y propiedades de este vocabulario se proporcionarán a continuación algunos ejemplos.

En primer lugar podemos observar la representacion de la clase [esagenda:Evento](#Evento "http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#Evento") que recoge las caracteristicas que no pueden ser encontradas en otras ontologias pero se consideran necesarias para un despliegue correcto.

La clase [esagenda:Evento](#Evento "http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#Evento") tiene como datos una lista skos que identifica los tipos de evento que se le pueden asignar ([esagenda:tipo-evento](#/tipo-evento "http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/tipo-evento")); la ubicacion que tendra el elemento ([esagenda:ubicacion](#ubicacion "http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#ubicacion")); documentacion asociada al evento ([esagenda:documentacion](#documentacion "http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion")); localizacion del evento para conocer su codigo postal ([esagenda:localizacion](#location "http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#location")); un evento que forma parte del evento que esta sucediento ([schema:subEvent](#http://schema.org/subEvent "http://schema.org/subEvent")); o un evento del que forma parte el evento que esta sucediendo ([schema:subEvent](#http://schema.org/superEvent "http://schema.org/superEvent")) y conocer si un evento se va a realizar en un espacio cerrado y techado ([esagenda:interior](#interior "http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#interior")).

Ademas, de la clase [esagenda:Evento](#Evento "http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#Evento") se forma una subclase llamada [schema:Event](#http://schema.org/Event "http://schema.org/Event") que nos proporciona las caracteristicas que deben ser encontradas en la ontologia pero que ya han sido recogidas por [schema.org](http://schema.org). Las propiedades que añadimos de esta clase son el publico objetivo ([schema:audiencia](#http://schema.org/audience "http://schema.org/audience")); la hora de adminsion ([schema:hora de apertura de puertas](#http://schema.org/doorTime "http://schema.org/doorTime")); la fecha de finalizacion ([schema:fecha fin](#http://schema.org/endDate "http://schema.org/endDate")); el modo de asistencia ([schema:modo de asistencia al evento](#http://schema.org/eventAttendanceMode "http://schema.org/eventAttendanceMode")); el estado del evento ( [schema:estado del evento](#http://schema.org/eventStatus "http://schema.org/eventStatus")); saber si es accesible de forma gratuita ([schema:es accesible gratis](#http://schema.org/isAccessibleForFree "http://schema.org/isAccessibleForFree")); la capacidad maxima ([schema:capacidad maxima](#http://schema.org/maximumAttendeeCapacity "http://schema.org/maximumAttendeeCapacity")); la fecha de inicio ([schema:fecha inicio](#http://schema.org/startDate "http://schema.org/startDate")); el rango de edad ([schema:rango edad](#http://schema.org/typicalAgeRange "http://schema.org/typicalAgeRange")) y el trabajo realizado ([schema:trabajo realizado](#http://schema.org/workPerformed "http://schema.org/workPerformed")).

    
    <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/Evento/123456> a esagenda:Evento ;
       esagenda:interior "false"^^xsd:boolean ;
       esagenda:tipo-evento <http://vocab.linkeddata.es/page/datosabiertos/kos/cultura-ocio/agenda/tipo-evento/futbol> ;
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
             

A traves de la propiedad [esagenda:ubicacion](#ubicacion "http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#ubicacion") se establece una relacion con la clase [dbo:Región Administrativa Gubernamental](#http://dbpedia.org/ontology/GovernmentalAdministrativeRegion "http://dbpedia.org/ontology/GovernmentalAdministrativeRegion") que nos va a servir para poder ubicar donde se va a realizar el evento. Para ello, se van a usar las clases derivadas de la ontologia [dbpedia.org](http://dbpedia.org) y de la ontología territorio de ciudades abiertas. De estas ontologías vamos a añadir las clases de [dbo:Province](#http://dbpedia.org/ontology/Province "http://dbpedia.org/ontology/Province"), [dbo:District](#http://dbpedia.org/ontology/District "http://dbpedia.org/ontology/District"), [dbo:Municipaly](#http://dbpedia.org/ontology/Municipaly "http://dbpedia.org/ontology/Municipaly"), [dbo:Neighborhood](#http://dbpedia.org/ontology/Neighborhoods "http://dbpedia.org/ontology/Neighborhoods"), [esadm:Provincia](#http://vocab.linkeddata.es/datosabiertos/def/sector-publico/territorio#Provincia "http://vocab.linkeddata.es/datosabiertos/def/sector-publico/territorio#Provincia"), [esadm:Distrito](#http://vocab.linkeddata.es/datosabiertos/def/sector-publico/territorio#Distrito "http://vocab.linkeddata.es/datosabiertos/def/sector-publico/territorio#Distrito"), [esadm:Municipio](#http://vocab.linkeddata.es/datosabiertos/def/sector-publico/territorio#Municipio "http://vocab.linkeddata.es/datosabiertos/def/sector-publico/territorio#Municipio"), y [esadm:Barrio](#http://vocab.linkeddata.es/datosabiertos/def/sector-publico/territorio#Barrio "http://vocab.linkeddata.es/datosabiertos/def/sector-publico/territorio#Barrio").

    
    <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/ubicacion/123456> a dbo:GovernmentalAdministrativeRegion ;
       esadm:Provincia "Comunidad de Madrid" ;
       esadm:Distrito "San Nicasio" ;
       esadm:Municipio "Leganés" ;
       esadm:Barrio "San Nicasio" .
               

A traves de la propiedad [esagenda:documentacion](#documentacion "http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#documentacion") se establece una relacion con la clase [schema:Trabajo Creativo](#http://schema.org/CreativeWork "http://schema.org/CreativeWork") que nos va a servir para poder documentar la informacion relacionada con el evento. Para ello se tiene la subclase llamada [schema:Documento Digital](#http://schema.org/DigitalDocument "http://schema.org/DigitalDocument") con las que se añaden las propiedades que sirven para identificar a los eventos con un ID ([schema:identificador](#http://schema.org/identifier "http://schema.org/identifier")), el nombre del evento ([schema:nombre](#http://schema.org/name "http://schema.org/name")), la descripcion del evento ([schema:descripcion](#http://schema.org/description "http://schema.org/description")), una imagen para el evento ([schema:imagen](#http://schema.org/image "http://schema.org/image")), y un enlace del evento ([schema:url](#http://schema.org/url "http://schema.org/url")).

    
    <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/documentacion/123456> a schema:CreativeWork ;
       schema:identifier "123456"^^xsd:string ;
       schema:name "CD Leganes - Valencia CF"^^xsd:string ;
       schema:description "Partido de semifinales de la Copa del Rey"^^xsd:string ;
       schema:image "https://www.google.com/url?sa=i&url=https%3A%2F%2Fas.com%2Ffutbol%2F2020%2F07%2F12%2Fprimera%2F1594571717_735226.html&psig=AOvVaw1CcXttttYDI8PYWnh3h-d2&ust=1648832906359000&source=images&cd=vfe&ved=0CAsQjRxqFwoTCKC_7a_r8PYCFQAAAAAdAAAAABAJ"^^xsd:string ;
       schema:url "https://www.cdleganes.com/info-partido/temporada-2016-2017/laliga-santander/6/leganes_valencia"^^xsd:string .
                

A traves de la propiedad [esagenda:localizacion](#location "http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#location") se establece una relacion con la clase [schema:Lugar](#http://schema.org/Place "http://schema.org/Place") que nos sirve para poder identificar la direccion en la que se va a realizar el evento. Para ello se usa la clase [esequip:nombre](#http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras/equipamiento#nombre "http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras/equipamiento#nombre") de la ontología equipamiento de datos abiertos para conocer el establecimiento en el que se realiza el evento; y para saber la direccion de este se usa [esagenda:direccion](#direccion "http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#direccion").

    
    <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/location/123456> a schema:location ;
       esequip:nombre "Estadio Municipal de Butarque" ;
       esagenda:direccion <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/direccion/123456> .
                

A traves de la propiedad [esagenda:direccion](#direccion "http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda#direccion") se establece una relacion con la clase [schema:Direccion Postal](#http://schema.org/PostalAddress "http://schema.org/PostalAddress") que es la encargada de darnos su direccion con [schema:direccion](#http://schema.org/address "http://schema.org/address") y su codigo postal con [schema:codigo postal](#http://schema.org/postalCode "http://schema.org/postalCode").

    
    <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/direccion/123456> a esagenda:direccion
       schema:address "C. Arquitectura, s/n,"^^xsd:string ;
       schema:postalCode "28918"^^xsd:string .
                

Finalmente, un ejemplo completo de la ontologia podria ser

    
    <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/Evento/123456> a esagenda:Evento ;
       esagenda:interior "false"^^xsd:boolean ;
       esagenda:tipo-evento <http://vocab.linkeddata.es/page/datosabiertos/kos/cultura-ocio/agenda/tipo-evento/futbol> ;
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
    
    <http://vocab.linkeddata.es/datosabiertos/def/cultura-ocio/agenda/documentacion/123456> a schema:CreativeWork ;
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