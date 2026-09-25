# Historial de procesos y decisiones - Juan Antonio Gutiérrez

## 1. Explicación del proceso de limpieza de datos

Para esta segunda entrega, como grupo nos dimos cuenta de que trabajar con bases de datos separadas (como hicimos en la Entrega 01) era un enredo y no nos iba a servir para contar una buena historia. Por eso, decidimos armar un solo archivo gigante con todas las ediciones de los Juegos Olímpicos. Como era mucha información, nos dividimos la base por bloques de años. A mí me tocó limpiar y analizar el tramo intermedio, que va desde **Londres 1948 hasta Los Ángeles 1984**. 

Este periodo es clave para nuestra investigación periodística porque abarca toda la época de la posguerra y la Guerra Fría. Es justo el momento donde se nota más el letargo del COI: las mujeres empezaron a entrar a los Juegos, pero a un ritmo lentísimo y con muchas trabas para acceder a deportes de equipo o de combate.

Para limpiar los datos usé Python con la librería Pandas en Google Colaboratory. Como no soy experto programando, traté de mantener el código lo más simple y ordenado posible. Estos fueron los pasos detallados que seguí:

**Paso 1: El problema al cargar el archivo (Codificación)**
Lo primero que me pasó fue que Python no quería leer el Excel original que guardamos como CSV. Me tiraba un error enorme en rojo. Investigando me di cuenta de que era porque el archivo tenía tildes y eñes (como en la palabra "AÑO" o "CATEGORÍA"). Tuve que agregarle al código el parámetro `encoding='latin-1'` para forzar la lectura sin que se borraran las palabras en español.

**Paso 2: Arreglar los nombres de las columnas**
El archivo original venía con las columnas en mayúsculas, con tildes y hasta con espacios en blanco al final (la columna de hombres decía `N° HOMBRES ` con un espacio extra). Trabajar así en Python es súper incómodo porque te tira error a cada rato. Así que armé un diccionario para renombrar todo a minúsculas y sin espacios. Las dejé así: `jjoo`, `anio`, `deporte`, `disciplina`, `categoria`, `mujeres`, `hombres` y `medalla`.

**Paso 3: Filtrar mis años y crear nuevas columnas**
Después de limpiar los títulos, filtré la base para quedarme solo con las 10 ediciones que me tocaron (1948 a 1984). Pero revisando nuestra hipótesis (que habla de un letargo de décadas), me di cuenta de que ver la evolución año a año no era tan claro para la historia. Así que creé una columna nueva llamada `decada`. Lo hice con una división matemática simple en el código para agrupar todo en los 40s, 50s, 60s, 70s y 80s.
También armé una columna sumando hombres y mujeres (`total_atletas`) y otra para sacar el porcentaje de mujeres en cada prueba (`pct_mujeres`). Esto es fundamental porque en periodismo de datos los números absolutos engañan, necesitamos las proporciones reales.

**Paso 4: Etiquetar la paridad para la webstory**
Para que mi parte calcara perfecto con la de mi compañera en su bloque de años, armé una función para clasificar cada fila. Si el porcentaje de mujeres estaba entre 40% y 60%, le puse "Cerca de la paridad". Si era 50% clavado o había una diferencia de 1 o 2 personas nomás, le puse "Paridad exacta". Todo lo demás quedó como "Brecha alta". Al correr el código, me di cuenta de que en mis años casi todo es brecha alta, lo que confirma lo que queríamos demostrar como grupo.

**Paso 5: Revisión y guardado final**
Antes de terminar, le pedí a Python que me mostrara si quedaban celdas vacías (`df.isnull().sum()`) para estar seguro de que no faltaban datos en ninguna fila. Finalmente, exporté mi pedazo de la base de datos limpia como `database_limpia_1948_1984.csv`, pero esta vez me aseguré de guardarlo en formato `utf-8` universal para que cuando juntemos todo el trabajo del grupo en GitHub no tengamos el mismo problema de lectura que tuve yo al principio.

---

## 2. Fuentes de datos utilizadas

La información la sacamos buscando a mano y cruzando datos de sitios públicos, siguiendo la lógica de OSINT:
*   **Olympedia / Sports-Reference:** Fue nuestra fuente principal. Es una base de datos gigante armada por historiadores olímpicos. Me sirvió un montón para rastrear exactamente en qué año de la Guerra Fría entraron las mujeres a competencias específicas (como el vóleibol en Tokio 1964) y cuántos cupos les dieron.
*   **Documentos del COI:** Usamos los registros oficiales del Comité Olímpico para confirmar cuántos cupos reales se abrían para mujeres y si las pruebas entregaban medallas de verdad o eran solo exhibiciones para calmar las críticas.

---

## 3. Ejemplos de preguntas que puedo responder ahora

Con la base de datos ya limpia y ordenada en un CSV, la puedo meter a Excel o hacer una tabla dinámica para sacar datos duros para el reportaje:

1.  **¿En qué década exacta (50s, 60s o 70s) el COI empezó a aflojar y aparecieron las primeras pruebas etiquetadas como "Cerca de la paridad"?** 
    *(Esto me sirve para ver si hubo algún hito histórico, como los Juegos de Múnich 72 o Montreal 76, que los obligó a abrirse más).*
2.  **¿Qué deportes clásicos mantuvieron la columna de `mujeres` en 0 absoluto durante las 10 ediciones que van desde Londres 1948 hasta Los Ángeles 1984?**
    *(Con esto podemos apuntar con nombre y apellido a las disciplinas más atrasadas institucionalmente, como los deportes de combate o la halterofilia).*
3.  **A medida que pasaban las décadas, ¿el aumento en el `total_atletas` femenino significaba que el COI le quitaba cupos a los hombres o simplemente la organización agrandaba los Juegos Olímpicos en general?**
    *(Esto nos sirve para analizar la verdadera gestión administrativa de la igualdad en esa época).*
