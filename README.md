Sistema de IA para Sugerencia de Operaciones en el Oro (XAUUSD)

🟡 1. Resumen Ejecutivo

Este proyecto presenta un sistema de Inteligencia Artificial aplicado al trading del oro (XAUUSD), capaz de predecir y sugerir operaciones de Compra, Venta o Neutral con alta precisión.

La solución integra datos reales de MetaTrader 5, técnicas modernas de Machine Learning y una arquitectura de despliegue ligera, demostrando cómo la IA puede apoyar la toma de decisiones en mercados altamente volátiles.

El resultado final es un modelo capaz de clasificar operaciones con hasta 97% de exactitud, superando estrategias basadas únicamente en indicadores tradicionales.

🟡 2. Problema a Resolver

Los traders del oro suelen enfrentar desafíos como:

✔ Altísima volatilidad en sesiones clave

✔ Señales contradictorias entre indicadores

✔ Dificultad para mantener consistencia en decisiones

✔ Sesgos emocionales en la entrada al mercado

Este proyecto busca resolver estas limitaciones mediante un sistema objetivo, basado en datos y libre de sesgos humanos, que entregue una recomendación clara antes de operar.

🟡 3. Propuesta de Valor del Proyecto
🔹 Decisiones más informadas

El sistema analiza múltiples indicadores simultáneamente, algo difícil de lograr de forma manual.

🔹 Estabilidad y consistencia

El modelo aprende patrones que se repiten en diferentes condiciones del mercado.

🔹 Velocidad

Predicciones en milisegundos, aptas para trading intradía y automatización futura.

🔹 Aplicación inmediata

Puede integrarse a dashboards, bots o estrategias híbridas con intervención humana.

🟡 4. Metodología Utilizada
1. Captura de datos reales (MT5)

Un Expert Advisor personalizado registró:

Precios OHLC

Promedios móviles (SMA/EMA)

Indicadores técnicos clásicos (RSI, MACD, ADX, CCI, Williams %R, Bull/Bear Power, etc.)

Señales discretizadas de compra/venta

Datos horario por vela

2. Preparación y selección de variables

Tras un análisis de correlación y multicolinealidad, se seleccionaron las señales de indicadores y medias móviles, por su alta relación con la dirección del mercado.

3. Entrenamiento de modelos

Se entrenaron 10 algoritmos de clasificación, incluyendo:

Support Vector Classifier

HistGradientBoosting

XGBoost

Random Forest

Logistic Regression

4. Evaluación

Se utilizaron métricas comerciales y técnicas:

Accuracy

Precision

Recall

F1-macro

Matrices de confusión

🟡 5. Resultados Más Relevantes

Entre los modelos probados, se destaca:

⭐ SVC (Support Vector Classifier)

Accuracy: 0.97

F1-macro: 0.98

Desempeño por clase:

Compra: 97% F1

Neutral: 100% F1

Venta: 96% F1

Sin embargo, para producción se eligió XGBoost, gracias a su mayor estabilidad y menor tiempo de predicción.

🟡 6. Prototipo Web Funcional

El modelo entrenado fue desplegado en una aplicación web que permite:

Ingresar valores de indicadores

Ejecución del modelo en tiempo real

Obtención de la recomendación de la IA

🔗 Demo Web:
https://lfrm1971.github.io/Trading_Oro_web/

Este prototipo demuestra la aplicabilidad inmediata del sistema.

🟡 7. Impacto Comercial y de Negocio

Este proyecto tiene potencial para integrarse en:

✔ Plataformas de análisis financiero
✔ Sistemas automatizados de trading (EAs / bots)
✔ Herramientas educativas para nuevos traders
✔ Sistemas de alertas móviles o web
✔ Departamentos de gestión de riesgo

Además, abre la puerta a soluciones más avanzadas basadas en:

Algoritmos predictivos de series temporales

Estrategias algorítmicas completas

Backtesting automático

Integración con APIs de trading real

🟡 8. Limitaciones y Lineamientos Éticos

El sistema no reemplaza al trader humano, sino que sirve como apoyo.
Además:

No gestiona riesgo (StopLoss, posición, lotaje)

No incorpora noticias ni volatilidad

No debe usarse como herramienta de inversión autónoma

Se enfatiza el uso educativo y de investigación.

🟡 9. Conclusiones

Este proyecto demuestra que:

La IA puede analizar señales técnicas con mayor consistencia que métodos tradicionales.

Modelos como SVC y XGBoost ofrecen alto rendimiento para mercados volátiles.

El despliegue web valida la viabilidad real del sistema.

Es una base sólida para futuras investigaciones en trading algorítmico, IA financiera y sistemas expertos.

🟡 10. Autor

Leo Restrepo
Estudiante de Inteligencia Artificial
Trader de XAUUSD – MT5
