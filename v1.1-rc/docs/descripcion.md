# 3. Descripcion

Para representar un evento se tiene el concepto esagenda:evento para el cual se reutilizan las clases schema:Event, schema:DigitalDocument, schema:CreativeWork, schema:Place y schema:PostalAddress del vocabulario schema, y esequip:Equipamiento del vocabulario esequip.

Para poder implementar la información que ya se encuentran desarrolladas sobre eventos en el vocabulario schema.org, se ha establecido que esagenda:evento es subclase de schema:event. En cambio, para representar que un evento debe de tener asociado un archivo digital (que puede ser desde una página web o un archivo PDF), se ha establecido la relación con la clase schema:DigitalDocument a traves de la propiedad esagenda:documentación. Finalmente, como un evento debe de guardar información sobre el lugar en que se llevara a cabo, se ha decidido relacionar esagenda:evento con la clase schema:Place a través de la propiedad schema:location.

Para añadir al vocabulario los datos que deben de ser añadidos a la hora de documentar el evento en el fichero digital que creamos oportuno, se ha establecido que schema:DigitalDocument es subclase de schema:CreativeWork.

Con la finalidad de representar el equipamiento donde puede tener lugar el evento, se ha implantado que esequip:equipamiento es subclase de schema:Place. Además, para situar el equipamiento que se ha mencionado anteriormente, se ha establecido una relación a través de la propiedad schema:address entre schema:Place y la clase schema:PostalAddress.

Adicionalmente, en este vocabulario se ha utilizado un esquema de conceptos SKOS llamado esagenda:tipo-evento para representar el tipo de evento que puede ser. Los valores se han especificado en <http://vocab.linkeddata.es/datosabiertos/kos/cultura-ocio/agenda>

## 3.1 Ejemplos de uso

Con la finalidad de facilitar la compresión del uso de algunas clases y propiedades de este vocabulario, se proporcionarán a continuación algunos ejemplos.

En primer lugar, para la representación de un evento se crea una instancia de la clase esagenda:evento con las propiedades schema:isAccesibleForFree (indica si el acceso el gratuito), schema:eventStatus (indica el estado), schema:eventAttendanceMode (indica el modo de asistencia), schema:workPerformed (indica el trabajo que se realiza), schema:doorTime (indica la hora a la que se puede acceder), schema:audience (indica el público recomendado), schema:startDate (indica la fecha y hora a la que empieza), schema:endDate (indica la fecha y hora a la que finaliza), schema:maximunAttendeeCapacity (indica el máximo de personas que pueden asistir), schema:typicalAgeRange (indica la edad recomendada), esagenda:interior (indica si está techado el lugar). Asimismo, se enlace a través de la propiedad esagenda:tipoEvento, el tipo de evento con el concepto correspondiente de la taxonomía del tipo de evento. Finalmente, el evento se relaciona con una instancia de schema:CreativeWork y esequip:Equipamiento.

<http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153785025> a esagenda:Evento
    schema:audience  "Público familiar" ; 
    schema:startDate "2022-08-12T22:00+01:00"^^xsd:dateTime ;
    schema:endDate "2022-08-13T01:00+01:00"^^xsd:dateTime ;
    schema:eventAttendanceMode "Presencial" ;
    schema:isAccesibleForFree "false"^^xsd:boolean ;
    schema:maximunAttendeeCapacity "301" ;
    schema:eventStatus "Por empezar ;
    schema:typicalAgeRange "0-" ;
    esagenda:tipoEvento <http://vocab.linkeddata.es/datosabiertos/kos/cultura-ocio/agenda/tipo-evento/teatro> ;
    esagenda:documentacion <http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153785025/documentacion> ;
    esequip:Equipamiento <http://vocab.linkeddata.es/datosabiertos/recurso/urbanismo-infraestructuras/equipamiento-municipal/equipamiento/1284236227322> .


A continuación se representa una instancia de schema:CreativeWork con las propiedades dct:identifier (indica el identificador), schema:name (indica el nombre), schema:description (indica la descripción), schema:imagen (indica la imagen promocional), schema:url (indica el enlace donde se encuentra la información), schema:FileFormat (indica el formato donde está la información).

<http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153785025/documentacion> a esagenda:Documentacion
    dct:identifier "1285153785025" ;
    schema:name "'Caravana escape room - Houdini experience' (HÉCTOR SANSEGUNDO)" ;
    schema:description "Disfruta de una mezcla perfecta de espectáculo de teatro y magia dentro de un museo inversivo , y forma parte de la historia viviendo un escape room único, original y con sorpresas inolvidables."; 
    schema:image "https://cultura.jcyl.es/web/jcyl/binarios/744/545/CARAVANA%20LA%20MAQUINA.jpeg"^^xsd:anyURI ;
    schema:url "https://cultura.jcyl.es/web/jcyl/Cultura/es/Plantilla100Detalle/1284282053297/Evento/1285153785025/Comunicacion"^^xsd:anyURI ;
    schema:fileFormat "HTML" .

A continuación se va a representar una instancia de esequip:Equipamiento con las propiedades dct:identifier (indica el identificador) y esequip:nombre (indica el nombre). Finalmente, el equipamiento se relaciona a través de la propiedad schema:address con una instancia de schema:PostalAddress

<http://vocab.linkeddata.es/datosabiertos/recurso/urbanismo-infraestructuras/equipamiento-municipal/equipamiento/1284236227322> a esequip:Equipamiento
    dct:identifier "1284236227322" ;
    esequip:nombre "Centro Cultural de la Villa (Lumbrales)" ;
    schema:address <http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153785025/address> .

A continuación se va a representar una instancia de schema:PostalAddress con las propiedades schema:addressRegion (indica la provincia), schema:addressLocality (indica el municipio), schema:postalCode (indica el código postal), schema:streetAddress (indica la dirección)

<http://vocab.linkeddata.es/datosabiertos/recurso/cultura-ocio/agenda/evento/1285153785025/address> a schema:Address
    schema:addressRegion "Salamanca" ;
    schema:addressLocality "Lumbrales" ;
    schema:postalCode "37240" ;
    schema:streetAddress "Plaza Mayor, 1" .
