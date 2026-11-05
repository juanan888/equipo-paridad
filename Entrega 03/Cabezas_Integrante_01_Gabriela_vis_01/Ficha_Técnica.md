# Ficha Técnica de la Base de Datos
## Características generales de los datos
* Formato: Archivo CSV delimitado por comas (database_ocupada.csv).
* Unidad de análisis: Registro de la oferta de pruebas con medalla y participación de atletas, desglosado por disciplina y edición olímpica.
* Período temporal: 1900 – 2024.
* Fuentes principales: Registros históricos del Comité Olímpico Internacional (COI) y base de datos independiente Olympedia.

## Variables extraídas para la visualización: 
Para el gráfico de áreas apiladas absolutas que evidencia la contención del programa masculino, el script filtró y agrupó exclusivamente las variables AÑO, N°PRUEBAS HOMBRES, N° PRUEBAS MUJERES, N° PRUEBAS MIXTAS y N° PRUEBAS ABIERTAS.

Variables incorporadas:

* JJOO: Ciudad anfitriona donde se realizó la edición de los Juegos Olímpicos.
* AÑO:	Año correspondiente a la edición olímpica.
* DEPORTE:	Categoría general del deporte oficial dentro del programa olímpico (ej. Deportes Acuáticos).
* DISCIPLINA:	Rama específica o subcategoría dentro de cada deporte (ej. Natación, Saltos, Waterpolo).
* N° PRUEBAS HOMBRES:	Cantidad de competencias oficiales (con medallas a repartir) destinadas exclusivamente a hombres.
* N° PRUEBAS MUJERES:	Cantidad de competencias oficiales (con medallas a repartir) destinadas exclusivamente a mujeres.
* N° PRUEBAS MIXTAS:	Cantidad de competencias oficiales estructuradas para equipos o dúos que pueden ser integrados por ambos géneros.
* N° PRUEBAS ABIERTAS:	Cantidad de competencias oficiales donde hay restricción de género para participar (históricamente común en ecuestre).
* N° MUJERES:	Cantidad absoluta de atletas mujeres participantes registradas en esa disciplina.
* N° HOMBRES:	Cantidad absoluta de atletas hombres participantes registrados en esa disciplina.
* LINK:	Enlace URL directo a la fuente de Olympedia para la trazabilidad y verificación del registro.

## Observaciones sobre la base de datos
La base de datos actual es el resultado de un proceso de limpieza y revisión largo tras las correcciones iniciales del proyecto. Eliminamos columnas redundantes que no aportaban al análisis, corregimos inconsistencias y agregamos datos y disciplinas que se habían omitido en su primera versión.
