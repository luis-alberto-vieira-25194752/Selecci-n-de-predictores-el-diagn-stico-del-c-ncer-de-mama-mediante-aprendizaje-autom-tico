# Selección de predictores y reducción de dimensionalidad para optimizar el diagnóstico del cáncer de mama mediante aprendizaje automático

## Introducción
Este proyecto tiene como objetivo predecir y diagnosticar el cáncer de mama utilizando cinco algoritmos de aprendizaje automático: regresión logística, árboles de decisión, bosques aleatorios, máquinas de vectores de soporte y naive bayes. Utilizando los datos de cáncer de mama de la Universidad de Wisconsin, se realizó una exploración profunda de los datos y se aplicaron diversos métodos de selección de predictores para optimizar los modelos predictivos.

## Descripción del proyecto
El proyecto se centra en la predicción y el diagnóstico del cáncer de mama mediante el uso de algoritmos de aprendizaje automático y un proceso detallado de selección de predictores. Se realizó una exploración exhaustiva de los datos, identificando valores perdidos y duplicados, y visualizando las correlaciones entre las variables predictoras. A partir de estas correlaciones, se seleccionaron las variables más relevantes para los modelos de aprendizaje automático.
Los datos se dividieron en conjuntos de entrenamiento y prueba, y se aplicaron cinco modelos para evaluar su desempeño en términos de exactitud, precisión, sensibilidad y F1_score. Los mejores modelos fueron la regresión logística y el bosque aleatorio, cuando se usaron 16 predictores. Luego, los predictores se seleccionaron utilizando diversos métodos de selección como SelectKBest y eliminación recursiva de características (RFE). Se evaluó el desempeño de estos dos mejores modelos con los cinco predictores seleccionados por ambos métodos de selección, SelectKBest y RFE.
Además, se seleccionaron los cinco mejores predictores mediante coeficientes de la regresión logística y se evaluó su importancia. También se seleccionaron los cinco predictores y su ranking en el modelo de bosque aleatorio. Se compararon los métodos de selección de predictores mencionados y se analizó la coincidencia de los predictores dependiendo del modelo. Los predictores evaluados mediante el bosque aleatorio coincidieron en casi todos los métodos de selección.
Posteriormente, se realizó un análisis de componentes principales (PCA) y una visualización de la varianza explicada en datos normalizados. Se seleccionaron tres componentes principales que explicaron el 70% de la variabilidad de los datos para una interpretación más clara. Luego, se identificaron los predictores claves mediante PCA en datos normalizados. De los tres primeros componentes principales identificados, se seleccionaron los cinco predictores más relevantes para cada uno.
Al comparar los modelos de regresión logística y bosque aleatorio con diferentes conjuntos de predictores, se evaluaron estos tres conjuntos de predictores utilizando validación cruzada con modelos de regresión logística y bosque aleatorio. Se identificaron los predictores comunes entre los modelos de regresión logística, bosque aleatorio y PCA. Por otro lado, se obtuvieron los siguientes resultados de la validación cruzada:

**Regresión logística**:
- common_predictors + logistic_predictors: score 0.846
- common_predictors + forest_predictors: score 0.909
- common_predictors + PCA: score 0.894

**Bosque aleatorio**:
- common_predictors + logistic_predictors: score 0.897
- common_predictors + forest_predictors: score 0.919
- common_predictors + PCA: score 0.944

El modelo de bosque aleatorio mostró scores más altos. Por lo tanto, se recomienda utilizarlo como modelo principal para optimizar la precisión de las predicciones. 
Por último, se mostraron en un gráfico de barras los cinco predictores más importantes en un modelo de bosque aleatorio.

## Características principales del proyecto
-	Exploración de datos: Análisis de valores perdidos, duplicados y visualización de correlaciones entre variables predictoras.
-	Modelos de aprendizaje automático: Implementación de regresión logística, árboles de decisión, bosques aleatorios, máquinas de vectores de soporte y naive bayes, y comparación de su desempeño.
-	Selección de predictores: Uso de métodos como SelectKBest y RFE para seleccionar las variables más relevantes.
-	Modelos de aprendizaje automático: Implementación de los dos mejores modelos: regresión logística y bosque aleatorio, y comparación de su desempeño.
-	Optimización de modelos: Uso de RFECV para determinar el número óptimo de predictores y mejorar la precisión de los modelos.
-	Selección de predictores más importantes: Uso de métodos como coeficientes de la regresión logística y evaluación de la importancia y ranking de predictores en bosque aleatorio.
-	PCA: Identificación de componentes principales que explican el 70% de la variabilidad.
-	Comparación de modelos: Evaluación de tres conjuntos de predictores utilizando validación cruzada con modelos de regresión logística y bosque aleatorio.
-	Visualización de los predictores más importantes: En un modelo de bosque aleatorio.

## Herramientas utilizadas
**Lenguaje de programación**: 
-	Python
**Librerías de Python**:
-	Pandas (para manipulación de datos)
-	Numpy (para operaciones numéricas)
-	Matplotlib y seaborn (para visualización de datos)
-	Scikit-learn (para preprocesamiento y evaluación de modelos)
-	Entorno de desarrollo: Jupyter Notebook
-	Dataset: Wisconsin Breast Cancer Dataset

## Conclusión
La conclusión principal de este proyecto es que la combinación de diferentes métodos de selección de predictores y algoritmos de aprendizaje automático puede mejorar significativamente la precisión y el rendimiento en la detección y diagnóstico del cáncer de mama. Los modelos de bosque aleatorio y regresión logística demostraron ser los más efectivos, especialmente cuando se utilizaron predictores seleccionados mediante métodos como SelectKBest, RFE y PCA.
Además, el PCA ayudó a identificar los predictores más relevantes, explicando el 70% de la variabilidad de los datos. La validación cruzada mostró que los modelos de bosque aleatorio tuvieron un rendimiento ligeramente superior en comparación con la regresión logística, especialmente cuando se utilizaron predictores comunes y seleccionados por PCA.
La integración de técnicas avanzadas de selección de características y algoritmos de aprendizaje automático puede proporcionar herramientas poderosas para el diagnóstico temprano y preciso del cáncer de mama. La selección de predictores mediante diferentes métodos mostró consistencia en los resultados, reforzando la confianza en la relevancia de los predictores seleccionados. La combinación de enfoques supervisados y no supervisados proporcionó una visión completa y confiable para construir modelos predictivos robustos y precisos.

## Inspiración y agradecimiento
Este proyecto se inspiró en este trabajo compartido en Kaggle Feature Selection and Data Visualization (kaggle.com), el cual ofreció valiosas percepciones sobre el aprendizaje. Agradezco enormemente al autor por compartir su conocimiento y recursos con la comunidad de código abierto.

## Estado del proyecto
Finalizado

