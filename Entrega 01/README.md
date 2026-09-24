# Proyecto 
De París 1900 a París 2024: La evolución de la paridad de género y brechas de disciplina en los Juegos Olímpicos.  

## Síntesis 

Desde el nacimiento de los Juegos Olímpicos de Atenas 1896, este evento se ha posicionado como uno de los más importantes del mundo deportivo. Sin embargo, este espacio no ha estado libre de sesgos e inequidades, estando la participación femenina fuertemente restringida por muchos años, en especial por prejuicios culturales e institucionales sobre qué disciplinas y niveles se consideraban “aptos” para el cuerpo femenino.  

En los Juegos Olímpicos de París 1900, la participación femenina fue marginal, con un 2,2% del total de atletas (22 de 997 participantes), y estaban concentradas en solamente cinco deportes (tenis, vela, crocket, hípica y golf). 124 años después, los juegos de 2024 toman lugar en la misma sede, donde el Comité Olímpico Internacional anunció un hito histórico: por primera vez en la historia de los Juegos Olímpicos se alcanzó la paridad de género numérica, con 5.250 participantes mujeres y 5.250 hombres.  

A pesar del valor que tiene este anuncio, la paridad numérica no significa que en realidad exista una paridad absoluta dentro de este evento. Todavía persisten diferencias en la cantidad de cupos por disciplina, la proporción de pruebas que otorgan medallas y el número de eventos femeninos que estén programados para en horarios de máxima audiencia.  

Con este contexto, nuestro proyecto busca analizar, mediante el uso de bases de datos y la recolección de información de estos 124 años históricos (1900-2024), la evolución cuantitativa del acceso femenino a los Juegos Olímpicos. A través del cruce entre participación, disciplinas y oportunidades de medalla, pretendemos determinar si el 50/50 anunciado por el Comité el 2024 representa una verdadera paridad de género dentro de los Juegos o si todavía existen brechas ocultas dentro de esta cifra.  

## Pregunta de investigación 

¿El 50/50 anunciado por el Comité Olímpico Internacional en los Juegos de París 2024 representa una verdadera paridad de género?  

## Hipótesis 

Aunque en París 2024 se alcanzó una por primera vez una paridad de género numérica entre la cantidad de participantes mujeres y hombres, esta igualdad no se replica necesariamente dentro de las propias disciplinas ni en las oportunidades competitivas disponibles para los deportistas, por lo que el 50/50 no representa una equidad de género absoluta en los Juegos Olímpicos.  

## Antecedentes 

La participación femenina en los Juegos Olímpicos ha aumentado progresivamente durante el último siglo. París 1900 marcó la primera participación oficial de mujeres, aunque en una escala muy reducida. Olympedia señala que las primeras participantes oficiales compitieron en croquet, equitación, golf, vela y tenis. 

La propia historia de los Juegos muestra que el acceso femenino no avanzó de manera homogénea. Durante décadas, numerosas disciplinas estuvieron restringidas a los hombres. Un ejemplo particularmente ilustrativo es el boxeo: las mujeres participaron por primera vez en este deporte olímpico recién en Londres 2012. 

El crecimiento de la participación femenina se aceleró especialmente durante las últimas décadas. Según el movimiento olímpico, las mujeres pasaron de representar un 2,2% de los participantes en París 1900 a un 23% en Los Ángeles 1984, 44% en Londres 2012 y 48% en Tokio 2020. París 2024 fue presentado como el primer Juego Olímpico con una distribución 50:50 de las plazas de atletas. 

La discusión contemporánea, por lo tanto, ha comenzado a desplazarse desde la pregunta sobre cuántas mujeres participan hacia una pregunta más amplia sobre en qué condiciones participan. La existencia de eventos masculinos, femeninos y mixtos permite analizar si la igualdad numérica general también se refleja en la distribución de oportunidades. En París 2024, por ejemplo, hubo 22 eventos mixtos, cuatro más que en Tokio 2020. 

Además, algunos deportes continúan presentando diferencias estructurales. En fútbol, por ejemplo, París 2024 contó con 16 equipos masculinos y 12 femeninos, pese al objetivo general de igualdad en el número de atletas. 

Nuestro proyecto busca aportar a esta discusión desde una perspectiva de datos. En lugar de estudiar únicamente la evolución general de la participación femenina, se desagregarán los datos para observar las diferencias existentes entre deportes y eventos y determinar si la paridad general oculta desigualdades internas. 

## Datos 

Para comprobar la hipótesis será necesario construir una base histórica que permita comparar las distintas ediciones de los Juegos Olímpicos de verano entre 1900 y 2024. 

1. Datos necesarios:  
- Año de los juegos. 
- Ciudad sede. 
- Número total de atletas. 
- Número de atletas mujeres. 
- Número de atletas hombres. 
- Porcentaje de participación femenina. 
- Deporte. 
- Disciplina/evento. 
- Sexo o categoría del evento. 
- Número de participantes por sexo. 
- Número de eventos masculinos. 
- Número de eventos femeninos. 
- Número de eventos mixtos. 
- Medallas entregadas por sexo/categoría. 
- Número de países participantes, como variable contextual. 

2. Datos que ya tenemos: 

Bases históricas disponibles públicamente que contienen información de atletas y reusltados olímpicos. Una alternativa de apoyo es el conjunto histórico basado en OLympedia disponible en Kaggle, que reúne información de atletas y resultados desde 1896 y contiene datos de más de 150.000 atletas. 

También existen bases que incorporan los Juegos hasta París 2024, con variables como atleta, sexo, país, año, deporte, evento y medalla. Estas bases podrán utilizarse como material de apoyo, pero sus datos serán contrastados con fuentes oficiales e históricas antes de incorporarlos a la base definitiva. 

3. Datos que necesitamos conseguir o construir 

La principal tarea será construir una base propia que permita relacionar tres niveles: Edición > deporte/disciplina > evento.  

Esto permitirá evitar que la investigación se limita al número total de participantes y posibilitará calcular diferencias específicas entre mujeres y hombres.  

También será necesario revisar y corregir manualmente aquellos registros históricos que presenten inconsistencias de clasificación, especialmente para las primeras ediciones.  

4. Datos que no existen como única base 

No contamos con una única base histórica que entregue de manera homogénea todas las variables que necesitamos desde París 1900 hasta París 2024. 

Por esta razón, se realizará un proceso de integración de diferentes fuentes. los registros de atletas y resultados podrán provenir de Olympedia y bases históricas derivadas de ella, mientras que los datos institucionales de participación y cuotas serán contrastados con información del Comité Olímpico Internacional. 

5. Datos públicos y confiabilidad 
Las fuentes utilizadas serán principalmente públicas. Se priorizarán: 

- Comité Olímpico Internacional (IOC): fuente institucional para cifras de participación, cuotas y políticas de igualdad. 
- Olympedia: fuente histórica especializada para resultados, atletas, deportes y eventos.  
- Bases de datos históricas derivadas de Olympedia: utilizadas como apoyo y punto de partida. 
- Fuentes académicas y periodísticas: utilizadas para contextualizar cambios históricos y contrastar hallazgos.  

La información histórica será tratada con especial precaución. El caso de París 1900 demuestra que existen diferencias en la forma de contabilizar participantes y eventos. Olympedia advierte que la edición se desarrolló en conjunto con la Exposición Universal y que no siempre existe consenso sobre qué competencias deben considerarse olímpicas.  

Por ello, se documentarán los criterios utilizados para cada cálculo y se evitará presentar como certeza una cifra cuando existan discrepancias entre fuentes.  

## Preguntas para responder con datos: 

- ¿En qué décadas/ediciones de los juegos se produjeron los mayores incrementos en la tasa de participación femenina? 
- ¿Cómo evolucionó el porcentaje de participación femenina desde 1900 a 2024? 
- ¿Qué disciplinas presentan una paridad más cercana al 50/50 en 2024? 
- ¿Qué disciplinas presentan las mayores brechas de participación entre hombres y mujeres en 2024?  
- ¿Existen disciplinas en las que hay una participación femenina mayor al 50% en 2024? 
- ¿Cuántas medallas obtuvieron las mujeres a comparación de los hombres de 1900 a 2024?  

## Historia Visual:  

Nuestro proyecto busca contar cómo ha evolucionado la participación femenina en los Juegos Olímpicos, desde las 22 mujeres que participaron en las olimpiadas en París 1900 hasta la paridad numérica alcanzada en la misma locación en 2024. Sin embargo, queremos usar este 5/50 como punto de partida para preguntarnos si la igualdad de género en el numero de atletas también se refleja dentro de las disciplinas. Para esto, queremos construir un recorrido que primero muestre el progreso de la participación femenina en las olimpiadas, para luego ir descomponiendo las cifras. Pasando así, desde una mirada general de los Juegos, hasta poder observar las diferentes brechas entre disciplinas, eventos y oportunidades de medalla.  

Elementos que ayudarán a contar la historia: 

1. Línea de tiempo: Este será el principal elemento que dará continuidad a la historia. Será una representación visual del porcentaje de mujeres en participación desde 1900 a 2024: del 2,2% al 50%. Esta línea permite la visualización de la evolución, y se podrán sacar conclusiones de por qué hay aumentos significativos ciertos años.  

2. Representación numérica: Representación visual con dos colores que representen la cantidad de participantes hombres y mujeres en 1900 y 2024 (22 de 997 participantes a 5.250 participantes de 10.500) (buscar los códigos de color).  

3. ¿50/50 en todas las disciplinas?: Una vez presentada la actual paridad, buscaremos mostrar gráficos de barras de cada disciplina del 2024, demostrando el porcentaje real de participación femenina y masculina en cada uno, y así verificar si el 50/50 general puede o no esconder diferencias significativas dentro de los Juegos. Estos datos también se complementarán con visualizaciones que detallen la distribución de eventos femeninos, masculinos y mixtos y, cuando sea posible, las oportunidades de medalla. 

## Resultados:  

¿Qué es lo mínimo que se puede contar?: 

Lo mínimo que puede contarse con los datos escogidos es la evolución de la participación femenina en los Juegos Olímpicos desde 1900 hasta 2024, destacando el aumento desde el 2,2% hasta el alcance del 50/50. Además, se podrá comparar la distribución de mujeres y hombres en las distintas disciplinas de París 2024. 

Lo máximo que se puede contar: 

Idealmente, podría llegarse a determinar si este 50/50 alcanzado en 2024 representa verdaderamente una paridad de genero en sus distintas dimensiones, considerando tanto la cantidad de atletas participantes como la distribución de disciplinas y oportunidades de medalla. Con esto, podríamos igualmente identificar si aún existen brechas persistentes, y nos permitirá demostrar si la igualdad en los números puede traducirse realmente en igualdad dentro de los Juegos. 
