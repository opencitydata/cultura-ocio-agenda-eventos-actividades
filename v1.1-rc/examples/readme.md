# Examples
La descripción de los archivos que podemos encontrar:

## datos.csv
Conjunto de datos que han sido obtenidos de los portales de ciudades abiertas. Las ciudades en las que se han consultado los eventos son:

* Madrid

	* http://datos.munimadrid.es/sites/v/index.jsp?vgnextoid=57be24206a91b510VgnVCM2000001f4a900aRCRD&vgnextchannel=374512b9ace9f310VgnVCM100000171f5a0aRCRD

	* Origen de los datos: Datos abiertos del ayuntamiento de Madrid
	* Licencia: https://datos.madrid.es/egob/catalogo/aviso-legal 
	
* Salamanca
	* https://analisis.datosabiertos.jcyl.es/explore/dataset/eventos-de-la-agenda-cultural-categorizados-y-geolocalizados/table/?refine.nombre_provincia=Salamanca&refine.fecha_inicio=2022

	* Origen de los daots: Datos abiertos de la comunidad de Castilla y Leon
	* Licencia: https://creativecommons.org/licenses/by/4.0/deed.es_ES
	
* Lorca
	* https://datosabiertos.regiondemurcia.es/ayuntamiento-de-lorca/catalogo/cultura-ocio/agenda-cultural-lorca
	* Origen de los datos: Datos abiertos de la Región de Murcia.
	* Licencia: http://datos.lorca.es/avisolegal

## config.ini
Fichero que contiene la configuracion de Morph-KGC.

## mapping.rml
Archivo que contiene el mapping RML para estructurar los datos del CSV para realizar la generacion de RDF de acuerdo con el vocabulario.

### Atributos: 
* **audience**: Reprensenta el público al que va dirigido el evento.
* **maximumAttendeeCapacity**: Representa el número total de personas que pueden asistir al evento.
* **postalCode**: Representa el código postal.
* **description**: Representa la descripción del evento.
* **streetAddress**: Representa la dirección de la calle.
* **addressLocality**: Representa la localidad en la que tendrá lugar el evento
* **addressRegion**: Representa la región en la que tendrá lugar el evento
* **url**: Representa el enlace del evento.
* **isAccessibleForFree**:Representa si el evento es accesible de forma gratuita
* **eventStatus**: Representa el estado del evento
* **endDate**: Representa la fecha y la hora de finalización del evento.
* **startDate**: Representa la fecha y la hora de inicio del evento.
* **fileFormat**: Representa el tipo de archivo donde se encuentra la descripción del evento
* **doorTime**: Representa la hora de unicio de adminisión al evento
* **identifier**: Representa el identificar del evento
* **id**: Representa el identificador del lugar donde se producirá el evento.
	
	Para obtener los identificadores del equipamiento donde tienen lugar los eventos se ha buscado los datos abiertos relacionados con las instalaciones de las siguientes ciudades:

	* Madrid

		* https://datos.madrid.es/sites/v/index.jsp?vgnextoid=2f115117d05b3410VgnVCM1000000b205a0aRCRD&vgnextchannel=374512b9ace9f310VgnVCM100000171f5a0aRCRD
		* Origen de los datos: Datos abiertos del ayuntamiento de Madrid
		* Licencia: https://datos.madrid.es/egob/catalogo/aviso-legal 

	* Salamanca: 
		* https://datosabiertos.jcyl.es/web/jcyl/set/es/cultura-ocio/infraestructuras_culturales/1284305389968
		* Origen de los daots: Datos abiertos de la comunidad de Castilla y Leon
		* Licencia: https://creativecommons.org/licenses/by/4.0/deed.es_ES
	* Lorca:
		* https://datos.lorca.es/catalogo/monumentos y https://datos.lorca.es/catalogo/servicios
		* Origen de los datos: Datos abiertos de la Región de Murcia.
		* Licencia: http://datos.lorca.es/avisolegal

* **image**: Representa la imagen del evento
* **interior**: Representa si un evento tiene lugar en un sitio cerrado.
* **eventAttendanceMode**: Representa el modo de asistencia de un evento
* **name**: Representa el Nombre del lugar donde se realiza el evento.
* **nombre**: Representa el nombre del evento.
* **typicalAgeRange**: Representa el rango de edad para el que va destinado el evento
* **workPerformed**: Representa el trabajo realizado en algun evento.


## output.nt
Resultado de procesar los datos a través de Morph-KGC con el archivo mapping.rml



