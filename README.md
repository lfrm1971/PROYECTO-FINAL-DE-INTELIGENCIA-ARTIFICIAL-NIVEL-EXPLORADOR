Predicción de Operaciones en XAUUSD usando Machine Learning

(Compra / Venta / Neutral)

🟡 1. Introducción

Este proyecto tiene como objetivo desarrollar un sistema de Machine Learning capaz de sugerir operaciones de compra, venta o neutral en el oro (XAUUSD), basándose en un conjunto de indicadores técnicos y señales generadas en MetaTrader 5 (MT5).

Se entrenaron y compararon 10 modelos de clasificación utilizando datos reales obtenidos mediante un Expert Advisor (EA).
El propósito es demostrar cómo los modelos de IA pueden complementar el análisis técnico tradicional, proporcionando señales objetivas y consistentes.

🟡 2. ¿Por qué el Oro (XAUUSD)?

El oro es uno de los activos más negociados del mundo debido a:

📌 Alta liquidez y volatilidad

📌 Activo refugio frente a crisis económicas

📌 Protección ante inflación

📌 Amplio uso en estrategias de trading intradía y swing

Sin embargo, es importante recordar que operar oro implica riesgos debido a su comportamiento volátil y posible impacto de noticias macroeconómicas.

🟡 3. Obtención de los Datos

Los datos fueron recolectados desde MetaTrader 5 mediante un Expert Advisor personalizado, el cual registró:

Velas (open, close, high, low)

Precios de entrada

Indicadores técnicos

Señales generadas por cada indicador

Promedios móviles (SMA/EMA)

Datos agrupados por hora

📊 Tamaño del dataset

27.083 registros

Periodo de estudio según histórico de MT5

🟡 4. Indicadores e Información Incluida

Se calcularon los siguientes indicadores técnicos:

🔹 Promedios Móviles

SMA y EMA de 5, 10, 20, 50, 100 y 200 periodos

Señales binarias:

1 = compra

-1 = venta

0 = neutral

🔹 Indicadores Técnicos

RSI

MACD

ADX

Williams %R

CCI

High/Lows

Bull Power / Bear Power

Estocástico

✔ Cada indicador generó señales discretizadas que se usan como features del modelo.

🟡 5. Estructura del Dataset

El dataset incluye más de 50 columnas, entre ellas:

Valores OHLC

Señales de indicadores

Señales de promedios móviles

Diferencias entre precios y medias

Indicadores técnicos continuos

Target: Acción (Compra / Venta / Neutral)

La estructura permite alimentar modelos ML con información rica en tendencias y fuerza del mercado.

🟡 6. Análisis Exploratorio y Selección de Variables
🔍 Matriz de correlación

La matriz muestra que las señales de indicadores y promedios móviles tienen una correlación moderada con la variable objetivo (aprox. 0.30 – 0.56).

🟦 ¿Por qué se eligieron estas variables?

✔ Ya están discretizadas → menos ruido
✔ Baja multicolinealidad
✔ Capturan dirección del mercado
✔ A los modelos ML les gustan las variables categóricas con señal clara

Estas características permiten entrenar modelos más estables y con mejor capacidad predictiva.

🟡 7. Modelos de Machine Learning Aplicados

Se entrenaron y evaluaron 10 modelos de clasificación:

SVC

HistGradientBoosting

GradientBoosting

Logistic Regression

Stochastic Gradient Descent

XGBoost

Decision Tree

Random Forest

ExtraTrees

GaussianNB

Todos obtuvieron métricas altas, destacándose:

⭐ Mejor modelo según F1-Macro: SVC

Accuracy: 0.97

F1 macro: 0.98

📘 Resultados por clase (SVC)

Compra → F1: 0.97

Neutral → F1: 1.00

Venta → F1: 0.96

🟡 8. Comparación General de Modelos
Modelo	Accuracy	F1-macro	Tiempo Entrenamiento (s)
SVC	0.9688	0.9777	12.02
HistGB	0.9677	0.9768	0.73
GradientBoosting	0.9677	0.9768	3.46
LogisticRegression	0.9656	0.9753	0.36
XGBoost	0.9654	0.9752	0.96
…	…	…	…
🟡 9. Matrices de Confusión

Se generaron matrices de confusión para los 10 modelos, permitiendo visualizar:

Aciertos en Compra

Aciertos en Venta

Errores clasificando Neutral

Falsos positivos/negativos por modelo

Estas gráficas reforzaron la elección final del modelo de despliegue.

🟡 10. Modelo Seleccionado para Producción (XGBoost)

Aunque SVC fue el modelo de mayor rendimiento, para el despliegue se eligió:

✔ XGBoost

Motivos:

Excelente equilibrio precisión/recall

Soporta predicciones rápidas

Reaccionó mejor al dataset completo

Matriz de confusión más estable para casos minoritarios

El modelo se exportó y se integró en una aplicación web.

🟡 11. Despliegue Web

El modelo fue publicado en:

👉 https://lfrm1971.github.io/Trading_Oro_web/

Funciones del sitio:

Cargar datos o parámetros

Visualizar señales generadas por el modelo

Interfaz ligera y accesible para usuarios sin conocimiento técnico

🟡 12. Conclusiones del Proyecto

El uso de datos provenientes de MT5 permitió entrenar un modelo robusto y cercano al trading real.

Los indicadores discretizados (señales) mejoraron la estabilidad del modelo.

El SVC obtuvo el mejor rendimiento global (F1-macro ≈ 0.98).

Para despliegue, el XGBoost mostró un balance óptimo entre rendimiento y velocidad.

El sistema es capaz de sugerir de manera confiable operaciones Compra / Venta / Neutral.

🟡 13. Límites y Próximos Pasos
⚠ Limitaciones actuales

No se aplicó gestión de riesgo (StopLoss dinámico, ATR, R-Multiple).

El modelo se basa solo en indicadores técnicos.

No incluye noticias, volatilidad ni patrones de precio.

Dataset basado en un solo símbolo (XAUUSD) y un solo periodo.

🚀 Futuras mejoras

Incluir backtesting completo con capital inicial.
