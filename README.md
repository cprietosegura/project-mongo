# project-mongo: localicación de oficinas

Este proyecto parte de la siguiente premisa: se ha creado un nueva empresa de la industria del gaming y **necesita una ubicación** para desarrollar su actividad. Para elegir la localización se ha hecho un estudio entre los empleados para averiguar sus preferencias. Entre ellas se han cumplido las siguientes:

- A los empleados les gustan asistir a charlas sobre su sector y estar cerca de alguna compañía del mismo gremio.
- El 30% de los trabajadores tiene al menos un hijo y necesitan que haya alguna escuela cercana.
- A los ejecutivos les gusta el café, tiene que haber alguna cafetería cerca.
- Todos los empleados tienen entre 25 y 40 años, les gustan salir de fiesta después al terminar la jornada laboral. 
- El CEO es vegano y le gusta tener opciones para comer cerca.

## Proceso

Para realizar el proyecto he partido de un dataset de Crunchbase con empresas con el que he trabajado con `MongoDB Compass` y with `pymongo`. Realicé un primer filtro para seleccionar solo las compañias relacionadas de alguna manera con el design y gaming, y que son posteriores a 2009. De entre los lugares con mayor número de compañías de este filtro, seleccioné la ciudad de Palo Alto en California, un lugar cercano a Sillicon Valley, también cerca de la prestigiosa universidad de Stanford.

Posteriormente, utilicé la `API de Yelp` para obtener las localizaciones de escuelas, restaurantes con opciones veganas, Starbucks y night clubs en Palo Alto y trasladé la información a varias collecciones en Compass, para determinar el geoindex de estos lugares.

Finalmente, desde el archivo main realizó varias geoqueries para encontrar cuál de las empresas de Palo Alto tenía alguna escuela,restaurantes vegano, night club y Starbucks en un radio de 300 metros para ubicar la oficina de la nueva empresa en la planta superior de este mismo edificio. Una vez seleccionada esta compañía ubiqué todos los lugares en un mapa con la librería `Folium` de Python.

## Documentos

En el archivo main están las geoqueries y el mapa con la localización final de la nueva compañía.

En la carpeta filtros se hayan los jupyter notebooks con los que he realizado la primera query a través de pymongo y las requests a la API, así como un dataset de aeropuertos que finalmente no he podido incorporar a la parte final del proyecto.

En input se pueden entontrar los diferentes datasets con los que he trabajado. 