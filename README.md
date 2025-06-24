# Análisis y modelo predictivo de riesgo de suicidio en población infantil y juvenil - Colombia

Este proyecto analiza los presuntos intentos de suicidio reportados por el Instituto Nacional de Medicina Legal y Ciencias Forenses en Colombia (2015–2023). Se seleccionó la población específica entre 0 y 17 años.

## 🎯 Objetivo

Explorar y comprender los patrones del fenómeno en la infancia y adolescencia. 
Además, construir una variable de “Riesgo Alto” con base en criterios psicosociales, y entrenar un modelo predictivo que permita identificar factores relevantes.

## 🔍 Dataset

Fuente: [Datos Abiertos Colombia - Medicina Legal](https://www.datos.gov.co)

Filtrado por:
- Limpieza de datos, columnas con valores nulos, filas duplicadas, selección de datos pertinentes según criterio propio
- Ciclo vital: Primera infancia, Infancia y Adolescencia
- Columnas relevantes como: edad, sexo, escolaridad, razón del suicidio, entre otras

## 📈 Análisis exploratorio

Algunos hallazgos:
- Mayor número de casos en adolescentes (12 a 17 años)
- Predominio en hombres
- Las razones más comunes (cuando disponibles): desamor, enfermedades mentales o físicas
- Mayor frecuencia en Antioquia y Bogotá; predominio en ciudades grandes
- Aumento significativo en 2022, probablemente relacionado al fin del confinamiento

## 🤖 Modelo Predictivo

Se definió una variable binaria `Riesgo Alto` bajo estos criterios:
- Adolescente (12 a 17 años)
- Sexo masculino
- Razón: Desamor, enfermedad física o mental
- Zona: Cabecera municipal
- Año: 2022 o posterior

Modelo usado: `RandomForestClassifier`

Resultados:
- Alta precisión general
- Dificultad para detectar casos de riesgo alto (clase minoritaria)
- Variables más relevantes: Escolaridad, Sexo femenino, Actividad durante el hecho
## 📊 Visualizaciones del Análisis Exploratorio

A continuación se presentan algunas gráficas que permitieron identificar patrones importantes sobre los intentos de suicidio en población infantil y juvenil en Colombia.

### 🗓 Casos por año y por mes

Estas gráficas muestran la evolución de los casos reportados entre 2015 y 2023. El año con mayores cifras fue 2022, los mes con tasas más altas son Abril y Agosto.

![Casos por año](images/casos_x_año.jpg)
![Casos por mes](images/casos_x_mes.jpg)

### 👤 Distribución por sexo y ciclo vital

De la población seleccionada, la mayoría de los casos ocurren en adolescentes, con una prevalencia en varones.

![Casos por sexo](images/casos_x_sexo.jpg)
![Ciclo vital](images/ciclo_vital.jpg)

### 🌍 Ubicación geográfica

La mayoría de los casos se presentan en cabeceras municipales y se concentran en departamentos como Antioquia y Bogotá.

![Zona del hecho](images/zona.jpg)
![Municipios](images/municipios.jpg)
![Departamentos](images/departamentos.jpg)

### 💔 Razones del suicidio

Aunque muchos registros no incluyen esta información, entre las razones más comunes reportadas se encuentran: desamor, enfermedades mentales y enfermedades físicas.

![Razones del suicidio](images/razones.jpg)

> ⚠️ Este modelo no busca diagnosticar ni reemplazar juicio clínico. Es un ejercicio exploratorio que muestra cómo el análisis de datos puede apoyar la investigación social.

## 🧠 Reflexión

Como psicóloga interesada en ciencia de datos, este proyecto me permitió conectar estadística, conocimiento contextual y sensibilidad humana. El resultado no es un algoritmo perfecto que logra predecir un tema tan delicado como el suicidio, sin embargo es una herramienta que permite pensar los datos que se tienen frente al tema, analizando las posibles variables asociadas a este evento y utilizando las cifras para estudiar el fenómeno triste de acabar con la propia vida. Esta exploración permite comprender cómo la interpretación y manipulación influye en los modelos, siendo entrenados con las características dadas por el analista según corresponda.

## 🛠️ Herramientas

- Python (pandas, matplotlib, scikit-learn)
- Jupyter Notebook
- GitHub
