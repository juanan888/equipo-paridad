# Ficha Técnica y Diccionario de Datos

## Ficha Técnica

**Fuente de datos:**
Utilicé datos históricos basados en los registros de Olympedia y el Comité Olímpico Internacional (COI).
- https://www.olympedia.org/editions
- https://www.olympics.com/ioc

**Metodología de la construcción de la base:**
Para mantener la coherencia con el trabajo grupal, dividimos la historia de los Juegos Olímpicos. Mi investigación abarca 10 ediciones de los Juegos Olímpicos de Verano, desde Londres 1948 hasta Los Ángeles 1984. Para ordenar la información, agrupamos los microeventos por disciplina deportiva para no duplicar deportistas, categorizando la participación por género (Femenino, Masculino) en base a los registros de participación efectiva.

**Alcance de los datos:**
Los datos cubren el periodo de 1948 a 1984. Esta época es vital para nuestro análisis de paridad, ya que abarca el periodo de la Guerra Fría (incluyendo los grandes boicots de 1980 y 1984) y muestra la lenta, pero progresiva, incorporación de la mujer en el deporte (por ejemplo, la entrada del Voleibol femenino en 1964 y el Baloncesto femenino en 1976).

**Característica de los datos:**
Base de datos tabular agregada a nivel de disciplina por edición olímpica. Combina variables cualitativas categóricas (nombres de sedes, categorías, estado de medalla) y cuantitativas discretas (conteo de deportistas por género).

**Otras observaciones sobre la base:**
- El periodo analizado refleja fluctuaciones en los números totales debido a factores sociopolíticos (como el boicot a Moscú 1980 y Los Ángeles 1984).
- Hay disciplinas como la Halterofilia que, durante todo este periodo, se mantuvieron exclusivamente masculinas, lo que ayuda a contrastar la brecha de género de la época.

---

## Diccionario de Datos

| Variable | Descripción | Tipo de dato |
| :--- | :--- | :--- |
| **JJOO** | Juegos Olímpicos y nombre de la ciudad sede. Posibles valores: Londres, Helsinki, Melbourne, Roma, Tokio, Ciudad de México, Múnich, Montreal, Moscú, Los Ángeles. | Categórico (Texto) |
| **AÑO** | Año de realización de la edición. Intervalos de 4 años. | Numérico (Entero), de 1948 a 1984 |
| **DEPORTE** | Macrocategoría del COI (Ej: Atletismo, Deportes Acuáticos, Gimnasia). Permite agrupar disciplinas. | Categórico (Texto) |
| **DISCIPLINA** | Modalidad específica dentro del deporte (Ej: Natación, Gimnasia Artística). Unidad principal de análisis. | Categórico (Texto) |
| **CATEGORÍA** | Composición de género permitida (Femenino, Masculino). Crucial para medir la brecha. | Categórico (Texto) |
| **N° MUJERES** | Cantidad total de atletas mujeres participantes. Un valor de 0 indica exclusividad masculina. | Numérico (Entero) |
| **N° HOMBRES** | Cantidad total de atletas hombres participantes. Un valor de 0 indica exclusividad femenina. | Numérico (Entero) |
| **MEDALLA** | Indicador de si la disciplina otorgó medallas oficiales. En esta base todas corresponden a eventos oficiales (SI). | Categórico (Texto) |
