Criminal Pandas 🔪🩸

👻 ¿Qué es CreepIQ?
CreepIQ es un proyecto de análisis de datos que se adentra en las entrañas del cine de terror. Nuestro objetivo: identificar los elementos clave para crear la película de miedo definitiva. Para lograrlo, hemos analizado más de medio siglo de cine aterrador, combinando fuentes de datos, técnicas de transformación y visualización avanzada.

🗂️ Dataset
Hemos trabajado con la unión de dos conjuntos de datos descargados de Kaggle:

horror_movies.csv
IMDB_Horror_movies.csv
Los datos han sido tratados de forma conjunta para generar un único dataset unificado, limpio y enriquecido.

🧹 Procesamiento de datos
Todo el tratamiento de datos se ha realizado con Python, utilizando:

Limpieza y unificación con pandas
Normalización y transformación de campos
Exportación final a .csv y .xlsx
Posteriormente, el dataset fue cargado en Power BI Desktop para su análisis visual:

Transformación y creación de columnas calculadas en Power Query
Medidas personalizadas y KPIs usando DAX
Visualizaciones interactivas organizadas por secciones
📊 Visualizaciones
La presentación del proyecto se divide en varios dashboards temáticos, todos dentro de Power BI Desktop (versión gratuita):

Dashboard	Descripción
🎬 CreepIQ	Portada del proyecto y presentación del equipo
🗺️ Cartografía del Miedo	Subgéneros de terror por país de éxito
💰 Sangre y Dinero	Análisis de la rentabilidad por subgénero
😱 Sangre y Miedo	Evolución de la popularidad de los subgéneros
🎬 Autoras del Miedo	Directores/as más influyentes del cine de terror
🎓 Graduación del Terror	Subgéneros, duración e ingresos por clasificación de edad
👥 Criaturas del Cine	Actores y actrices más presentes y rentables
🌍 Terror sin Fronteras	Contraste entre países de rodaje y estreno
🧪 Autopsia del Éxito	Fórmula ganadora para una peli perfecta
⚰️ Muerte	Cierre del proyecto
📁 Estructura del repositorio
CreepIQ/
├── data/
│   ├── horror_movies.csv
│   ├── IMDB_Horror_movies.csv
│   ├── Peliculas_terror_csv.csv
│   └── Peliculas_terror_excel.xlsx
├── notebooks/
│   ├── PARTE1-union-python.ipynb
│   └── PARTE2-limpieza-modificacion.ipynb
├── powerbi/
│   └── CreepIQ.pbix
├── README.md
👩‍💻 Proyecto académico
Este proyecto forma parte del Módulo 4 del Bootcamp de Analítica de Datos de Adalab, y ha sido desarrollado por:

🎃 Aida Bau
🕯️ Arantxa Herrero
🕷️ Gemma Traguany
☠️ Silvia Farled
🧟‍♀️ ¡Danos sustos, no bugs!
¿Tienes sugerencias o ideas macabras? Estaremos encantadas de escuchar tus gritos... digo, feedback.
Abre una issue o mándanos un pull request.

💀 Licencia
Este proyecto es de uso educativo. Consulta la licencia del dataset original en Kaggle para usos comerciales.
