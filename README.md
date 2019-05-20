# Visualizador de Mapas de IDERA

	Instrucciones sobre la instalación el visualizador de mapas web de IDERA en su última versión y el servidor proxy asociado.
	El proxy es utilizado para consultar geoservidores que publican servicios WMS de IDERA y que no poseen la opción de Access-Control-Allow-Origin (CORS). El proxy agrega esta opción.

	# Pasos

	## 1. Creación de sitio de publicación

	 El visualizador debe ser publicado mediante un servidor web. Se debe crear un directorio relacionado a un sitio para la publicación del visualizador. El resto del instructivo asume que el directorio de trabajo esta publicado.

	## 2 Descargar el Visualizador ARGENMAP

	`git clone --branch ItemGroupWMSSelector https://github.com/ign-argentina/argenmap idera`

	## 3 Descargar el template del visualizador de IDERA

		cd idera
		git clone --branch develop https://github.com/ign-argentina/argenmap-leaflet-idera-tpl.git templates

	## 4 Copiar el archivo de configuración
		mv templates/argenmap-leaflet-idera-tpl/conf/menu.json js/
