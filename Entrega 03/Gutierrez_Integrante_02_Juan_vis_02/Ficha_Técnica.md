# Ficha Técnica de la Base de Datos y Datos Calculados

**Características de los datos:**
*   **Formato de origen:** CSV.
*   **Unidad de análisis original:** Registro de participación por deporte, disciplina y edición olímpica (1900 - 2024).
*   **Nivel de agregación para la visualización:** Datos colapsados a nivel de `DEPORTE`, calculando los años mínimos de aparición por categoría de género.

## Variables incorporadas al análisis visual

| Variable | Descripción |
| :--- | :--- |
| `DEPORTE` | Deporte general oficial dentro del programa olímpico (Ej: Boxeo, Halterofilia, Atletismo, Ciclismo). |
| `Debut_Masculino` | **Variable calculada:** Corresponde al año mínimo (`min(AÑO)`) en el que la base de datos general registra un valor mayor a 0 en la columna original `N°PRUEBAS HOMBRES` para ese deporte específico. Indica la génesis masculina del deporte en los JJOO. |
| `Debut_Femenino` | **Variable calculada:** Corresponde al año mínimo (`min(AÑO)`) en el que la base de datos general registra un valor mayor a 0 en la columna original `N° PRUEBAS MUJERES` para ese deporte específico. Indica la génesis femenina del deporte. |
| `Años_de_Espera` | **Variable calculada:** Diferencia matemática resultante de restar `Debut_Masculino` a `Debut_Femenino`. Representa cuantitativamente la cantidad de años que las mujeres fueron marginadas de competir en dicho deporte tras el estreno de la categoría masculina. Es la variable principal del eje X en el gráfico. |

**Observaciones sobre la base de datos:**
Para este gráfico específico, las variables originales del archivo CSV (como *JJOO, Disciplina, N° Pruebas Mixtas y N° Atletas*) no fueron utilizadas directamente en la visualización, ya que el enfoque del script estuvo centrado estrictamente en aislar la temporalidad (AÑO) y la segregación original de las pruebas exclusivas para hombres y mujeres por deporte macro.
