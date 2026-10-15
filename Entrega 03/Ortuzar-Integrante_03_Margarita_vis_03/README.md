# Documentación

## Explicación de cómo se realizó el proceso de visualización, con los pasos y decisiones tomados:  

Antes de empezar a hacer la visualización, revisé los distintos ejemplos que presenta la librería Altair, es decir, los gráficos con los que uno puede trabajar. Teniendo en cuenta las correcciones que recibimos sobre los errores de cobertura y comparabilidad en nuestros datos anteriores, entendí que no podíamos hacer un gráfico basado en filas sueltas o mal agrupadas. Con ello me di cuenta de que un gráfico de líneas (Line Chart with Point Markers) era la mejor alternativa para observar el comportamiento y la evolución del programa olímpico a lo largo de sus ediciones desde 1900 a 2024. 

Teniendo eso en consideración, entré a Google Colab, cree un cuaderno nuevo, y pegué el código que me daba Altair. Subí la base de datos corregida y completada al cuaderno, antes claramente corroborando que no hubiera celdas vacías.  

Mi objetivo era poder abordar la brecha en la oferta real de eventos competitivos, por lo que me di cuenta de que mi visualización debería abordar la relación entre el número de pruebas (hombre, mujer, mixtas o abiertas) y los años de edición. Esto se debe a que, al analizar los datos obtenidos de Olympedia, se logra suponer que la “paridad” lograda en París 2024 responde a una reestructuración acelerada en las últimas décadas, mientras que durante casi un siglo las pruebas femeninas estuvieron drásticamente relegadas o ausentes. 

Ahora, para comenzar a realizarlo en conjunto a Altair, escogí en específico el gráfico “Line Chart with Point Markers”. Decidí que las variables del gráfico debían ser: “Año de edición” en el eje X, el cual abarcaría todos los años en que hubo Juegos Olímpicos desde 1900 a 2024; y en el eje Y eje se contabilizaría el número acumulado de pruebas oficiales por año. Con 4 líneas de diversos colores, se diferenciaría entonces “N° Pruebas de Hombres”, “N° Pruebas de Mujeres”, “N° Pruebas mixtas” y “N° Pruebas abiertas”. Cada línea tendrá un color distinto para una mejor comprensión del gráfico, las cuales representan la evolución de cada categoría de prueba:
- Línea celeste para las pruebas exclusivas de Hombres. 
- Línea roja para las pruebas exclusivas de Mujeres. 
- Línea naranja para las pruebas Mixtas. 
- Línea azul para las pruebas Abiertas (Sin restricción de género) 

En conjunto con la ayuda de las IA Gemini y Claude, logré hacer unas operaciones previas a lo que iría en Colab para seleccionar las columnas de pruebas y años, además de ayudarme a agrupar el tipo de prueba según año (Ej. Todas los N° Prueba de Hombre del 2024). Cuando ya estaba listo lo previo, lo pegué en Colab. 

Luego de varios intentos fallidos, llegué a un código que parecía prometedor, lo hice correr, y funcionó. Un código con varias variantes que llevaba a hacer un gráfico de líneas de Altair para Python en Colab.  

En resumen, en este gráfico se pueden observar con total claridad las transformaciones históricas del Comité Olímpico Internacional, demostrando gráficamente cómo la brecha entre el programa masculino y femenino se fue reduciendo progresivamente con el paso de las décadas hasta converger en las ediciones más recientes. 

## Base de datos (CSV) que utilicé, cómo la procesé hasta dejarla lista para usar en la visualización que quieren hacer y por qué la seleccionaron: 

LINK 

(El CSV fue subido a la entrega) 

Previo a la construcción de mi gráfico debimos arreglar y reestructurar la versión anterior, ya que presentaba grandes errores:  
- Datos erróneos: Descubrimos que algunas cifras de atletas y división de disciplinas no coincidían con la realidad histórica de los Juegos Olímpicos. Tuve que verificar y editar los datos de manera manual, teniendo de respaldo los registros oficiales de Olympedia. 
- Falta de datos: Siguiendo con las correcciones de la Entrega 02, comprendimos la necesidad de añadir columnas que entregaran información con respecto a los tipos de pruebas que hay en los Juegos Olímpicos. Para esto, añadimos las columnas de “N° Prueba Hombres”, “N° Prueba Mujeres”, “N° Pruebas Mixtas” y “N° Pruebas Abiertas”.  
- Datos innecesarios: Teníamos unas columnas con datos innecesarios, como por ejemplo la de “Categoría” que señalaba si participaban mujeres y hombres, y la columna de “Medalla”, que señalaba si se obtenía o no medalla en el deporte. Estas columnas fueron eliminadas.  

Utilizamos esta base, ya que es la que hemos ido mejorando con las correcciones desde la Entrega 01. Además, creo que cuenta con información relevante y concreta para realizar un buen gráfico que logre dar a entender nuestra hipótesis. Para la realización del gráfico no se utilizó toda la información de la base, pero no fue necesario dividir la base, ya que las instrucciones de qué información utilizar fueron hechas en Python. 

## Ejemplos de preguntas a las que puede contestar mi visualización:  

- ¿Cómo ha cambiado la cantidad de pruebas oficiales para hombres y mujeres a lo largo de la historia de los Juegos Olímpicos (1900–2024)? 

- ¿En qué periodo histórico comenzó la verdadera aceleración e incremento de las pruebas femeninas en el programa deportivo? 

- ¿Demuestra el gráfico que la paridad lograda en París 2024 fue el resultado de un proceso de convergencia acelerado y tardío por parte del COI? 
