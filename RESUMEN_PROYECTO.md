# Resumen del Proyecto – Regresión Avanzada con PyCaret

## Datos Generales

| Campo | Detalle |
|---|---|
| **Materia** | Inteligencia Artificial y MLOps |
| **Profesor** | Jheser Guzman Ph.D. |
| **Fecha de entrega** | Martes 30 de Junio 2026 – 23:59 |
| **Formato de entrega** | Email al profesor con URL del repositorio de GitHub |

---

## Contexto del Negocio

**Surprise Housing** es una empresa de vivienda estadounidense que quiere entrar al mercado australiano. Su modelo de negocio consiste en comprar propiedades por debajo de su valor real y revenderlas a mayor precio.

La empresa necesita responder dos preguntas clave:

1. ¿Qué variables son significativas para predecir el precio de una casa?
2. ¿Qué tan bien describen esas variables el precio de una casa?
3. ¿Cuál es el valor óptimo de **lambda** para Ridge y Lasso?

---

## Objetivo Técnico

Construir un **modelo de regresión con regularización** que prediga el valor real de propiedades australianas, usando el dataset CSV provisto en `_data/dataset.csv`.

---

## Estructura del Notebook (lo que hay que completar)

### 1. Introducción
- [ ] Completar nombres e emails de los integrantes del grupo

### 2. Configuración e Instalación
- Librerías ya importadas: `numpy`, `pandas`, `matplotlib`, `seaborn`, `pycaret`, `sklearn`, `statsmodels`

### 3. Entendimiento de los Datos
- [ ] Exploración inicial del dataset (`shape`, `info`, `describe`, `head`)
- [ ] Identificar tipos de variables (numéricas vs categóricas)

### 4. Manipulación y Limpieza de Datos
- [ ] **Dropping Data**: eliminar columnas/filas irrelevantes o duplicadas
- [ ] **Derived Data**: crear nuevas métricas o columnas derivadas si aplica
- [ ] Imputación de valores faltantes (estrategia correcta y justificada)
- [ ] Creación de variables dummy para categóricas

### 5. Análisis de Datos (EDA)
- [ ] **Análisis Univariable**: distribución de variables numéricas y categóricas (histogramas, boxplots, barplots)
- [ ] **Análisis Bivariable**: correlaciones con la variable objetivo (precio)

### 6. Preparación de Datos y Modelado
- [ ] Split Train/Test (documentar el porcentaje usado)
- [ ] Escalar variables con `StandardScaler` o `MinMaxScaler`

### 7. Construcción del Modelo
- [ ] **Ridge Regression**: tuning de lambda con `GridSearchCV`
- [ ] **Lasso Regression**: tuning de lambda con `GridSearchCV`
- [ ] **ElasticNet Regression**: tuning de parámetros
- [ ] Comparar modelos con métricas: R², RMSE (u otras)
- [ ] Seleccionar el mejor modelo y justificarlo

### 8. Conclusiones y Observaciones
- [ ] Interpretar el modelo ganador en términos de negocio
- [ ] Listar las variables más importantes y su impacto en el precio
- [ ] Documentar el lambda óptimo de Ridge y Lasso

---

## Rúbrica de Evaluación

| Criterio | Peso |
|---|---|
| Entendimiento de datos, limpieza y EDA | **40%** |
| Construcción y evaluación del modelo | **50%** |
| Lineamientos de código (comentarios, nombres, legibilidad) | **10%** |

### Puntos clave para la nota máxima

**EDA (40%)**
- Todos los problemas de calidad de datos resueltos y explicados
- Dummy variables correctamente creadas
- Nuevas métricas derivadas (si aplica)

**Modelo (50%)**
- Parámetros ajustados con metodología correcta y explicada
- Consideración de aspectos técnicos Y de negocio
- Selección correcta de variables (RFE u otra técnica)
- Comparación de múltiples modelos
- Interpretación clara del modelo final

**Código (10%)**
- Comentarios donde corresponda (no en exceso)
- Nombres de variables descriptivos
- Código conciso, legible e indentado correctamente

---

## Entregables en el Repositorio GitHub

- [ ] `dataset.csv` – el dataset en `_data/`
- [ ] `MFSDv1p1_Regresion Avanzada con PyCaret.ipynb` – notebook completo y ejecutado
- [ ] `README.md` – descripción breve del proyecto

---

## Stack Tecnológico

```
Python · Pandas · NumPy · Matplotlib · Seaborn
Scikit-learn (Ridge, Lasso, ElasticNet, GridSearchCV, RFE)
Statsmodels (OLS, VIF, Durbin-Watson)
PyCaret
```
