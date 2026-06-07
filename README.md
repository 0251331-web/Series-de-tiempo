# Series_de_tiempo

## I. Propósito

Este repositorio documenta el trabajo desarrollado en el curso de **Series de Tiempo Aplicadas a Finanzas**. El objetivo central fue comprender cómo modelar, interpretar y pronosticar variables económicas y financieras cuya evolución depende explícitamente del tiempo.

A diferencia de los modelos tradicionales de corte transversal, donde el orden de las observaciones es irrelevante, en una serie de tiempo el pasado contiene información potencialmente útil para explicar el presente y anticipar el futuro. Esta característica convierte al tiempo en una variable fundamental dentro del análisis.

Las aplicaciones estudiadas incluyen precios de activos financieros, rendimientos bursátiles, inflación, exportaciones, ventas comerciales, producción industrial, volatilidad y riesgo de mercado.

---

# II. Teorema Fundamental de las Series de Tiempo: Toda serie debe entenderse antes de modelarse

El primer principio del análisis temporal establece que ningún modelo debe estimarse antes de comprender la estructura de los datos.

Toda serie puede contener una combinación de:

* Tendencia
* Estacionalidad
* Ciclos
* Ruido
* Cambios estructurales
* Valores atípicos
* Dependencia temporal
* Volatilidad variable

La inspección gráfica constituye el primer diagnóstico. En la práctica profesional, esta etapa funciona como un *screening* preliminar que permite identificar comportamientos que posteriormente deberán ser capturados por el modelo.

---

# III. Teorema de la Estacionariedad

La estacionariedad constituye la hipótesis fundamental detrás de la mayoría de los modelos clásicos de series de tiempo.

Una serie estacionaria mantiene propiedades estadísticas constantes a través del tiempo.

Formalmente:

E(y_t)=μ

Var(y_t)=σ²

Cov(y_t,y_(t-k))=γ_k

La importancia de esta propiedad radica en que permite extrapolar patrones observados en el pasado hacia el futuro.

Cuando una serie no es estacionaria, los parámetros estimados pueden resultar inconsistentes y producir relaciones espurias.

---

# IV. Teorema de la Raíz Unitaria

Una raíz unitaria implica que los shocks tienen efectos permanentes sobre la trayectoria de la serie.

Si una perturbación modifica el nivel de la serie y dicho efecto no desaparece con el tiempo, la serie posee raíz unitaria.

La prueba principal estudiada fue la prueba Augmented Dickey-Fuller (ADF).

Hipótesis:

H₀: La serie posee raíz unitaria.

H₁: La serie es estacionaria.

La decisión se basa en el valor p.

La prueba ADF constituye uno de los pilares de la metodología Box-Jenkins.

---

# V. Teorema de las Transformaciones

No toda serie es modelable en su estado original.

Frecuentemente es necesario aplicar transformaciones que permitan estabilizar la estructura estadística.

## Logaritmos

Los logaritmos convierten cambios absolutos en cambios relativos.

ln(y_t)

Son especialmente útiles cuando la varianza crece con el nivel de la serie.

## Diferencias

La diferenciación elimina tendencia estocástica.

Δy_t = y_t - y_(t-1)

## Diferencias Estacionales

Δ_s y_t = y_t - y_(t-s)

Permiten eliminar patrones periódicos recurrentes.

---

# VI. Teorema de la Dependencia Temporal

La dependencia temporal se estudia mediante dos herramientas fundamentales:

## ACF

Autocorrelation Function.

Mide la relación entre una observación y sus rezagos.

## PACF

Partial Autocorrelation Function.

Mide la relación directa entre una observación y un rezago específico, eliminando el efecto de los rezagos intermedios.

Estas funciones constituyen la principal herramienta de identificación de modelos.

---

# VII. Teorema Autorregresivo

Los modelos AR suponen que el presente depende de observaciones pasadas.

AR(p):

y_t = c + φ₁y_(t-1) + ... + φ_py_(t-p) + ε_t

La memoria del proceso queda resumida en el parámetro p.

---

# VIII. Teorema de Media Móvil

Los modelos MA explican la serie mediante errores pasados.

MA(q):

y_t = μ + ε_t + θ₁ε_(t-1) + ... + θ_qε_(t-q)

Aquí la memoria no proviene de la serie misma, sino de los shocks históricos.

---

# IX. Teorema ARMA

ARMA combina estructura autorregresiva y estructura de errores.

ARMA(p,q)

Permite modelar procesos estacionarios con memoria y persistencia.

---

# X. Teorema de Integración

Cuando la serie no es estacionaria se introduce el concepto de integración.

ARIMA(p,d,q)

d representa el número de diferencias requeridas para alcanzar estacionariedad.

La integración conecta la teoría de series estacionarias con variables económicas reales que suelen presentar tendencia.

---

# XI. Teorema de la Estacionalidad

Las series económicas frecuentemente contienen patrones recurrentes.

Para capturarlos se utiliza:

SARIMA(p,d,q)(P,D,Q)s

donde s representa el periodo estacional.

Este modelo incorpora simultáneamente dinámica de corto plazo y dinámica estacional.

---

# XII. Teorema de las Variables Exógenas

La historia no siempre contiene toda la información relevante.

SARIMAX permite incorporar variables explicativas externas.

Ejemplos:

* Promociones
* Días festivos
* Tasas de interés
* Tipo de cambio
* Producción industrial

El modelo deja de ser puramente autorreferencial y se convierte en una herramienta explicativa.

---

# XIII. Teorema Box-Jenkins

La metodología Box-Jenkins constituye el framework clásico de construcción de modelos.

Etapas:

I. Identificación

II. Estimación

III. Diagnóstico

IV. Pronóstico

Su importancia radica en que transforma la modelación en un proceso sistemático.

---

# XIV. Teorema de la Parsimonia

Un modelo más complejo no necesariamente es mejor.

La selección se apoya en:

* AIC
* BIC
* Log-Likelihood

El objetivo es encontrar el equilibrio óptimo entre ajuste y complejidad.

---

# XV. Teorema del Residuo Blanco

Un modelo adecuado debe dejar residuos sin estructura.

Los residuos deben comportarse como ruido blanco.

Para verificarlo se utilizan:

* ACF residual
* PACF residual
* Ljung-Box
* Histogramas
* QQ-Plots

---

# XVI. Teorema del Pronóstico

Pronosticar no significa adivinar.

Un pronóstico representa una distribución condicional basada en información histórica.

Todo forecast debe acompañarse de:

* Valor esperado
* Intervalos de confianza
* Horizonte temporal
* Supuestos

---

# XVII. Teorema de los Rendimientos Financieros

Los precios suelen ser no estacionarios.

Por ello se trabaja con rendimientos.

Rendimiento simple.

Log-rendimiento.

Los rendimientos presentan propiedades estadísticas más adecuadas para modelación.

---

# XVIII. Teorema de la Heterocedasticidad Condicional

La volatilidad no permanece constante.

Los periodos de alta volatilidad suelen ser seguidos por periodos de alta volatilidad.

Este fenómeno se conoce como volatility clustering.

---

# XIX. Teorema ARCH

ARCH modela la varianza condicional mediante errores pasados.

La innovación principal de Engle consistió en permitir que la volatilidad evolucionara dinámicamente.

---

# XX. Teorema GARCH

Bollerslev extendió ARCH incorporando rezagos de la propia varianza.

GARCH(1,1) se convirtió en el estándar de la industria por su capacidad para capturar persistencia con pocos parámetros.

---

# XXI. Teorema de la Asimetría

Los mercados reaccionan de manera distinta a buenas y malas noticias.

GJR-GARCH y EGARCH permiten modelar este comportamiento.

Las noticias negativas suelen generar incrementos mayores en volatilidad.

---

# XXII. Teorema del Riesgo y Rendimiento

GARCH-M incorpora la volatilidad dentro de la ecuación de media.

Permite estudiar si un mayor riesgo esperado exige una compensación adicional en forma de rendimiento.

---

# XXIII. Teorema del Value at Risk

El VaR representa la pérdida máxima esperada bajo un nivel de confianza determinado.

Con modelos GARCH se obtiene un VaR dinámico que evoluciona conforme cambia la volatilidad.

---

# XXIV. Teorema del Backtesting

Todo modelo de riesgo debe ser validado.

El backtesting compara pérdidas observadas contra pérdidas esperadas.

La validez de un sistema de gestión de riesgo depende de esta etapa.

---

# XXV. Aplicaciones Desarrolladas

Durante el curso se trabajó con:

* Series simuladas
* Series financieras
* Ventas
* Exportaciones
* Acciones
* Índices bursátiles
* Pronósticos
* Volatilidad
* Riesgo de mercado

Los ejercicios se implementaron en Python utilizando Pandas, NumPy, Statsmodels, Arch y yfinance.

---

# XXVI. Herramientas Utilizadas

* Python
* Pandas
* NumPy
* Statsmodels
* Matplotlib
* Arch Package
* yfinance
* Google Colab
* LaTeX
* GitHub

---

# XXVII. Bibliografía Fundamental

* Box & Jenkins
* Hamilton
* Hyndman & Athanasopoulos
* Enders
* Tsay
* Engle
* Bollerslev

---

# XXVIII. Autor

**Sofia Escamilla**

Licenciatura en Finanzas

Universidad Panamericana

Curso: Series de Tiempo Aplicadas a Finanzas

