# Predicción de Precios de Bienes Raíces — Regresión Avanzada con PyCaret

Proyecto grupal de la materia **Inteligencia Artificial y MLOps** (MFSDv1p1) — Universidad
Católica Boliviana San Pablo. Profesor: **Jheser Guzmán, Ph.D.**

## Descripción

La empresa de vivienda **Surprise Housing** quiere ingresar a un nuevo mercado inmobiliario.
Su modelo de negocio consiste en **comprar propiedades por debajo de su valor real y
revenderlas** a un precio mayor. Para apoyar esa decisión se construye un **modelo de
regresión con regularización** que:

1. Identifica **qué variables son significativas** para predecir el precio de una vivienda.
2. Mide **qué tan bien** esas variables explican el precio.
3. Determina el **valor óptimo de lambda (λ)** para las regresiones **Ridge** y **Lasso**.

> El dataset corresponde a viviendas de **Ames, Iowa (EE. UU.)** — 1460 registros y 80
> atributos. El marco de negocio del "nuevo mercado" se mantiene de forma ilustrativa.

## Estructura del repositorio

```
.
├── _data/
│   ├── dataset.csv             # Dataset (1460 x 81)
│   └── data_description.txt    # Diccionario de datos
├── MFSDv1p1_Regresion Avanzada con PyCaret.ipynb   # Notebook completo y ejecutado
├── presentaciones/             # Material de clase de referencia
└── README.md
```

## Metodología

El notebook sigue el flujo completo:

1. **Entendimiento de los datos** — dimensiones, tipos de variables y distribución del
   objetivo `SalePrice` (sesgada → se modela en escala `log`).
2. **Limpieza** — control de duplicados, eliminación de columnas no informativas
   (`Id`, `Utilities`, `Street`) e **imputación de faltantes** diferenciando los `NA` que son
   categoría ("sin garaje/sótano/piscina") de los faltantes reales (`LotFrontage` imputado
   por mediana de vecindario, etc.).
3. **Variables derivadas** — `TotalSF`, `TotalBath`, `HouseAge`, `TotalPorchSF` e indicadores
   binarios (`HasGarage`, `HasPool`, …).
4. **EDA** — análisis univariable y bivariable (histogramas, boxplots, correlaciones, heatmap).
5. **Preparación** — codificación ordinal de calidades, *dummies* para nominales, split
   80/20 y escalado con `StandardScaler`.
6. **Selección de variables** — **RFE** + **VIF** para un modelo lineal interpretable.
7. **Modelado** — comparación de múltiples modelos:
   - **AutoML con PyCaret** (`compare_models` con validación cruzada de 10 folds, incluyendo
     modelos de *ensemble*: Random Forest, Gradient Boosting, LightGBM).
   - **Regresión Lineal** (OLS, baseline interpretable).
   - **Ridge**, **Lasso** y **ElasticNet** con `GridSearchCV` para hallar el **λ óptimo**.
8. **Análisis de residuos** — gráficos de residuos, Q-Q plot y estadístico de Durbin-Watson.
9. **Predicción y conclusiones** — interpretación de negocio y variables más significativas.

## Resultados principales

- Los modelos regularizados explican aproximadamente el **85–90 % de la variabilidad** del
  precio (R² de prueba en escala logarítmica).
- Variables más influyentes: **`OverallQual`** (calidad general), la **superficie**
  (`TotalSF`, `GrLivArea`), la **calidad de cocina/exteriores**, el **garaje** y el
  **vecindario**.
- Los valores óptimos de λ para Ridge, Lasso y ElasticNet se determinan por validación
  cruzada y se reportan en el resumen final del notebook.

## Stack tecnológico

`Python 3.11` · `pandas` · `numpy` · `matplotlib` · `seaborn` ·
`scikit-learn` (Ridge, Lasso, ElasticNet, GridSearchCV, RFE, StandardScaler) ·
`statsmodels` (OLS, VIF, Durbin-Watson) · `PyCaret 3.x`

## Requisitos

| Requisito | Detalle |
|---|---|
| **Python** | **3.9, 3.10 o 3.11** (obligatorio) |
| Dependencias | ver [`requirements.txt`](requirements.txt) |

> ⚠️ **PyCaret no es compatible con Python 3.12 o superior.** Si solo dispones de una versión
> más nueva, instala adicionalmente Python 3.11 (desde [python.org](https://www.python.org/downloads/release/python-3119/)
> o con `conda`) y crea el entorno con esa versión.

## Cómo ejecutar

> 📌 **El notebook ya está ejecutado con todas sus salidas guardadas** (tablas, gráficos y
> resultados). Para **leer** el proyecto **no hace falta instalar nada**: basta
> abrir el `.ipynb` en GitHub o en Jupyter. Los pasos siguientes solo son necesarios si se
> desea **volver a ejecutarlo**.

**1. Clonar el repositorio**
```bash
git clone <URL_DEL_REPO>
cd SubProyecto_Regresion
```

**2. Crear el entorno virtual con Python 3.11**
```bash
# Windows (con el py launcher):
py -3.11 -m venv venv
venv\Scripts\activate

# macOS / Linux:
python3.11 -m venv venv
source venv/bin/activate
```

**3. Instalar las dependencias**
```bash
pip install -r requirements.txt
```

**4. Abrir y ejecutar el notebook**
```bash
jupyter notebook "MFSDv1p1_Regresion Avanzada con PyCaret.ipynb"
```
En Jupyter: menú **Kernel → Restart & Run All** para reproducir todos los resultados.

### Alternativa sin instalar nada
- **GitHub**: abre el `.ipynb` directamente en el repositorio; se renderiza con todas las salidas.
- **Google Colab**: `File → Open notebook → GitHub`, pega la URL del repo. (En Colab,
  ejecuta primero una celda con `!pip install pycaret statsmodels` ya que Colab usa otra
  versión de Python.)

## Integrantes

- Daniel Tarqui
- David Rivas
- Harold Sanchez
- Jonas Maidana
