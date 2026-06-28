# **Model Selection & Ensemble** 

**By Jheser Guzman - @Bluminds** 

## 

2 

1 

## **Introducción** 

**Cross Validation** K-Folds, LOOCV, Stratified, Groups, Monte-Carlo 

Tipos de Selección 

3 

4 

5 **Automatic Selection** Pycaret 

**Optimización de Hiperparametros** Grid Search Random Search 

**Ensemble** Bagging, Stacking, Boosting 

# **Model Selection** 

## **¿Que es Model-Selection?** 

Proceso de seleccionar el mejor modelo de ML para un conjunto de datos determinado. 

## **Tecnicas de Model-Selection** 

- **Validación Cruzada:** Técnica para evaluar el rendimiento de un modelo en un conjunto de datos. Esta técnica divide el conjunto de datos en K-Folds para train y test. Los resultados se promedian para obtener una medida general del rendimiento del modelo. 

- **Optimización de Hiperparámetros:** Los hiperparámetros de los modelos de ML deben ser ajustados para obtener mejores resultados. Esto puede hacerse utilizando técnicas como la GridSeach, la búsqueda aleatoria o la optimización bayesiana. 

- **Ensemble Learning:** Ensemble Learning implica combinar varios modelos de ML para mejorar el rendimitno del modelo. Las técnicas de Ensemble Learning incluyen Bagging, Boosting y Stacking. 

- **Selección Automática de Modelos:** Algoritmos de selección automática de modelos incluyen el algoritmo de selección de modelo automático (AutoML) y el algoritmo de búsqueda de modelos (Model Search). 

# **Cross Validation** 

## **Cross Validation** 

Cross Validation es una **técnica de evaluación** de modelos de ML que consiste en **dividir los datos** disponibles en diferentes conjuntos de **entrenamiento y prueba** de manera repetida. 

**Objetivos:** Evaluar el rendimiento del modelo de manera más precisa y reducir el riesgo de sobreajuste. 

- K-Fold 

- Leave-One-Out 

- Estratificada. 

- K-Fold Grupos 

- Monte Carlo (Shuffle) 

## **Cross Validation – K-Folds** 

**K-Fold:** Divide los datos en **k partes iguales (folds)** , entrena y evalúa el modelo k veces, utilizando una partición diferente test en cada iteración y el resto de los datos como conjunto de entrenamiento.  Al final, se **calcula la media** de las métricas de evaluación obtenidas en cada iteración. 

## **Cross Validation – K-Folds en Python** 

## **Cross Validation – LeaveOneOut** 

**Leave-One-Out (LOOCV):** Utilizada para conjuntos de datos pequeños y deja un solo ejemplo como conjunto de prueba en cada iteración y utiliza todos los demás ejemplos como conjunto de entrenamiento. El proceso se repite para todos los ejemplos y se calcula la media de las métricas de evaluación obtenidas. 

## **Cross Validation – LeaveOneOut** 

## **Cross Validation – Stratified** 

**Estratificada:** Utilizada para clasificación cuando **las clases no están equilibradas** . Se asegura de que cada partición contenga una proporción equilibrada de ejemplos de cada clase. Esto ayuda a **evitar la sobre-estimación o sub-estimación** de la precisión y otras métricas de evaluación. 

## **Cross Validation – Stratified en Python** 

## **Cross Validation – Group K-fold** 

**Por Grupos:** Utiliza para problemas en los que los ejemplos tienen una estructura de grupos, como en el análisis de series de tiempo o en los estudios longitudinales. Se asegura de que los ejemplos pertenecientes al mismo grupo no estén presentes en ambos conjuntos de entrenamiento y prueba. 

## **Cross Validation – Monte-Carlo** 

**Monte Carlo (Shuffle):** Se generan de manera aleatoria **k particiones** del conjunto de datos en **entrenamiento y prueba** , y se entrenan **y evalúan k veces el modelo** . La ventaja de esta técnica es que se puede obtener una mejor estimación de la variabilidad del modelo y reducir la influencia de particiones particulares. 

# **Optimización de Hiperparámetros** 

## **Tecnicas de Model-Selection** 

Los hiper-parámetros de los modelos de ML deben ser ajustados para obtener mejores resultados. 

Entre las técnicas conocidas tenemos: 

- GridSeach 

- Randomized Search 

- Optimización Bayesiana. 

## **Grid Search Cross Validation** 

**GridSearchCV** es una técnica de búsqueda exhaustiva (todas las combinaciones) de hiperparámetros en el ML, que permite buscar la mejor combinación de hiperparámetros para un modelo determinado. 

## **Randomized Search** 

**RandomizedSearchCV** es una técnica de optimización de hiperparámetros que implica la selección aleatoria de combinaciones de valores de para entrenar y evaluar un modelo de aprendizaje automático. Esta permite probar una amplia gama de valores en un tiempo razonablemente corto usando una distribución de probabilidad para cada hiperparámetro. 

## **Optimización Bayesiana** 

**Bayesian-Optimization** utiliza el enfoque del Teorema de Bayes para encontrar la mejor combinación de hiperparámetros para un modelo determinado. 

Utiliza una función objetivo y una distribución de probabilidad a priori sobre los valores de los hiperparámetros para obtener una distribución de probabilidad posterior. La distribución de probabilidad posterior se actualiza a medida que se observan más datos 

**==> picture [25 x 7] intentionally omitted <==**

**----- Start of picture text -----**<br>
PAGE | 146.0<br>**----- End of picture text -----**<br>


# **Ensemble** 

## **Limitaciones de los Modelos de ML** 

- Sensibilidad a los datos frente a Outliers. 

- • Sobreajuste y  Falta de Generalización. 

- • Complejidad computacional. 

- • Sesgo en la selección de un modelo. 

## **¿Que es Ensemble?** 

Técnica de ML que **combina múltiples modelos** para mejorar la precisión y el rendimiento de la predicción 

- Bagging (Bootstrap Aggregation) 

- Stacking 

- • Boosting 

## **Ventajas de Ensemble** 

Mejora significativamente la precisión y la estabilidad de los modelos de aprendizaje automático. Es especialmente útil en situaciones donde se necesitan predicciones precisas y robustas en conjuntos de datos complejos. 

- **Mejora de la precisión** 

   - Combinar varios modelos de ML cuando los datasets son complejos o ruidosos. 

- **Reducción del Overfitting:** 

Se debe a que el promedio de las predicciones de varios modelos puede ser más generalizable y menos propenso a ajustarse demasiado a los datos de entrenamiento. 

## • **Estabilidad del modelo:** 

Reduce la varianza y el riesgo de modelos defectuosos o inestables. 

- **Menos ruidosos:** 

Menos propenso a errores de medición o datos faltantes. 

- **Tolerancia a fallos:** 

El promedio de las predicciones de varios modelos suelen ser más robustos y tolerantes a estos fallos individuales. 

## **Decision Tree** 

Modelo de ML donde cada nodo interno representa una característica del conjunto de datos, cada rama representa una decisión basada en esa característica, y cada hoja representa una clase o un valor de salida. 

## **Random Forest** 

Random Forest es un algoritmo de ML que utiliza la técnica de Bagging en Ensemble para mejorar la precisión y la estabilidad de los modelos de Decision Trees. 

## **Random Forest en Python** 

# **Bootstrap Aggregation** 

## **¿Que es Bagging?** 

Técnica que **entrena un conjunto de modelos independientes** utilizando diferentes subconjuntos aleatorios del conjunto de datos de entrenamiento. 

## **Bagging + Clasificacion** 

Bagging (Boostrapping Aggregation) es una **técnica** útil de ensamblaje de modelos que puede mejorar la precisión y la estabilidad de las predicciones combinando múltiples modelos ajustados en diferentes muestras de datos de entrenamiento. 

## **Bagging + Clasificacion** 

## **Bagging Example** 

## **Bagging en Python** 

# **Stacking** 

## **Stacking** 

Stacking (Stacked Generalization) es una técnica de ensamblaje de modelos que **combina múltiples modelos** de ML **para mejorar la precisión y el rendimiento de las predicciones** . La idea detrás de Stacking es utilizar las predicciones de múltiples modelos base como características para entrenar un modelo final, llamado metamodelo, que combina las predicciones de los modelos base para producir una predicción final. 

## **Stacking en Python** 

## **Bagging vs Stacking** 

|**Característica**|**Bagging**|**Stacking**|
|---|---|---|
|**Muestras de**<br>**entrenamiento**|Se generan múltiples muestras de<br>entrenamiento utilizando muestreo con<br>reemplazo (bootstrap) y se ajusta un modelo<br>base a cada muestra.|Se utilizan múltiples modelos base entrenados<br>en el conjunto de entrenamiento original y sus<br>predicciones se utilizan para ajustar un meta-<br>modelo.|
|**Combinación de**<br>**modelos**|Las predicciones de los modelos base se<br>combinan mediante votación, promedio o<br>ponderación.|Las predicciones de los modelos base se<br>utilizan como características para ajustar un<br>meta-modelo.|
|**Nivel de complejidad**<br>~~a~~|Relativamente simple en términos de diseño e<br>implementación.|Mayor complejidad debido a la necesidad de<br>ajustar un meta-modelo en las predicciones de<br>múltiples modelos base.|
|**Selección de modelos**<br>~~a~~|Se puede utilizar con cualquier modelo<br>predictivo como modelo base.|Funciona mejor con modelos heterogéneos (es<br>decir, modelos que tienen diferentes<br>arquitecturas, técnicas de entrenamiento y<br>parámetros).|



# **Boosting** 

## **Boosting** 

Boosting es una técnica de ensamblaje de modelos que combina múltiples modelos de aprendizaje automático para mejorar la precisión y el rendimiento de las predicciones. A diferencia de Bagging, no utiliza muestreo con reemplazo (bootstrap) para generar múltiples muestras de entrenamiento, sino que se enfoca en **secuencialmente mejorar un único modelo base mediante ajuste iterativo de pesos** en las muestras de entrenamiento. 

## **Tipos de Boosting** 

Boosting es una técnica de ensamblaje de modelos que combina múltiples modelos de aprendizaje automático para mejorar la precisión y el rendimiento de las predicciones. A diferencia de Bagging, no utiliza muestreo con reemplazo (bootstrap) para generar múltiples muestras de entrenamiento, sino que se enfoca en **secuencialmente mejorar un único modelo base mediante ajuste iterativo de pesos** en las muestras de entrenamiento. 

- AdaBoost. 

- Gradient Boosting 

- XGBoost (Extreme Gradient Boosting) 

- LightGBM 

- CatBoost 

## **AdaBoost** 

El algoritmo AdaBoost (Adaptive Boosting) fue uno de los primeros algoritmos de Boosting propuestos. 

- Ajusta el modelo base en las muestras de entrenamiento ponderadas y utiliza la suma ponderada de los modelos base para producir una predicción final. 

- En cada iteración, se ajustan los pesos de las muestras de entrenamiento para dar mayor peso a las muestras que se ajustaron incorrectamente en la iteración anterior. 

## **AdaBoost en Python** 

## **Gradient Boosting (GB)** 

El algoritmo Gradient Boosting es un enfoque más general de Boosting que se enfoca en ajustar un modelo que minimice la función de pérdida. 

- en 

- En cada iteración, se ajusta un modelo base para **minimizar la función de pérdida** las muestras de entrenamiento ponderadas. 

- Se utiliza la suma ponderada de los modelos base para producir una predicción final. 

## **Gradient Boosting (GB) en Python** 

## **XGBoost** 

XGBoost (Extreme Gradient Boosting) es una implementación de Gradient Boosting que utiliza técnicas adicionales como la regularización y el manejo de valores faltantes para mejorar el rendimiento y la velocidad de la implementación. 

## **LightGBM** 

LightGBM es otra implementación de Gradient Boosting que utiliza técnicas de agrupamiento y ordenamiento de características para mejorar el rendimiento y la velocidad de la implementación. 

## **CatBoost** 

CatBoost es un algoritmo de Boosting que utiliza una técnica de codificación de características categóricas para mejorar el rendimiento en conjuntos de datos con características categóricas. 

## **Boosting Resumen** 

|**Algoritmo**|**Técnica de**<br>**Ensemble**|**Tipo de problema**|**Velocidad y**<br>**escalabilidad**|**Requerimientos de**<br>**memoria**|**Sensibilidad al**<br>**ruido y valores**<br>**atípicos**|**Flexibilidad de**<br>**hiperparámetros**|
|---|---|---|---|---|---|---|
|**AdaBoost**|Boosting clásico|Clasificación y<br>Regresión|Rápido y escalable|Bajo|Sensible|Baja|
|**Gradient Boosting**|Boosting secuencial|Clasificación y<br>Regresión|Moderadamente<br>rápido y escalable|Moderado|Sensible|Alta|
|**XGBoost**|Boosting secuencial|Clasificación y<br>Regresión|Rápido y escalable|Moderado|Sensible|Alta|
|**LightGBM**|Boosting secuencial|Clasificación y<br>Regresión|Muy rápido y<br>escalable|Bajo|Sensible|Alta|
|**CatBoost**|Boosting secuencial|Clasificación y<br>Regresión|Rápido y escalable|Moderado|Robusto|Alta|



# **Selección Automatica de Modelos** 

## **Automatic Model Selection** 

AutoML se refiere a la automatización de todo el proceso de ML, enfocado en: 

- La selección de características 

- La preparación de datos hasta la optimización de modelos 

- La implementación de soluciones para pase a Producción. 

AutoML automatiza gran parte del proceso para hacer que el aprendizaje automático sea más accesible y escalable. 

Entre las herramientas que se usan tenemos: 

- Pycaret y Scikit-learn 

- Google AutoML 

- H2O.ai 

- DataRobot. 

## **AutoML con Pycaret** 

## **AutoML con Pycaret** 

## **Opt. de HyperParametros con Pycaret** 

