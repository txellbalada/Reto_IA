# Reto_IA
Este repositorio contiene el código, los datos y la documentación para el Reto de IA. Nuestro objetivo principal es desarrollar y entrenar un modelo de Machine Learning capaz de distinguir con alta precisión si un archivo de audio es una voz humana real o si ha sido generado sintéticamente por Inteligencia Artificial.

📁 Estructura del Repositorio
El proyecto está dividido en varias fases, reflejadas en los siguientes archivos y carpetas:

📓 1_Pipeline_extraccion_features.ipynb

Descripción: Es el motor de procesamiento de datos. Este notebook carga los archivos de audio sin procesar, extrae sus características acústicas clave (features como MFCC, ZCR, RMS) y genera las etiquetas de los metadatos basándose en la nomenclatura de los archivos.

Salida: Exporta los resultados limpios a los archivos CSV.

📊 CSVs de datos extraídos (Ej. 500chileno_dataset_features_real.csv)

Descripción: Contiene los datasets estructurados generados por el pipeline. Estos archivos tabulares incluyen el ID del audio, sus características estadísticas (medias y desviaciones estándar) y la variable objetivo o label (0 = Real, 1 = IA), listos para alimentar los modelos.

📈 2_Analisis_Datos_VX.ipynb

Descripción: Archivo dedicado al Análisis Exploratorio de Datos (EDA) y al modelado. Aquí se inspeccionan los CSVs, se eliminan las variables redundantes, se visualizan las distribuciones y se entrenan/evalúan los modelos de clasificación (ej. XGBoost, Random Forest).

⚙️ Flujo de Trabajo (Pipeline)
Ingesta: Lectura iterativa de los archivos .wav desde el directorio de origen.

Procesamiento: Extracción de ~600 características estadísticas optimizadas para evitar la maldición de la dimensionalidad.

Consolidación: Guardado de los datos en formato CSV.

Modelado: Entrenamiento del clasificador y análisis de la importancia de las variables (Feature Importance).

🛠️ Tecnologías y Librerías Utilizadas
Para ejecutar los notebooks de este repositorio, se necesita tener instaladas las siguientes dependencias:

Python 3.8+

librosa (Procesamiento de audio y extracción de features)

pandas y numpy (Manipulación de DataFrames y cálculos matemáticos)

scikit-learn (Métricas de evaluación y preprocesamiento)

xgboost (Entrenamiento del modelo predictivo)

matplotlib / seaborn (Visualización de datos)

👥 Equipo
Geovana Daniela Camacho
Sofía Cardona 
Meritxell Balada
