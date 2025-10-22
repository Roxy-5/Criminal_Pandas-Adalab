![](https://github.com/Roxy-5/Evaluacion1-Adalab/blob/main/image.jpg?raw=true)
### 🔍 Criminal Pandas 🔪🩸

### 🎬 Storytelling
Somos Criminal Pandas 🐼: un escuadrón de analistas nocturnos que merodean entre tablas y gráficos. Bajo la luz tenue del PC olfateamos anomalías, atrapamos outliers como si fuera bambú y convertimos datos sospechosos en pruebas irrefutables.

Dicen que, cuando cae la noche, los trimestres susurran secretos y nosotros los escuchamos para convertirlos en gráficos que estremecen (pero que siempre pasan por control de calidad). Si algo huele a error o a etiqueta mal escrita, allí aparece un panda con una lupa y un cuaderno de notas.

Advertencia: nuestros análisis dan miedo 👻 a los datos sucios.

### 🌍 Cómo usar  
Clona este repositorio.    
Instala las dependencias necesarias:  
- seaborn  
- matplotlib  
- pandas  
- numpy  
- scipy
  
Ejecuta el proyecto.  
Ejecuta la presentación en Tableau.

🪐 Autor
Rocío Ramírez

### 🌌 Proceso llevado a cabo para la limpieza y corrección
- **Carga de datos:** se usa la función load_csv con sep=';' para leer los ficheros trimestre1-trimestre4 pertenecientes al año 2024 y se mantienen las copias originales.
- **Estandarización:** se normalizan los nombres de columnas: strip, lower y espacios→guión bajo; se eliminan los caracteres no alfanuméricos.
- **Unión:** se asegura el conjunto de columnas (cols_union), se añade el campo 'trimestre' y se concatena con df_all.
- **Limpieza numérica:** se convierte la columna 'total' a numérico, se eliminan los separadores de miles ('.'), se cambia la coma decimal a punto y se convierten con pd.to_numeric(errors='coerce').
- **Detección inteligente de columnas (búsqueda heurística):** comunidad/autonomía, tipología, periodos.
- **Filtrado de filas no deseadas:** exclusión de filas agregadas (regex para 'total', 'nacional', 'en el extranjero', etc.) y filas de variación porcentual.

### 🚀 Respuestas a las preguntas del cliente
1. **¿Qué tipología penal concentra más hechos en cada trimestre?**
![](https://github.com/user-attachments/assets/e7f30c72-ebb9-430b-8224-c06150809bf0)
La criminalidad convencional es la más frecuente en todos los trimestres.

2. **¿Cómo evoluciona el total de delitos por comunidad autónoma a lo largo de los trimestres?**
![](https://github.com/user-attachments/assets/c2f91ada-cbde-4aed-aad4-4be6985a981f")
Cataluña, Andalucía, Madrid, Comunidad Valenciana y País Vasco.

3. **¿Qué comunidades tuvieron más homicidios y asesinatos?**
![](https://github.com/user-attachments/assets/2ecc240d-fca3-45a9-ab21-040ea9c4ab0e)
Comunidad Valenciana, Extremadura, Andalucía, Cantabria y Cataluña.

5. **¿En qué periodos se concentran más delitos por tipología y trimestre?**
![](https://github.com/user-attachments/assets/e43080a2-60ea-47e0-bae1-28eeb875a30c)
En enero-diciembre del trimestre 4.

### 🌋 Hallazgos
- La criminalidad convencional aparece como el delito más frecuente en todos los trimestres.
- Top 5 comunidades con más delitos: Cataluña, Andalucía, Madrid, Comunidad Valenciana y País Vasco.
- Top 5 comunidades con más homicidios y asesinatos: Comunitat Valenciana, Extremadura, Andalucía, Cantabria y Cataluña.
- Periodos: tras convertir los periodos acumulativos a no‑acumulativos, la mayor incidencia queda en el tramo final del año (trimestre 4).

### 🧭 Recomendaciones estratégicas
- Calcular tasas por 100k habitantes para ajustar por tamaño de la población y así medir el riesgo real por habitante. 
- Filtrar comunidades con pocas observaciones y aplicar control de outliers antes de interpretar la variabilidad.
- Calcular intervalos de confianza (poisson) para ver si las diferencias son estadísticamente relevantes.
- Agrupar CCAA por perfil de delitos (clustering) para proponer políticas regionales compartidas.
