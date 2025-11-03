# 📈 Sales Forecasting Project - Product Development

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green.svg)](https://pandas.pydata.org/)

## 🎯 Descripción del Proyecto

Este proyecto forma parte del **curso de Product Development** del **Postgrado en Análisis y Predicción de Datos** de la Universidad Galileo. Su objetivo principal es desarrollar un sistema completo de **forecasting de ventas** utilizando técnicas avanzadas de análisis de datos y machine learning.

### 🎓 Contexto Académico
- **Curso:** Product Development
- **Programa:** Postgrado en Análisis y Predicción de Datos
- **Institución:** Universidad Galileo
- **Proyecto:** #2 - Sistema de Predicción de Ventas

## 🏢 Problema de Negocio

El proyecto aborda el desafío de **predecir las ventas futuras** de múltiples productos en diferentes sucursales, considerando:

- **Múltiples productos** con diferentes patrones de demanda
- **Diversas sucursales** con comportamientos únicos
- **Estacionalidad temporal** (semanal, mensual)
- **Tendencias a largo plazo**
- **Factores externos** que afectan las ventas

## 🚀 Objetivos

### Objetivo Principal
Desarrollar un modelo de forecasting robusto y preciso que permita predecir ventas futuras con alta confiabilidad.

### Objetivos Específicos
1. **Realizar un EDA completo** del dataset de ventas
2. **Identificar patrones temporales** y estacionalidad
3. **Implementar múltiples modelos** de forecasting
4. **Evaluar y comparar** el rendimiento de los modelos
5. **Crear visualizaciones** interactivas y reportes
6. **Generar predicciones** para períodos futuros

## 📊 Dataset

### Características del Dataset
- **Registros:** 45,000 observaciones
- **Período:** 90 días (2018-01-01 a 2018-03-31)
- **Frecuencia:** Diaria
- **Granularidad:** Sucursal-Producto-Fecha

### Variables
| Variable | Tipo | Descripción |
|----------|------|-------------|
| `date` | datetime | Fecha de la venta |
| `store` | int | Identificador de la sucursal |
| `item` | int | Identificador del producto |
| `sales` | float | Cantidad de ventas (variable objetivo) |

## 🔬 Metodología

### 1. Análisis Exploratorio de Datos (EDA)
- ✅ **Comprensión inicial** del dataset
- ✅ **Validación de estructura** y calidad de datos
- ✅ **Análisis de valores faltantes** y duplicados
- ✅ **Estadísticas descriptivas** por producto y sucursal
- ✅ **Exploración temporal** y patrones estacionales
- ✅ **Análisis de autocorrelación** (ACF/PACF)
- ✅ **Detección de outliers** y comportamientos anómalos

### 2. Ingeniería de Características
- 🔄 Variables temporales (día de semana, mes, año)
- 🔄 Lags significativos (1, 7, 30 días)
- 🔄 Medias móviles (7, 14, 30 días)
- 🔄 Indicadores estacionales
- 🔄 Variables categóricas codificadas

### 3. Modelado Predictivo
- 🔄 **SARIMA:** Modelos autoregresivos estacionales
- 🔄 **Prophet:** Framework de Facebook para forecasting
- 🔄 **LSTM/GRU:** Redes neuronales recurrentes
- 🔄 **Random Forest:** Ensamble de árboles de decisión
- 🔄 **XGBoost:** Gradient boosting optimizado

### 4. Evaluación y Validación
- 🔄 Validación cruzada temporal
- 🔄 Métricas múltiples (MAPE, RMSE, MAE)
- 🔄 Intervalos de confianza
- 🔄 Análisis de residuos

## 📁 Estructura del Proyecto

```
ProductDevelopment-Proyecto2/
├── 📄 LICENSE                    <- Licencia MIT
├── 🔧 Makefile                   <- Comandos automatizados
├── 📖 README.md                  <- Documentación principal
├── 📊 data/
│   ├── external/                 <- Datos de fuentes externas
│   ├── interim/                  <- Datos intermedios transformados
│   ├── processed/                <- Datos finales para modelado
│   └── raw/                      <- Datos originales inmutables
│       └── final_submission.csv  <- Dataset principal (45K registros)
├── 📚 docs/                      <- Documentación del proyecto
│   ├── Instrucciones_Proyecto_2.pdf
│   └── conf.py
├── 🤖 models/                    <- Modelos entrenados y predicciones
├── 📓 notebooks/                 <- Notebooks de Jupyter
│   └── 01_exploratory_data_analysis.ipynb  <- EDA completo
├── 📋 references/                <- Diccionarios y materiales explicativos
├── 📈 reports/                   <- Análisis generados (HTML, PDF)
│   └── figures/                  <- Gráficos y visualizaciones
├── 📋 requirements.txt           <- Dependencias del proyecto
├── ⚙️ setup.py                   <- Configuración del paquete
├── 🔧 tox.ini                    <- Configuración de testing
├── 🧪 test_environment.py        <- Verificación del entorno
└── 🐍 src/                       <- Código fuente
    ├── __init__.py
    ├── data/                     <- Scripts de procesamiento de datos
    │   └── make_dataset.py
    ├── features/                 <- Scripts de ingeniería de características
    │   └── build_features.py
    ├── models/                   <- Scripts de entrenamiento y predicción
    │   ├── predict_model.py
    │   └── train_model.py
    └── visualization/            <- Scripts de visualización
        └── visualize.py
```

## 🛠️ Instalación y Configuración

### Requisitos Previos
- Python 3.10+
- Conda o Miniconda
- Jupyter Notebook/Lab

### Instalación

1. **Clonar el repositorio:**
```bash
git clone https://github.com/j0su3-2019/ProductDevelopment-Proyecto2.git
cd ProductDevelopment-Proyecto2
```

2. **Crear entorno virtual:**
```bash
conda create -n sales-forecasting python=3.10
conda activate sales-forecasting
```

3. **Instalar dependencias:**
```bash
pip install -r requirements.txt
```

4. **Configurar el proyecto:**
```bash
pip install -e .
```

5. **Verificar instalación:**
```bash
python test_environment.py
```

## 🚀 Uso del Proyecto

### 1. Análisis Exploratorio
```bash
jupyter lab notebooks/01_exploratory_data_analysis.ipynb
```

### 2. Procesamiento de Datos
```bash
python src/data/make_dataset.py
```

### 3. Ingeniería de Características
```bash
python src/features/build_features.py
```

### 4. Entrenamiento de Modelos
```bash
python src/models/train_model.py
```

### 5. Generar Predicciones
```bash
python src/models/predict_model.py
```

## 📊 Resultados Principales del EDA

### ✅ Hallazgos Clave
- **Dataset limpio:** Sin valores faltantes ni duplicados
- **Frecuencia consistente:** Datos diarios sin gaps temporales
- **Estacionalidad múltiple:** Patrones semanales y mensuales detectados
- **Autocorrelación significativa:** Dependencia temporal clara
- **Heterogeneidad:** Diferentes patrones por sucursal y producto

### 📈 Patrones Identificados
- **Tendencia temporal:** Evolución clara a lo largo del tiempo
- **Estacionalidad semanal:** Variaciones por día de la semana
- **Estacionalidad mensual:** Diferencias entre meses
- **Outliers controlados:** <5% del dataset total

### 🎯 Insights para Forecasting
- **Variables críticas:** Sucursal, producto, fecha
- **Lags significativos:** 1, 7, 30 días
- **Componentes estacionales:** Múltiples niveles detectados
- **Predictibilidad:** Alta autocorrelación permite pronósticos precisos

## 🧪 Testing y Validación

### Ejecutar Tests
```bash
# Test completo
tox

# Test específicos
python -m pytest tests/

# Verificar calidad de código
flake8 src/
```

### Métricas de Evaluación
- **MAPE:** Error porcentual medio absoluto
- **RMSE:** Error cuadrático medio
- **MAE:** Error absoluto medio
- **R²:** Coeficiente de determinación

## 📚 Recursos y Referencias

### Librerías Principales
- **Pandas:** Manipulación y análisis de datos
- **NumPy:** Computación numérica
- **Matplotlib/Seaborn:** Visualización estática
- **Plotly:** Visualización interactiva
- **Statsmodels:** Análisis estadístico y modelos temporales
- **Scikit-learn:** Machine learning
- **Prophet:** Forecasting automático

### Referencias Académicas
- Box, G. E. P. & Jenkins, G. M. (2015). *Time Series Analysis: Forecasting and Control*
- Hyndman, R. J. & Athanasopoulos, G. (2021). *Forecasting: Principles and Practice*
- Taylor, S. J. & Letham, B. (2018). *Forecasting at Scale*

## 👥 Contribuciones

### Autor Principal
- **Nombre:** [Tu Nombre]
- **Email:** [tu.email@example.com]
- **LinkedIn:** [tu-linkedin]
- **GitHub:** [@j0su3-2019](https://github.com/j0su3-2019)

### Agradecimientos
- **Universidad Galileo** - Postgrado en Análisis y Predicción de Datos
- **Profesores del curso** Product Development
- **Compañeros de clase** por retroalimentación y colaboración

## 📄 Licencia

Este proyecto está licenciado bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

### ¿Por qué MIT License?

La **Licencia MIT** es ideal para proyectos académicos porque:

- ✅ **Permisiva:** Permite uso comercial y modificación
- ✅ **Simple:** Fácil de entender y aplicar
- ✅ **Compatible:** Funciona bien con otras librerías open source
- ✅ **Académica:** Ampliamente aceptada en el ámbito universitario
- ✅ **Colaborativa:** Facilita colaboraciones futuras

## 🔄 Estado del Proyecto

- ✅ **Fase 1:** Análisis Exploratorio de Datos (Completado)
- 🔄 **Fase 2:** Ingeniería de Características (En Progreso)
- ⏳ **Fase 3:** Modelado Predictivo (Pendiente)
- ⏳ **Fase 4:** Evaluación y Validación (Pendiente)
- ⏳ **Fase 5:** Deployment y Presentación (Pendiente)

## 📞 Contacto

Para preguntas, sugerencias o colaboraciones:

- **Email:** [tu.email@galileo.edu]
- **GitHub Issues:** [Crear Issue](https://github.com/j0su3-2019/ProductDevelopment-Proyecto2/issues)
- **LinkedIn:** [Tu Perfil de LinkedIn]

---

*Desarrollado con ❤️ para el Postgrado en Análisis y Predicción de Datos - Universidad Galileo*

---

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
