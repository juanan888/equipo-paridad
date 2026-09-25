## Documentación
En la Entrega 01 optamos por bases de datos individuales, lo que complicó el proceso y no era el escenario ideal para realizar nuestro proyecto periodístico. Tras los comentarios recibidos, comprendimos que acotar todo a una sola base de datos unificada nos entregaría un análisis mucho más profundo y con mejores ángulos para nuestra historia final. Por esta razón, tomamos la decisión de construir una sola tabla y nos dividimos las ediciones de los Juegos Olímpicos de Verano. A mí me correspondió investigar el primer bloque histórico: desde París 1900 hasta Berlín 1936.
Este rango temporal comprende las primeras 9 ediciones efectivas del siglo XX (considerando la cancelación de 1916). El objetivo en este tramo no era buscar la paridad, sino rastrear los "puntos de origen" de la participación femenina (por ejemplo, el debut de las mujeres en 1900 con el golf y el tenis, su entrada a la natación en Estocolmo 1912 y su tardía inclusión en el atletismo en Ámsterdam 1928).

### Proceso de limpieza y obtención de datos:

Para estructurar los datos, el primer desafío fue la inconsistencia histórica de los archivos de principios de 1900. Inicié creando una tabla en Excel donde ingresé cronológicamente las sedes. A diferencia de las ediciones modernas que trabajó mi compañera, la cantidad de disciplinas y participantes era bastante fluctuante entre una edición y otra (San Luis 1904, por ejemplo, casi no tuvo presencia femenina ni internacional).
Extraje la información de Olympedia, filtrando año por año, deporte por deporte. Debido a que las plataformas históricas presentan el dato de atletas masculinos y femeninos por separado, diseñamos las columnas "N° MUJERES" y "N° HOMBRES" de manera que, al haber un 0, evidenciara automáticamente la exclusión de un género.

Para agilizar la transformación de estos datos sueltos a una única base, utilicé herramientas de IA (Gemini). El proceso exacto fue:

1. Recopilar manualmente las cifras de participación por deporte/disciplina de cada año (1900 a 1936) desde Olympedia.
2. Ingresé esta información en crudo a Gemini a través de "bloques de años" (por ejemplo, entregándole los datos de 1900 a 1912 primero) para evitar cualquier error y pedirle que lo convirtiera en estructura CSV según las columnas que definimos con mi grupo (JJOO, AÑO, DEPORTE, DISCIPLINA, CATEGORÍA, N° MUJERES, N° HOMBRES, MEDALLA).
3. Y una vez generado el CSV, llevé el texto a Excel utilizando la función "Datos > Desde texto/CSV", verificando que los tipos de datos fueran los correctos (números enteros para los conteos, textos para las categorías).


Fuentes de datos utilizadas y justificación:

www.Olympedia.org: La elegimos al ser la base de datos de historia olímpica más exhaustiva y precisa de internet, construida por la Sociedad Internacional de Historiadores Olímpicos (ISOH).

www.Olympics.com (COI): La utilizamos para contrastar y validar la denominación oficial de los deportes (ej. "Deportes Acuáticos").

### Preguntas de investigación (Ejemplos basados en mi data):

Si armamos una tabla dinámica con esta base limpia, podríamos responder:

¿En qué año y en qué deporte se registró el primer aumento significativo de la participación femenina (pasando de menos de 10 atletas a más de 20)?

¿Cuál es el promedio de crecimiento de la participación femenina en Atletismo desde su inclusión en 1928 hasta Berlín 1936?

¿Cuántas ediciones tuvieron que pasar para que la suma total de mujeres superara, al menos, la cantidad de hombres inscritos en un solo deporte como la Gimnasia?
