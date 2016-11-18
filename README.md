ckanext-datajsonAR
================
Descripcion Narrativa de contexto y dependencias
parte del proyecto (portal_andino)[link_a_portal_andino]

Extencion de CKAN forkeada de [GSA/ckanext-datajson](https://github.com/GSA/ckanext-datajson)

Link a la [Documentacion](https://github.com/GSA/ckanext-datajson/blob/master/README.md) original(EN)

TOC:
===

Instalacion:
===========
dependencias:
Depende de:
+ Python 2.7.x 
+ CKAN 2.5.2
+ ckanext [gobAR-Theme](https://github.com/gobabiertoAR/distribuible.datos.gob.ar)
+ ckanext [Hierarchy](https://github.com/datagovuk/ckanext-hierarchy)
+ ckanext [Harvest](link_a_harvest)


	# Dentro del virtualenv de CKAN
	# . ruta/al/ckan_pyenv/bin/activate
	(ckan_pyenv) $ pip install pyyaml lepl jsonschema rfc3987
	(ckan_pyenv) $ pip install -e git+https://github.com/datosgobar/ckanext-datajson.git#egg=ckanext-datajson

Luego, dentro de su archivo de configuracion de CKAN, normalmente alojado en `/etc/ckan/default/config_name.ini`, agregar la sigiente linea en la seccion de `[plugins]` a `ckan.plugins`

	ckan.plugins = (otros plugins) datajson

test de que esta todo OK
	
	http://{tu_host}/data.json

Usage:
=====
Customizacion....


Tests:
=====
*WIP*

Credits / Copy
nos -> UK -> US


Contacto:
Este proyecto es en desarrollo, si viste algun bug, creanos un issue.

Comentarios o preguntas?
escribinos a datos@modernizacion.gob.ar