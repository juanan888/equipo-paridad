# Historial de procesos y decisiones - Juan Antonio Gutiérrez

Tras los comentarios de la Entrega 01, como equipo decidimos consolidar nuestro análisis en una estructura de datos única para poder medir la evolución de la paridad de género en los Juegos Olímpicos. Para lograrlo de forma eficiente, nos dividimos las décadas. A mí me correspondió abarcar desde **Londres 1948 hasta Los Ángeles 1984** (10 ediciones).

Este periodo es fascinante periodísticamente porque representa los años de la Guerra Fría, donde el deporte fue una herramienta geopolítica y donde las mujeres comenzaron a ganar espacios en disciplinas tradicionalmente masculinas.

### Proceso de limpieza y estructuración:
1. **Recolección:** A partir de los portales históricos (Olympedia), identifiqué las sedes, años y disciplinas de mi periodo.
2. **Estructuración:** Basándome en la tabla de mi compañera, definí las mismas columnas (`JJOO`, `AÑO`, `DEPORTE`, `DISCIPLINA`, `CATEGORÍA`, `N° MUJERES`, `N° HOMBRES`, `MEDALLA`).
3. **Tabulación:** Fui ingresando los deportes más representativos (Atletismo, Natación, Gimnasia, Básquetbol, Voleibol y Halterofilia) diferenciando estrictamente si la categoría era femenina o masculina.
4. **Validación:** Me aseguré de reflejar hitos históricos, como que las mujeres no tuvieron participación en Baloncesto sino hasta Montreal 1976, o que la Halterofilia se mantuvo 100% masculina en este periodo.
5. **Consolidación:** Con la ayuda de herramientas como Gemini y Excel, estructuré la información final y la exporté en formato CSV UTF-8 para evitar problemas con los caracteres (como los tildes en "Múnich" o "Los Ángeles").

### Lista de fuentes utilizadas:
- **Olympedia:** Para contrastar la adición de nuevos deportes femeninos.
- **COI (olympics.com):** Para la nomenclatura oficial de "Deporte" vs "Disciplina".

### Preguntas que se pueden responder con mi base de datos limpia:
Armando una tabla dinámica con este CSV, podemos responder a lo siguiente:
1. ¿En qué año y disciplina específica comenzaron a integrarse las mujeres por primera vez entre 1948 y 1984?
2. ¿Cómo afectaron los boicots políticos de Moscú 1980 y Los Ángeles 1984 en la cantidad total de mujeres participantes en comparación con la edición de Montreal 1976?
3. ¿Qué deportes mantuvieron una exclusividad masculina total (cero participación femenina) durante todo el periodo analizado?
