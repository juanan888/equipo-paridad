# Historial de procesos y decisiones - Juan Antonio Gutiérrez

## 1. Explicación del proceso de limpieza de datos

Para esta segunda entrega del proyecto, como grupo nos dimos cuenta de que trabajar con bases de datos separadas (como hicimos en la Entrega 01) era un enredo y no nos iba a servir para contar una historia coherente y con buenos ángulos periodísticos. Tras darle un par de vueltas y ver los comentarios que recibimos, decidimos armar un solo archivo consolidado con todas las ediciones de los Juegos Olímpicos de Verano. Como son demasiados datos y ediciones, nos dividimos la base por bloques de años. A mí me tocó hacerme cargo de limpiar y analizar el tramo intermedio, que va desde **Londres 1948 hasta Los Ángeles 1984**.

Desde el punto de vista periodístico, este periodo de 36 años es clave para nuestra investigación. Abarca toda la época de la posguerra y las mayores tensiones de la Guerra Fría (incluyendo los famosos boicots de Moscú 1980 y Los Ángeles 1984). Es justo el momento histórico donde se nota más el letargo del Comité Olímpico Internacional (COI): las mujeres empezaron a entrar a los Juegos y a ganar algo de terreno, pero a un ritmo lentísimo y con muchas trabas institucionales para acceder a deportes de equipo o disciplinas de combate[cite: 5].

Para hacer el trabajo de limpieza de los datos usé Python con la librería Pandas en Google Colaboratory. Como estoy recién aprendiendo a usar estas herramientas de programación, traté de mantener el código lo más simple, lógico y ordenado posible. Estos fueron los pasos detallados que seguí para lograr el CSV final:

**Paso 1: El problema al cargar el archivo original (Codificación)**
Lo primero que me pasó fue que Python no quería leer el Excel original que guardamos como CSV. Me tiraba un error gigante de código. Investigando, me di cuenta de que el problema era que el archivo tenía caracteres en español (tildes en palabras como "CATEGORÍA" y la "Ñ" en la palabra "AÑO"). Tuve que agregarle al código el parámetro para forzar la lectura sin que se rompiera el programa ni se borraran las palabras.

**Paso 2: Estandarizar los nombres de las columnas**
El archivo original que armamos venía con las columnas en mayúsculas, con tildes y, lo peor de todo, con espacios en blanco al final (por ejemplo, la columna de hombres decía `N° HOMBRES ` con un espacio extra casi invisible). Trabajar así en Python es súper incómodo porque te tira error de sintaxis a cada rato. Para arreglarlo, armé un diccionario en el código para renombrar todo a minúsculas y sin espacios raros. Las columnas quedaron limpias así: `jjoo`, `anio`, `deporte`, `disciplina`, `categoria`, `mujeres`, `hombres` y `medalla`.

**Paso 3: Filtrar mis años y crear nuevas columnas**
Después de limpiar los títulos, filtré la base de datos completa para quedarme exclusivamente con las 10 ediciones que me tocaron (desde 1948 a 1984). Pero revisando nuestra hipótesis grupal —que habla de una brecha de décadas[cite: 5]—, me di cuenta de que ver la evolución año a año (cada 4 años en realidad) no era tan claro para mostrar un estancamiento. Así que decidí crear una columna nueva llamada `decada`. Lo hice con una división matemática simple en el código para agrupar todas las filas en los 40s, 50s, 60s, 70s y 80s.
Además, armé una columna sumando la cantidad de hombres y mujeres (`total_atletas`) y otra para sacar el porcentaje exacto de mujeres en cada prueba (`pct_mujeres`). Esto es súper importante para no hablar solo de números enteros, sino de proporciones reales.

**Paso 4: Etiquetar la paridad para la webstory**
Para que mi parte calcara perfecto con el trabajo que hizo mi compañera en su tramo de años más recientes, armé una función en Python para clasificar cada fila. Si el porcentaje de mujeres de una disciplina estaba entre el 40% y el 60%, le puse la etiqueta "Cerca de la paridad". Si era el 50% clavado o había una diferencia ínfima de 1 o 2 personas, le puse "Paridad exacta". Todo lo demás (que estuviera por debajo del 40% de mujeres o derechamente en 0%) quedó como "Brecha alta". Al correr el código, pude comprobar que en mis años casi todas las pruebas caen en "Brecha alta", lo que confirma totalmente la hipótesis de nuestro reportaje.

**Paso 5: Revisión y exportación final**
Antes de dar por terminado el trabajo, le pedí a Python que me mostrara si quedaban celdas vacías o nulas usando el comando `.isnull().sum()`. Quería estar seguro de que no faltaban datos importantes. Como todo estaba en orden, exporté mi pedazo de la base de datos como `database_limpia_1948_1984.csv`. Esta vez me aseguré de guardarlo en formato `utf-8` universal, para que cuando juntemos el trabajo de los tres integrantes en GitHub no tengamos el mismo problema de lectura que tuve al principio.

---

## 2. Fuentes de datos utilizadas

Toda nuestra información la sacamos buscando de forma manual y cruzando datos de sitios públicos, siguiendo la lógica de Inteligencia de Fuentes Abiertas (OSINT):
*   **Olympedia / Sports-Reference:** Fue nuestra salvación y la fuente más importante. Es una base de datos histórica gigante avalada por historiadores olímpicos. Me sirvió un montón para rastrear exactamente en qué año de la Guerra Fría entraron las mujeres a competencias específicas (como la gimnasia rítmica o el remo) y cuántos cupos les dieron.
*   **Documentos oficiales del COI:** Usamos los registros del Comité Olímpico Internacional para confirmar cuántos cupos reales se abrían para mujeres y si las pruebas entregaban medallas oficiales o eran solamente exhibiciones para calmar las críticas sociales de la época.

---

## 3. Ejemplos de preguntas que se pueden responder con la base limpia

Con esta base de datos ya limpia y estructurada en formato CSV, puedo armar tablas dinámicas para sacar datos duros que sustenten nuestro reportaje. Algunas preguntas que ahora puedo responder son:

1.  **¿En qué década exacta de este tramo histórico (50s, 60s o 70s) el COI empezó a ceder y aparecieron las primeras pruebas femeninas etiquetadas como "Cerca de la paridad"?** 
    *(Esto nos sirve para ver si hubo algún evento político o social en el mundo que los obligó a cambiar las reglas del juego).*
2.  **¿Qué deportes clásicos mantuvieron la columna de `mujeres` en 0 durante las 10 ediciones completas que van desde Londres 1948 hasta Los Ángeles 1984?**
    *(Con este dato podemos nombrar con nombre y apellido a las disciplinas más atrasadas y machistas de la época, como los deportes de combate o la halterofilia, que tuvieron que esperar muchísimos años más para abrirse).*
3.  **A medida que pasaban los Juegos, ¿el aumento en el `total_atletas` femenino significaba que el COI achicaba los cupos de los hombres para hacer espacio, o simplemente agrandaban el tamaño total de los Juegos Olímpicos?**
    *(Esta pregunta es súper interesante porque nos sirve para ver cómo la institución administraba los espacios y el presupuesto cuando por fin dejaban entrar a más mujeres a competir).*
