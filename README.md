ckanext-datajsonAR
==================
La extensión de CKAN `datajsonAR`, fue confeccionada dentro del marco del plan de `Datos Abiertos` de la República Argentina e incluida dentro del proyecto [portal andino](https://github.com/datosgobar/portal-andino), en función de que el mismo pueda asi cumplir con estándares de calidad para la confección de metadata para catálogos de datos [DCAT](https://www.w3.org/TR/vocab-dcat) propuestos por la World Wide Web Consortium([W3C](www.w3c.es)). 
Este desarrollo es un fork del trabajo realizado por la [GSA](https://github.com/GSA), con la extensión para CKAN, [GSA/ckanext-datajson](https://github.com/GSA/ckanext-datajson)


+ [Instalacion de la Extensión](#instalacion-de-la-extensión)
    + [Pre requisitos](#pre-requisitos)

##### Instalación de la Extensión:
###### Pre requisitos:
+ Python 2.7.x 
+ CKAN 2.5.2
+ ckanext [gobAR-Theme](https://github.com/gobabiertoAR/distribuible.datos.gob.ar)
+ ckanext [Hierarchy](https://github.com/datagovuk/ckanext-hierarchy)
+ ckanext [Harvest](https://github.com/ckan/ckanext-harvestt)

##### Proceso de instalación de la extensión datajsonAR
```bash
# Dentro del virtualenv de CKAN
# . ruta/al/ckan_pyenv/bin/activate
(ckan_pyenv) $ pip install pyyaml lepl jsonschema rfc3987
(ckan_pyenv) $ pip install -e git+https://github.com/datosgobar/ckanext-datajson.git#egg=ckanext-datajson
```
Dentro del apartado `[app:main]` de la configuracion de CKAN `(/etc/ckan/default/ckan_config.ini)` agregar los siguientes campos:
```bash
[app:mail]
ckan.owner = entidad-responsable-del-portal
ckan.owner.email = mail@entidad-responsable-del-portal.xxx # si este campo no se define, esta info se tomara del area de "contacto" de GobAr-Theme
```
Luego, dentro de su archivo de configuracion de CKAN, normalmente alojado en `/etc/ckan/default/config_name.ini`, agregar la siguiente linea en la sección de `[plugins]` a `ckan.plugins`

	ckan.plugins = (otros plugins) datajson

##### Probado que todo funciona:
Para saber que el proceso de instalación se realizo con exito, solo debemos tipear, en un navegador:
	
	http://{tu_host}/data.json

Y deberíamos ver una respuesta similar a esta:
```JSON
{
    "title": "Título del portal",
    "desciption": "Descripcion del portal",
    "superThemeTaxonomy": "http://datos.gob.ar/superThemeTaxonomy.json",
    "publisher": {
        "mbox": "email@decontacto.xxx",
        "name": "Nombre de la persona o institución responsable de la instancia CKAN."
},
	"themeTaxonomy": [],
	"dataset": []
}
```
##### Usage:
Customizacion....


##### Tests:
*WIP*

##### Credits / Copying
El presente desarrollo es un fork del trabajo de la [GSA](link), [GSA/ckanext-datajson](https://github.com/GSA/ckanext-datajson) y podes visitarlo [Aquí](https://github.com/GSA/ckanext-datajson/blob/master/README.md) (EN).
##### Contacto:
Este proyecto es en desarrollo, si viste algun `bug`, por favor, **creanos un issue**.

##### Comentarios o preguntas?
Escribinos a `datos@modernizacion.gob.ar`
