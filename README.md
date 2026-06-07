# Series_de_tiempo

# 📈 Series de Tiempo – Fundamentos y Aplicaciones

Repositorio académico para el estudio teórico y aplicado de **Series de Tiempo**, con énfasis en modelos econométricos clásicos y financieros utilizados para análisis, modelación y pronóstico de variables económicas y financieras.

El objetivo es comprender los procesos estocásticos que generan los datos observados, identificar patrones temporales, construir modelos estadísticos adecuados y generar pronósticos robustos para la toma de decisiones.

---

## 📚 Contenido del curso

### 1️⃣ Introducción a Series de Tiempo

#### 🔹 Conceptos fundamentales

- ¿Qué es una serie de tiempo?
- Dependencia temporal
- Componentes de una serie
- Predicción y pronóstico

#### 🔹 Componentes principales

- Tendencia
- Estacionalidad
- Ciclo
- Componente irregular
- Ruido aleatorio

---

### 📊 Visualización y Exploración de Datos

#### Análisis Exploratorio

- Gráficas temporales
- Estadísticos descriptivos
- Identificación de patrones
- Detección de valores atípicos

#### Transformaciones Comunes

- Logaritmos
- Diferenciación
- Tasas de crecimiento
- Rendimientos

---

### 2️⃣ Estacionariedad

#### 🔹 Conceptos

- Estacionariedad estricta
- Estacionariedad débil
- Media constante
- Varianza constante
- Covarianza constante

#### 🔹 Pruebas de Raíz Unitaria

- Dickey-Fuller (DF)
- Augmented Dickey-Fuller (ADF)
- Phillips-Perron (PP)

#### 🔹 Transformaciones para Estacionariedad

- Diferencias regulares
- Diferencias estacionales
- Eliminación de tendencia

---

### 3️⃣ Modelos ARIMA

#### 🔹 Modelo Autorregresivo (AR)

AR(p)

- Dependencia de rezagos
- Condiciones de estacionariedad
- Interpretación de parámetros

#### 🔹 Modelo de Medias Móviles (MA)

MA(q)

- Choques aleatorios
- Efectos transitorios
- Invertibilidad

#### 🔹 Modelo ARMA

ARMA(p,q)

- Combinación AR y MA
- Identificación de parámetros
- Estimación

#### 🔹 Modelo ARIMA

ARIMA(p,d,q)

- Integración mediante diferenciación
- Procesos no estacionarios
- Pronósticos

---

### 📈 Identificación del Modelo

#### Función de Autocorrelación (ACF)

- Identificación de componentes MA
- Persistencia temporal
- Correlogramas

#### Función de Autocorrelación Parcial (PACF)

- Identificación de componentes AR
- Rezagos significativos

---

### 4️⃣ Modelos SARIMA

#### 🔹 Componentes Estacionales

SARIMA(p,d,q)(P,D,Q)s

- Autorregresión estacional
- Diferenciación estacional
- Media móvil estacional
- Periodicidad

#### Aplicaciones

- Series mensuales
- Series trimestrales
- Variables económicas con estacionalidad

---

### 📊 Selección de Modelos

#### Principio de Parsimonia

- Modelos simples
- Balance entre ajuste y complejidad

#### Criterios de Información

##### AIC

Akaike Information Criterion

- Comparación de modelos
- Penalización por complejidad

##### BIC

Bayesian Information Criterion

- Selección conservadora
- Penalización más fuerte

#### Log-Verosimilitud

- Máxima verosimilitud
- Comparación estadística

---

### 5️⃣ Diagnóstico de Modelos

#### Análisis de Residuos

- Residuos estandarizados
- Ruido blanco
- Independencia temporal

#### Prueba Ljung-Box

- Autocorrelación residual
- Validación del modelo

#### Normalidad

- Jarque-Bera
- Curtosis
- Asimetría

---

### 6️⃣ Modelos con Variables Exógenas

#### 🔹 ARIMAX

ARIMA con regresores externos

- Variables explicativas
- Interpretación económica
- Pronósticos condicionados

#### 🔹 SARIMAX

SARIMA con variables exógenas

- Componentes estacionales
- Variables macroeconómicas
- Pronósticos multivariados

---

### 📈 Caso de Estudio: Exportaciones de México

#### Variables utilizadas

- Exportaciones mexicanas
- Índice de Producción Industrial de EE.UU.
- Componentes estacionales mensuales

#### Objetivos

- Modelar exportaciones
- Evaluar impacto de variables externas
- Generar pronósticos

---

### 7️⃣ Series de Tiempo Financieras

#### Características de los Rendimientos

- No normalidad
- Asimetría
- Leptocurtosis
- Clustering de volatilidad

#### Propiedades Empíricas

- Volatilidad variable
- Dependencia temporal en la varianza
- Colas pesadas

---

### 8️⃣ Modelos ARCH y GARCH

#### 🔹 ARCH

Autoregressive Conditional Heteroskedasticity

- Heterocedasticidad condicional
- Volatilidad dependiente del pasado

#### 🔹 GARCH

Generalized ARCH

GARCH(p,q)

- Persistencia de volatilidad
- Volatilidad de largo plazo
- Pronóstico de riesgo

#### Aplicaciones

- Mercados financieros
- Gestión de riesgos
- Pronóstico de volatilidad

---

### 9️⃣ Modelos Asimétricos de Volatilidad

#### 🔹 GJR-GARCH

- Efecto apalancamiento
- Impacto asimétrico de noticias

#### 🔹 EGARCH

- Logaritmo de la varianza
- Asimetría
- Positividad garantizada

#### 🔹 GARCH-M

- Prima de riesgo
- Relación riesgo-retorno

---

### 📊 Medición de Riesgo

#### Value at Risk (VaR)

- VaR paramétrico
- VaR dinámico
- VaR basado en volatilidad condicional

#### Aplicaciones

- Gestión de portafolios
- Riesgo de mercado
- Control de pérdidas

---

## 🧠 Objetivos del repositorio

- Comprender la teoría de series de tiempo.
- Identificar procesos estacionarios y no estacionarios.
- Aplicar modelos ARIMA y SARIMA.
- Incorporar variables exógenas mediante SARIMAX.
- Analizar volatilidad financiera.
- Implementar modelos GARCH y sus extensiones.
- Evaluar modelos mediante criterios estadísticos.
- Generar pronósticos económicos y financieros.
- Aplicar herramientas cuantitativas a datos reales.

---

## 🛠️ Tecnologías y Herramientas

- Python
- NumPy
- Pandas
- Statsmodels
- SciPy
- Matplotlib
- Seaborn
- ARCH Package
- Jupyter Notebook
- Google Colab

---

## 📂 Estructura sugerida del repositorio

```text
series_de_tiempo/
│
├── datos/
│   └── store_sales.csv
│
├── notebooks/
│   ├── exploracion_datos.ipynb
│   ├── arima_sarima.ipynb
│   ├── sarimax.ipynb
│   └── garch.ipynb
│
├── reportes/
│   ├── Reporte_SARIMA.pdf
│   ├── Informe_ARIMA_SARIMA_AAPL.pdf
│   └── Proyecto_Final.pdf
│
│
├── documentos/
│   ├── Proyecto_ST
│
└── README.md
```

---

## 📚 Bibliografía

- Box, G. E. P., Jenkins, G. M., Reinsel, G. C., & Ljung, G. M. *Time Series Analysis: Forecasting and Control.*
- Hamilton, J. D. *Time Series Analysis.*
- Hyndman, R. J., & Athanasopoulos, G. *Forecasting: Principles and Practice.*
- Tsay, R. S. *Analysis of Financial Time Series.*
- Enders, W. *Applied Econometric Time Series.*

---

## 👩‍🎓 Autor

**Sofía Escamilla**  
Licenciatura en Finanzas  

Curso: Series de Tiempo Aplicadas a Finanzas
