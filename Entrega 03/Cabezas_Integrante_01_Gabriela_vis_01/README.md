# Documentación individual

## 1. Explicación del proceso de visualización:
Para esta visualización, mi objetivo en específico fue demostrar la contención y posterior reducción de las pruebas masculinas. Tomando en cuenta las correcciones anteriores y luego de revisar que la base de datos ahora sí estuviera completa y sin errores, busqué entre la librería de Altair un grafico que permitiera observar claramente cómo, desde el año 2000 en adelante, la cantidad de eventos o pruebas exclusivamente masculinas se estancó para dar paso a más pruebas femeninas.

Finalmente, y con la ayuda de Gemini para hacer pruebas con las diferentes opciones, concluí que un gráfico de áreas apiladas en valores absolutos era la mejor opción, ya que, al definir los ejes X e Y como “Año de los Juegos Olímpicos” y ”Número Absoluto de Pruebas (Medallas)” respectivamente, puede observarse de forma clara cómo en los últimos años la línea que grafica la cantidad de eventos masculinos se estanca, mientras que la de eventos femeninos continúa en aumento sostenido (hasta París 2024, donde ambas disminuyeron).

Además asigné colores específicos para diferenciar las diferentes áreas:

• Azul para las pruebas exclusivas de Hombres.

• Rojo para las pruebas exclusivas de Mujeres.

• Verde para las pruebas Mixtas.

• Naranja para las pruebas Abiertas.

El resultado obtenido en la visualización termina por confirmar parte de nuestra hipótesis grupal: la paridad no se logró únicamente con una expansión de los eventos femeninos, sino que en conjunto con una contención del dominio de los programas exclusivamente masculinos.

## 2. Base de datos (CSV) utilizada
(El archivo ‘olympedia_database_ocupada” fue subido directamente en la entrega)

La base de datos corresponde a la tabla corregida tras las correcciones de la Entrega 02. Antes de entregar, debimos cambiar algunos de los indicadores de la tabla anterior, además de agregar los datos faltantes. Pudimos identificar errores en algunos valores que rellenamos con ayuda de inteligencia artificial, que se basaba en las cifras entregadas por la página de Olympedia. Además, agregamos las columnas de “N° Pruebas Hombres”, “N° Pruebas Mujeres”, “N° Pruebas Mixtas” y “N° Pruebas Abiertas” por cada disciplina. Y, finalmente, descartamos las columnas de “Categoría”, que entregaban los mismos datos que las columnas agregadas, y “Medalla”, ya que desde un inicio teníamos claro que sólo tomaríamos en cuenta las pruebas y disciplinas que contemplaran la entrega de medallas.

Esta base permite medir y visualizar la oferta real de competencias. Si bien, dentro de mi visualización no se contempla la cantidad de disciplinas, estos datos fueron útiles para asegurar una mayor precisión del conteo final de las diferentes pruebas.

## 3. Ejemplos de preguntas que pueden responderse con mi visualización:
• ¿En qué año específico el crecimiento ininterrumpido de las pruebas masculinas alcanzó su límite máximo antes de comenzar a ser contenido y reducido?

• ¿Cómo evidencia la altura total del gráfico (el techo olímpico) que la paridad en París 2024 requirió obligatoriamente recortar el espacio de los hombres en lugar de solo sumar eventos femeninos?

• ¿Cuál es la proporción visual del "sacrificio" o recorte masculino frente a la irrupción progresiva de las pruebas mixtas en las últimas dos décadas?
