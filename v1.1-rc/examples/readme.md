# Examples
La descripción de los archivos que podemos encontrar:

## datos.csv
Conjunto de datos que han sido obtenidos de los portales de ciudades abiertas de las ciudades de [Madrid](http://datos.munimadrid.es/portal/site/egob/menuitem.c05c1f754a33a9fbe4b2e4b284f1a5a0/?vgnextoid=57be24206a91b510VgnVCM2000001f4a900aRCRD&vgnextchannel=374512b9ace9f310VgnVCM100000171f5a0aRCRD&vgnextfmt=default), [Salamanca](https://analisis.datosabiertos.jcyl.es/explore/dataset/eventos-de-la-agenda-cultural-categorizados-y-geolocalizados/table/?refine.nombre_provincia=Salamanca&refine.fecha_inicio=2022) y [Lorca](https://datosabiertos.regiondemurcia.es/ayuntamiento-de-lorca/catalogo/cultura-ocio/agenda-cultural-lorca).

Para obtener los ID del equipamiento donde tienen lugar los eventos se ha buscado los datos abiertos relacionados con las instalaciones. Se han encontrado los de [Madrid](https://datos.madrid.es/sites/v/index.jsp?vgnextoid=2f115117d05b3410VgnVCM1000000b205a0aRCRD&vgnextchannel=374512b9ace9f310VgnVCM100000171f5a0aRCRD), [Salamanca](https://datosabiertos.jcyl.es/web/jcyl/set/es/cultura-ocio/infraestructuras_culturales/1284305389968), [Lorca monumentos](https://datos.lorca.es/catalogo/monumentos) y [Lorca servicios](https://datos.lorca.es/catalogo/servicios)

## mapping.rml
Archivo que estructura los datos del CSV basándonos en nuestro vocabulario para que sean procesados por rmlmapper. Los datos serán procesados y obtendremos un resultado acorde a nuestra ontología. 

## output.nt
Resultado de procesar los datos a través de rmlmapper con el archivo mapping.rml



