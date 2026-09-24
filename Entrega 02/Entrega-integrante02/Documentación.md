En la Entrega 01 optamos por bases de datos individuales, lo que complicó el proceso y no era ideal para realizar el proyecto. Tras los comentarios recibidos en la Entrega 01, nos dimos cuenta de que acotar todo a una sola base de datos nos daría un análisis mucho más profundo y con mejores ángulos periodísticos. Por esta razón, decidimos hacer una sola tabla, que, para esta entrega cada integrante haría el período de estudio de las últimas 10/9 ediciones de los Juegos Olímpicos de Verano. En mi caso individual, desde Seúl 1988 hasta París 2024. Este rango abarca exactamente 36 años de transformaciones en el programa olímpico y permite ver el proceso de modernización del Comité Olímpico Internacional (COI) hasta llegar a la paridad global declarada en 2024.  

De esta forma, nuestra base es distinta, considerando categorías y dimensiones de análisis para cruzar los datos: 

- Disciplina específica (diferenciando, por ejemplo, en Ciclismo entre Pista, Ruta, Mountain Bike y BMX). 
- Tipo de Categoría/Evento (Femenino, Masculino, Mixto). 
- Número exacto de cupos/atletas masculinos (N_HOMBRES). 
- Número exacto de cupos/atletas femeninos (N_MUJERES). 
- Porcentaje de participación femenina por disciplina. 
- Estado de paridad (Brecha alta, Cerca de la paridad, Paridad exacta). 

Para comenzar a ordenar los datos, comenzamos por anotar las ediciones con su país, y luego fuimos escribiendo los deportes con sus disciplinas y categorías, terminando con la cantidad de participantes hombres y mujeres en Excel. El mayor problema durante el proceso de obtención de los datos es que fue extenso al tener que buscar en ciertos deportes de manera particular, al ser más “complicados” de conseguir. Estos datos los obtuvimos de Olympedia. Para ir completando los datos que nos faltaban de cada edición olímpica, decidimos apoyarnos en Gemini agrupando la información por bloques de años.  

Cuando ya teníamos todos los datos, hicimos lo siguiente para checkearlos:  
- Enviamos a Gemini los datos obtenidos por cada edición para que funcionara de manera correcta al darle menos información, y así corroborar de a poco si la información obtenida era correcta. (Ej. Mandar toda la información obtenida de Paris 2024).  
- Con la información de cada edición de los Juegos cargada en Gemini, le pedimos como prompt que nos ordenara y entregara esos datos en formato CSV, incluyendo columnas para el año, sede, deporte, disciplina específica, categoría, número de hombres, número de mujeres, y si optan a medalla.  
- Gemini nos entregaba los bloques de información listos para copiar. Estos los pasamos a Excel y ordenamos de manera correcta.  
- Con el Excel ya hecho, nos fuimos a la opción “Obtener datos”, seleccionamos “Desde un archivo CSV/Texto” e importamos. De esta forma, Excel leía el código y generaba automáticamente la información ordenada en formato de tabla.
