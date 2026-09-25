### Fuente de datos:
Al igual que en el resto del proyecto grupal, utilicé datos extraídos directamente desde Olympedia y contrastados con la página oficial del Comité Olímpico Internacional (COI).
https://www.olympedia.org/editions
https://www.olympics.com/ioc

### Metodología de la construcción de la base:
A partir de las correcciones de la Entrega 01, consolidamos la investigación en una base de datos grupal dividida por épocas. Mi rol fue extraer y sistematizar la participación en los Juegos Olímpicos de Verano correspondientes a los primeros años: desde París 1900 hasta Berlín 1936 (9 ediciones de verano, recordando que la edición de 1916 se suspendió por la Primera Guerra Mundial). Agrupamos los microeventos por disciplina y calculé la participación por categoría (Femenino, Masculino) según la presencia efectiva de los pioneros deportivos registrados en esos años.

### Alcance de los datos:
Los datos que investigué cubren desde París 1900 hasta Berlín 1936. Si bien los Juegos comenzaron en 1896 (Atenas), las mujeres hicieron su debut olímpico oficial recién en París 1900. Por lo tanto, nuestro análisis de paridad arranca formalmente en esa fecha. Esta base evidencia los años más críticos de la brecha de género, donde disciplinas enteras estaban prohibidas para las mujeres.

### Características de los datos:
Base de datos tabular agregada a nivel de disciplina por edición olímpica. Combina variables cualitativas categóricas (nombres, categorías, estado de medalla) y cuantitativas discretas (conteo exacto de deportistas por género).

### Otras observaciones sobre la base:
Para los primeros Juegos (1900 y 1904) la separación formal de delegaciones nacionales e inscripciones era muy precaria, por lo que el conteo de mujeres participantes suele variar ligeramente entre registros históricos. Se priorizó el conteo oficial de Olympedia.
Se puede observar la inclusión paulatina de deportes femeninos, como la natación en 1912 y el atletismo recién en 1928.

### Diccionario de datos:

#### JJOO 
Nombre de la ciudad sede de esa edición.

Tipo de dato: Categórico de texto (París, San Luis, Londres, Estocolmo, Amberes, Ámsterdam, Los Ángeles, Berlín).

#### AÑO	
Año de realización de la edición olímpica.	

Tipo de dato: Numérico entero (1900 a 1936). Excluye 1916 por suspensión.

#### DEPORTE	
Macrocategoría oficial del COI para agrupar disciplinas.	

Tipo de dato: Categórico de texto (Atletismo, Deportes Acuáticos, Tenis, etc.).

#### DISCIPLINA	
Modalidad específica dentro del deporte oficial.	

Tipo de dato: Categórico de texto (100m, Individuales, Natación 100m libres, etc.).

#### CATEGORÍA	
Composición de género permitida o registrada.

Tipo de dato: Categórico de texto (Femenino, Masculino). En esta época no había registros oficiales mixtos formales como hoy.

#### N° MUJERES	
Cantidad total de atletas mujeres participantes.	

Tipo de dato: Numérico entero (ej: 0 a 64). El valor 0 indica exclusión femenina en esa disciplina.

#### N° HOMBRES	
Cantidad total de atletas hombres participantes.	

Tipo de dato: Numérico entero (ej: 0 a 111).

#### MEDALLA	
Indicador de si la disciplina otorgó medallas oficiales.	

Tipo de dato: Categórico (SI/NO). En esta base, todas corresponden a eventos oficiales (SI).
