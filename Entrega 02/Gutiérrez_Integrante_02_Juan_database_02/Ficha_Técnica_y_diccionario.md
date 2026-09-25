# Ficha Técnica y Diccionario de Datos

## 1. Ficha Técnica

*   **Fuente de los datos:** Archivos de Olympedia y registros públicos del Comité Olímpico Internacional (COI)[cite: 1].
*   **Metodología de construcción:** Buscamos los datos edición por edición y luego los limpié y ordené usando Python (Pandas) en Google Colab para arreglar textos, sacar porcentajes y armar décadas.
*   **Alcance de los datos:** Mi archivo cubre solo 10 ediciones de los Juegos Olímpicos de Verano, desde Londres 1948 hasta Los Ángeles 1984.
*   **Característica de los datos:** Es una tabla ordenada por deporte y disciplina, donde lo más importante es el conteo de cuántos hombres y mujeres compitieron.
*   **Observaciones:** Este bloque de años es vital para el grupo porque es la etapa más estancada. Muestra perfecto el letargo institucional antes de que empezara la modernización en los años 90[cite: 5].

## 2. Diccionario de Datos

| Variable | Descripción | Tipo de Dato | Valores Posibles |
| :--- | :--- | :--- | :--- |
| `jjoo` | Ciudad sede de los Juegos Olímpicos. | String | *Londres, Helsinki, Tokio, etc.* |
| `anio` | Año del evento. | Integer | *1948, 1952 ... 1984* |
| `decada` | Columna calculada para agrupar por décadas. | Integer | *1940, 1950, 1960, 1970, 1980* |
| `deporte` | Deporte principal. | String | *Atletismo, Natación, Gimnasia* |
| `disciplina` | La prueba específica. | String | *100m, Torneo Olímpico, etc.* |
| `categoria` | Género oficial de la prueba. | String | *Femenino, Masculino, Mixto* |
| `mujeres` | Cantidad total de cupos femeninos. | Integer | *0 - 1500* |
| `hombres` | Cantidad total de cupos masculinos. | Integer | *0 - 1500* |
| `total_atletas`| Suma total de hombres y mujeres. | Integer | *0 - 3000* |
| `pct_mujeres` | Porcentaje de participación femenina. | Float | *0.0 - 100.0* |
| `estado_paridad`| Etiqueta para saber qué tan grande es la brecha. | String | *Brecha alta, Cerca de la paridad, Paridad exacta* |
| `medalla` | Indica si es una prueba que da medalla oficial. | String | *Sí / No* |
