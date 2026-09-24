## Fuente de datos: 
Utilicé datos extraídos directamente desde Olympedia, que es una página web parecida a Wikipedia, pero exclusivamente de los Juegos Olímpicos. Y también utilicé la página oficial del Comité Olímpico Internacional (COI).  

https://www.olympedia.org/editions/61  

https://www.olympics.com/ioc  

## Metodología de la construcción de la base: 
A partir de las correcciones realizadas, confirmamos que efectivamente era mejor una base de datos grupal. Para eso, cada integrante realizó la investigación de 10/9 ediciones de los Juegos Olímpicos. Yo extraje exclusivamente los Juegos Olímpicos de Verano desde Seúl 1988 hasta París 2024 (10 ediciones consecutivas). Para “acotar” la cantidad de información, agrupamos los microeventos por disciplina (ej. 100 metros vallas va en atletismo, así tampoco duplicamos deportistas) y las disciplinas se dividieron en deportes. Luego calculé la participación por disciplina clasificándolas en Femenino, Masculino o Femenino y Masculino / Mixto, según la presencia efectiva de deportistas registrados. 

## Alcance de los datos: 
Los datos que yo investigué son a partir de los Juegos Olímpicos de 1988 a 2024, cubriendo al 100% las disciplinas incluidas dentro de estas ediciones. Las ediciones oficiales son a partir de 1896, pero en este trabajo comenzaremos de 1900, viendo el avance en paridad desde los Juegos de París 1900 a París 2024. 

## Característica de los datos: 
Base de datos tabular agregada a nivel de disciplina por edición olímpica. Combina variables cualitativas categóricas (nombres, categorías, estado de medalla) y cuantitativas discretas (conteo exacto de deportistas por género). 

## Otras observaciones sobre la base:  
- Para los deportes ecuestres (Salto, Adiestramiento, Concurso Completo) las cuotas se registran operacionalmente como abiertas/mixtas, asignándose equitativamente entre ambos géneros en los conteos oficiales.  
- La separación entre deportes y disciplinas responde al estándar oficial del COI (ej. El deporte Deportes Acuáticos engloba disciplinas como Natación, Waterpolo, Natación Artística, etc.). 
- No todos los años se realizan las mismas disciplinas, aunque estas ya se hayan realizado años anteriores.  

## Diccionario de datos:  
- JJOO: Hace referencia a Juegos Olímpicos, y el nombre de la ciudad sede de esa edición. Es un dato categórico de texto, sus posibles variables son: París, Tokio, Río de Janeiro, Londres, Pekín, Atenas, Sídney, Atlanta, Barcelona, Seúl. Este dato fue utilizado para agrupar y visualizar de manera cronológica las sedes.  
- AÑO: Año de realización de la edición de esos Juegos Olímpicos. Este es un dato numérico entero, y sus posibles variables van desde 2024 a 1988, con intervalos de 4 años entre ellos. Esta variable sirve para comprender de manera cronológica en el tiempo cuántos años se llevó para alcanzar la paridad y analizar tendencias.  
- DEPORTE: Es una macrocategoría para dividir ciertas disciplinas que utiliza el COI. Es un dato categórico de texto, y sus posibles variables son hartas: Atletismo, Deportes Acuáticos, Ciclismo, Gimnasia, Baloncesto, Lucha, etc. Este dato permite agrupar disciplinas afines bajo un mismo paraguas federativo. 
- DISCIPLINA: Hace referencia a una modalidad específica dentro de un deporte oficial. Es un dato categórico de texto, y sus posibles variables son hartas: Natación, Waterpolo, BMX Racing, Ciclismo en Ruta, Gimnasia Artística, etc. Es una unidad principal de análisis de la base de datos. 
- CATEGORÍA: Hace referencia a la composición de género permitida o registrada en la disciplina. Es un dato categórico de texto, y sus posibles variables son: Femenino, Masculino, Femenino y Masculino, y Mixto. Este dato es crucial para verificar el avance en el cierre de la brecha de género. 
- N° MUJERES: Cantidad total de atletas mujeres participantes en la disciplina. Es un dato numérico entero, y sus posibles variables van del 0 a 1806. Un valor igual a 0 indica exclusividad masculina en esa edición. 
- N° HOMBRES: Cantidad total de atletas hombres participantes en la disciplina. Es un dato numérico entero, y sus posibles variables van del 0 a 1268. Un valor igual a 0 indica exclusividad femenina en esa edición.  
- MEDALLA: Indicador de si la disciplina otorgó medallas oficiales. Es categórico, y sus variables son SI o NO. En esta base, todas las disciplinas incluidas corresponden a eventos oficiales con medalla (Sí). 