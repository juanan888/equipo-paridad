# Ficha Técnica y Diccionario de Datos

## 1. Ficha Técnica

*   **Fuente de los datos:** Archivos de Olympedia y registros públicos oficiales del Comité Olímpico Internacional (COI).
*   **Metodología de construcción:** Buscamos y agrupamos los datos edición por edición. Luego limpié y ordené la información usando Python (librería Pandas) en Google Colab para arreglar los textos, sacar los porcentajes matemáticos y armar categorías por décadas.
*   **Alcance de los datos:** Mi archivo cubre exclusivamente 10 ediciones de los Juegos Olímpicos de Verano, desde Londres 1948 hasta Los Ángeles 1984.
*   **Característica de los datos:** Es una tabla ordenada por deporte y disciplina, donde lo más importante es el conteo demográfico de cuántos hombres y mujeres compitieron por cada evento.
*   **Otras observaciones:** Este bloque de años es vital para la historia de nuestro grupo porque es la etapa más estancada. Muestra perfecto el letargo institucional del COI antes de que empezara el proceso de modernización real en los años 90.

## 2. Diccionario de Datos

| Variable | Descripción | Tipo de Dato | Valores Posibles |
| :--- | :--- | :--- | :--- |
| `jjoo` | La ciudad sede de los Juegos Olímpicos. | String | *Londres, Helsinki, Múnich, Los Ángeles, etc.* |
| `anio` | Año exacto del evento. | Integer | *1948, 1952, 1956 ... 1984* |
| `decada` | Columna calculada para agrupar los años por décadas. | Integer | *1940, 1950, 1960, 1970, 1980* |
| `deporte` | Deporte principal o macro-categoría. | String | *Atletismo, Natación, Gimnasia, etc.* |
| `disciplina` | La prueba específica dentro del deporte. | String | *100m, Relevos, Salto largo, etc.* |
| `categoria` | Si el evento era para hombres, mujeres o mixto. | String | *Femenino, Masculino, Femenino y Masculino* |
| `mujeres` | Cantidad exacta de mujeres inscritas. | Integer | *0 - 1500* |
| `hombres` | Cantidad exacta de hombres inscritos. | Integer | *0 - 1500* |
| `total_atletas`| Suma total de mujeres y hombres en la prueba. | Integer | *0 - 3000* |
| `pct_mujeres` | El porcentaje de participación femenina. | Float | *0.0 - 100.0* |
| `estado_paridad`| Etiqueta para agrupar qué tan grande era la brecha. | String | *Brecha alta, Cerca de la paridad, Paridad exacta* |
| `medalla` | Indica si la competencia entregaba medalla oficial o no. | String | *Sí / No* |
