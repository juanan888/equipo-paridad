# Documentación del Proyecto: EN PRUEBA

## 1. Manual de Identidad Visual

### Proceso de creación y moodboard
El concepto gráfico de **EN PRUEBA** nace para visibilizar 124 años de desigualdad en la oferta de pruebas olímpicas por género (1900-2024). El moodboard combina la memoria histórica del archivo olímpico mediante fotografía en duotono y textura de grano con el lenguaje técnico del dato (marcadores, pistas de atletismo, marcas de conteo y cuadrículas). La propuesta busca transmitir la tensión de un titular deportivo con el rigor de un análisis cuantitativo.

### Justificación de secciones

* **Color:**
  * **Azul Tinta (`#14213D` - 40%):** Utilizado para fondos, textos principales y estructura, aportando contraste y sobriedad editorial.
  * **Papel Hueso (`#F4EFE6` - 30%):** Utilizado como fondo de lectura y zonas de aire para evitar la fatiga visual.
  * **Fucsia (`#D63360` - 12%):** Asignado de forma exclusiva a la identificación de pruebas femeninas.
  * **Petróleo (`#1F7A8C` - 10%):** Asignado exclusivamente a la identificación de pruebas masculinas.
  * **Ámbar (`#F2B132` - 8%):** Destinado a elementos interactivos, botones de acción (CTA) y pruebas mixtas o abiertas.

* **Tipografía:**
  * **Anton (Títulos y cifras):** Fuente condensada en mayúsculas que imita la estética de los marcadores deportivos y titulares de prensa para lograr impacto visual inmediato (H1 a 96px, Cifras a 160px).
  * **DM Sans (Texto corrido):** Tipografía sans-serif limpia con interlineado de 1.45 y cuerpo de 14-16pt, orientada a la legibilidad fluida de la crónica periodística.
  * **Space Mono (Datos y etiquetas):** Fuente monoespaciada para años, etiquetas y fuentes metodológicas, reforzando la precisión del lenguaje de datos.

* **Recursos gráficos e iconografía:**
  * **Iconografía:** Trazos gruesos (4px) con esquinas rectas sin relleno en Azul Tinta o Papel Hueso[cite: 9]. Los colores de género solo se activan al aplicar filtros.
  * **Componentes UI:** Botones rectangulares con bordes sutiles de 6px. El color Ámbar se reserva para la acción activa/primaria y los filtros heredan el color del tipo de prueba seleccionado (Fucsia, Petróleo o Ámbar).
  * **Fotografía e Ilustración:** Fotografías de archivo en duotono (Fucsia/Petróleo) centradas en la acción y el entrenamiento (nunca poses estereotipadas), junto con ilustraciones geométricas planas.
  * **Patrones:** Líneas de carril, marcas de conteo de cinco y cuadrículas donde cada bloque equivale exactamente a 1 prueba olímpica.

---

## 2. Wireframes y Prototipo

### Link al prototipo
* **Prototipo interactivo en Miro:** https://miro.com/app/board/uXjVERJfAUk=/?share_link_id=568882807061

### Justificación de la estructura y propuesta de flujo
La estructura narrativa se organiza en un recorrido de scroll vertical continuo articulado en tres niveles:

1. **Pantalla de entrada / Portada:** Presenta la cifra protagonista (ej. 152/157 pruebas masculinas/femeninas en París 2024) en Anton junto a la tesis de la investigación para generar impacto inmediato.
2. **Desarrollo narrativo y módulos de datos:** Integración de las crónicas con visualizaciones embebidas donde cada cuadrado equivale a una prueba concreta.
3. **Filtros interactivos y navegación:** Permite al usuario filtrar por tipo de prueba (Femeninas, Masculinas, Mixtas) mediante botones codificados por color, garantizando un flujo claro y sin distracciones.

---

## 3. Actualización de la Hipótesis y Propuesta de Trabajo Grupal

### Actualización de la hipótesis
* **Hipótesis inicial:** La paridad alcanzada en París 2024 significaba el fin definitivo de la brecha de género en los Juegos Olímpicos.
* **Hipótesis actualizada:** La paridad de participantes en París 2024 oculta un ajuste tardío en el programa femenino y una contención del programa masculino tras 124 años de desigualdad acumulada. La paridad numérica actual de atletas no resuelve las disparidades históricas ni la brecha persistente en disciplinas específicas como los deportes de combate y resistencia.

### Propuesta de trabajo grupal
El grupo organizó el trabajo articulando la investigación a partir del registro histórico de Olympedia (1900-2024). Cada integrante desarrolló su propia crónica e integración en HTML/Pages a partir de su tramo asignado del dataset, mientras que las fichas de persona, el mapa de viaje del usuario, los wireframes y el manual de identidad visual se trabajaron de forma colaborativa para garantizar coherencia temática y gráfica en toda la webstory.
