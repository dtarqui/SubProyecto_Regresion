# Predicción de Precios de Bienes Raices en Australia - Regresión Avanzada

## Índice

- [Índice](#índice)
- [Introducción](#introducción)
  - [Métodos Utilizados](#métodos-utilizados)
  - [Tecnologías](#tecnologías)
- [Descarga y Configuración](#descarga-y-configuración)
  - [Requisitos Previos](#requisitos-previos)
  - [Cómo Ejecutar](#cómo-ejecutar)
- [Declaración del Problema](#declaración-del-problema)
  - [Objetivo Comercial](#objetivo-comercial)
  - [Preparación de Datos:](#preparación-de-datos)
  - [Construcción y Evaluación del Modelo](#construcción-y-evaluación-del-modelo)
  - [Conclusiones](#conclusiones)
    - [Regresión Ridge](#regresión-ridge)
    - [Regresión Lasso](#regresión-lasso)
    - [Regresión ElasticNet](#regresión-lasso)
    - [Las Variables Más Significativas Son:](#las-variables-más-significativas-son)

## Introducción

...

### Métodos Utilizados
...

### Tecnologías
* Python
* Pandas
* PyCaret
...

## Descarga y Configuración
### Requisitos Previos

Este proyecto necesita que Anaconda esté instalado en la computadora.

Para más detalles sobre la instalación, visite: https://docs.anaconda.com/anaconda/install/index.html

### Cómo Ejecutar

Puede descargar el código fuente clonando este repositorio usando Git:

1. Abra su aplicación Terminal favorita (Unix, Linux o Macos), como Terminal, Comando, Consola, iTerm2, etc.

2. Clone el repositorio

```
git clone <GITHUB_REPO_URL>
```

3. Abra el archivo notebook ** *.ipynb** en Anaconda.

```
jupyter notebook <FILE.ipynb
```


## Declaración del Problema

...

### Objetivo Comercial

...

---

### Preparación de Datos:

1. Limpieza de Datos y Análisis de Datos Faltantes.
2. Análisis y Tratamiento de Valores Atípicos.
3. Derivación de Columnas Categóricas.
4. Análisis Univariable.
5. Análisis Bivariable.
6. Análisis Multivariable.

### Construcción y Evaluación del Modelo

1. División de datos de entrenamiento y prueba.
2. Escalado de Características - StandardScaler.
3. Ingeniería y Selección de Características usando RFE y el Factor de Inflación de Varianza.
4. Regresión Lineal usando PyCaret.
5. Modelos de Regularización Ridge, Lasso y ElasticNet.
6. Análisis de Residuos.
7. Evaluación y Valoración del Modelo.
8. Predicción.
9. Conclusión y Análisis Final.

### Conclusiones

### Conclusions

R2_Score for Ridge regresion.... 
R2_Score for Lasso regresion.... 
R2_Score for ElasticNet regresion.... 

#### Ridge Regression (Segun PyCaret)
* **Optimal Lambda Value:** ##
* **R2 Score Train:** 0.##
* **R2 Test Score:**  0.##
* **RMSE Test:**      0.##

#### Lasso Regression (Segun PyCaret)
* **Optimal Lambda Value:** 0.####
* **R2 Score Train:**  0.##
* **R2 Test Score:**   0.##
* **RMSE Test:**       0.##

#### ElasticNet Regression (Segun PyCaret)
* **Optimal Lambda Value:** 0.####
* **R2 Score Train:**  0.##
* **R2 Test Score:**   0.##
* **RMSE Test:**       0.##

#### Las Variables Más Significativas Son:
* ...
* ...
* ...
* ...
