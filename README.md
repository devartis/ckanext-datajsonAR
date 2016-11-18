ckanext-datajsonAR
================
Depende de: 
+ ckanext [gobAR-Theme](https://github.com/gobabiertoAR/distribuible.datos.gob.ar)
+ ckanext [Hierarchy](https://github.com/datagovuk/ckanext-hierarchy)

Extencion de CKAN forkeada de [GSA/ckanext-datajson](https://github.com/GSA/ckanext-datajson)

Link a la [Documentacion](https://github.com/GSA/ckanext-datajson/blob/master/README.md) original(EN)

Instalacion:
===========

	# Dentro del virtualenv de CKAN
	# . ruta/al/ckan_pyenv/bin/activate
	(ckan_pyenv) $ pip install pyyaml lepl jsonschema rfc3987
	(ckan_pyenv) $ pip install -e git+https://github.com/datosgobar/ckanext-datajson.git#egg=ckanext-datajson

Luego, dentro de su archivo de configuracion de CKAN, normalmente alojado en `/etc/ckan/default/config_name.ini`, agraar la sigiente linea a ckan.plugin

	ckan.plugins = (otros plugins) datajson

Change-Log:
==========
+ Cambio 1
+ Cambio 2
+ Cambio n