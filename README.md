![](https://github.com/Roxy-5/Evaluacion1-Adalab/blob/main/image.jpg?raw=true)
### Criminal Pandas 🔪🩸
Analizamos los delitos de España en el año 2024 para conocer sus tendencias de criminalidad por comunidades autónomas. Así podremos prevenirlos, priorizar recursos y diseñar las intervenciones adecuadas.

### 🎬 Storytelling
Somos Criminal Pandas 🐼: un escuadrón de analistas nocturnos que merodean entre tablas y gráficos 📊. Bajo la luz tenue del PC olfateamos anomalías, atrapamos outliers como si fuera bambú y convertimos datos sospechosos en pruebas irrefutables.

Dicen que, cuando cae la noche, los trimestres susurran secretos y nosotros los escuchamos para convertirlos en gráficos que estremecen. Si algo huele a error o a etiqueta mal escrita, allí aparece un panda con su cuaderno de notas y lupa en mano para registrarlo todo.

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
- **Carga segura:** se usa la función load_csv con sep=';' para leer los ficheros trimestre1-trimestre4 y se mantienen las copias originales.
- **Estandarización:** se normalizan los nombres de columnas: strip, lower y espacios→guión bajo; se eliminan los caracteres no alfanuméricos.
- **Unión:** se asegura el conjunto de columnas (cols_union), se añade el campo 'trimestre' y se concatena con df_all.
- **Limpieza numérica:** se convierte la columna 'total' a numérico, se eliminan los separadores de miles ('.'), se cambia la coma decimal a punto y se convierten con pd.to_numeric(errors='coerce').
- **Control de calidad:** se registran shape, dtypes, nulos y duplicados.
- **Correcciones rápidas:** se usan las variables correctas en bucles (df vs dfc).
- **Detección inteligente (búsqueda heurística):** de las columnas comunidad/autonomía, tipología y periodos por si sus nombres varían algo.
- **Filtrado:** exclusión de filas agregadas (regex para 'total', 'nacional', 'en el extranjero') y filas de variación porcentual por no ser relevantes.

### 🚀 Respuestas a las preguntas del cliente
1. **¿Qué tipología penal es más frecuente por trimestre?**
![](https://github.com/user-attachments/assets/7f13bd30-6832-4273-8ba5-12a4208517ca)
La criminalidad convencional es la más frecuente en todos los trimestres.

2. **Top 5 comunidades autónomas con más delitos por trimestre**
![](https://github.com/user-attachments/assets/d37c77a6-054e-46f7-a32d-7a35fc894367)
Cataluña, Andalucía, Madrid, Comunidad Valenciana y País Vasco.

3. **¿Qué comunidades tuvieron más homicidios y asesinatos?**
![](https://github.com/user-attachments/assets/358671cc-0eb7-499e-8b1d-903f7c0850cd)
Comunidad Valenciana, Extremadura, Andalucía, Cantabria y Cataluña.

5. **¿En qué periodos se concentran más delitos por tipología y trimestre?**
![](https://github.com/user-attachments/assets/149099d2-8ae4-487f-b211-c89084c3ce0b)
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
