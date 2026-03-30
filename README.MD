# Pronóstico de Riesgo de Liquidez

Proyecto desarrollado como prueba técnica para modelado de series de tiempo aplicado al análisis de utilización del cupo de crédito.

## Objetivo

Construir un modelo de pronóstico sobre la serie mensual de porcentaje de utilización del cupo, evaluando distintas arquitecturas de series de tiempo y seleccionando la de mejor desempeño bajo criterios cuantitativos.

## Metodología

Se implementaron y compararon los siguientes modelos:

- ARIMA
- SARIMA
- Holt-Winters

La selección se realizó con base en métricas de error:

- MAE
- RMSE
- MAPE

Adicionalmente, se aplicó validación temporal mediante backtesting tipo walk-forward para evaluar estabilidad fuera de muestra.

## Estructura del repositorio

- `enunciado/`: documento original de la prueba técnica  
- `datos/`: base de datos utilizada  
- `notebooks/`: desarrollo completo del modelado  
- `entregables/`: informe técnico y prueba teórica  

## Resultado principal

El modelo ARIMA(1,1,1) presentó el mejor desempeño predictivo y fue seleccionado para el pronóstico final.

## Autor

Juan Ángel Gamez  
Ingeniero Físico  
Especialización en Data Science — Alura Latam
=======
# Pronóstico de Riesgo de Liquidez

Proyecto desarrollado como prueba técnica para modelado de series de tiempo aplicado al análisis de utilización del cupo de crédito.

## Objetivo

Construir un modelo de pronóstico sobre la serie mensual de porcentaje de utilización del cupo, evaluando distintas arquitecturas de series de tiempo y seleccionando la de mejor desempeño bajo criterios cuantitativos.

## Metodología

Se implementaron y compararon los siguientes modelos:

- ARIMA
- SARIMA
- Holt-Winters

La selección se realizó con base en métricas de error:

- MAE
- RMSE
- MAPE

Adicionalmente, se aplicó validación temporal mediante backtesting tipo walk-forward para evaluar estabilidad fuera de muestra.

## Estructura del repositorio

- `enunciado/`: documento original de la prueba técnica  
- `datos/`: base de datos utilizada  
- `notebooks/`: desarrollo completo del modelado  
- `entregables/`: Prueba teórica  

## Resultado principal

El modelo ARIMA(1,1,1) presentó el mejor desempeño predictivo y fue seleccionado para el pronóstico final sin variables externas consideradas.

## Autor

Juan Ángel Gamez  
Ingeniero Físico  
Especialización en Data Science — Alura Latam
>>>>>>> a5e13310224d309d057ce693757dac8c9754c5b6
