# Documentación Individual - Entrega 03

## Explicación del proceso de visualización y decisiones tomadas
Para esta visualización individual, el objetivo fue demostrar una dimensión particular de nuestra hipótesis de investigación: que la igualdad lograda en París 2024 esconde disparidades históricas muy grandes. Para no repetir los gráficos de líneas sobre la evolución total de pruebas que ya hizo mi grupo, decidí enfocarme en mostrar el "tiempo de espera" o "retraso institucional" que sufrieron las mujeres por cada deporte. 

Como no tengo conocimientos avanzados de programación en Python, **me apoyé en el uso de Inteligencia Artificial (Gemini)** para que me ayudara a estructurar y redactar el código necesario en Google Colab. Los pasos y decisiones fueron los siguientes:

1. **Idea y carga de datos:** Subí nuestro archivo CSV a Google Colab. Tenía claro que quería restar el año de la primera prueba femenina con la primera prueba masculina para sacar la brecha.
2. **Procesamiento de datos con IA:** Le pedí a la IA que me generara un script en `pandas` que lograra identificar automáticamente cuál fue el primer año (el mínimo) en que se registró una prueba de hombres para cada deporte, y que hiciera lo mismo para las mujeres. 
3. **Cálculo de la Brecha:** Con el código generado por la IA, se unieron esos dos datos y se creó una nueva columna llamada `Años_de_Espera`, que simplemente restaba el año debut de los hombres al de las mujeres. 
4. **Filtrado:** El código ordenó los resultados de mayor a menor y seleccionó el "Top 15" de deportes con la mayor cantidad de años de espera.
5. **Visualización:** Para graficarlo, le pedí a la IA que utilizara la librería `Altair` para crear un **Gráfico de Barras Horizontales**. Tomé esta decisión de diseño porque la longitud de la barra acostada representa de forma muy intuitiva la idea de una "línea de tiempo" o "duración de la espera".

## Base de datos (CSV) utilizada y procesamiento
Utilicé la base de datos oficial en la que hemos estado trabajando como equipo, basada en los registros de **Olympedia.org** (archivo: `BASE DE DATOS(Hoja1).csv`). 
*   **Por qué se seleccionó:** A diferencia de las bases que solo cuentan el número general de atletas, nuestra base tiene separadas las columnas de `N°PRUEBAS HOMBRES` y `N° PRUEBAS MUJERES`. Esta separación era fundamental para poder indicarle a la IA qué columnas debía mirar para encontrar el primer año de competencia por género.
*   **Procesamiento previo y actual:** La base ya venía limpia por el trabajo grupal (donde borramos cosas que no nos servían, como si daban medalla o no). Para este gráfico en particular, el único procesamiento extra que hizo el script de Colab fue resumir la información: colapsó todos los datos dejando solo los nombres de los deportes y calculando los años de espera entre el debut masculino y femenino.

## Ejemplos de preguntas que responde la visualización
* ¿Cuántos años transcurrieron en cada disciplina deportiva entre el debut de la primera prueba masculina y la incorporación de su prueba femenina equivalente?
* ¿Cuáles fueron los deportes que presentaron la mayor brecha temporal (castigo histórico) para permitir la participación de las mujeres?
* ¿Demuestra este análisis que la paridad 50/50 lograda en París 2024 omite los años de marginación y falta de oportunidades que sufrieron las atletas durante el siglo XX?
