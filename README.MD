# Pronóstico de Riesgo de Liquidez — Tarjeta Plus

Prueba técnica para el proceso de selección de pasantía universitaria en la
Gerencia de Metodologías de Riesgo de Mercado de Capitales — Bancolombia, 2026.

## Objetivo

Construir un modelo de pronóstico del porcentaje mensual de utilización del cupo
de la Tarjeta Plus, con horizonte de tres meses. Se comparan múltiples arquitecturas
de series de tiempo y se selecciona la de mejor desempeño bajo criterios cuantitativos,
con validación mediante backtesting orientado a entorno productivo.

## Contexto del problema

Los compromisos de crédito representan obligaciones futuras de desembolso preaprobadas
a clientes. Anticipar su comportamiento es una necesidad operativa concreta para la
gestión del riesgo de liquidez — el banco debe garantizar disponibilidad de fondos
para cubrir los desembolsos que los clientes decidan realizar sobre sus cupos aprobados.

## Metodología

1. **Exploración de datos** — análisis de la serie, identificación de outliers y
   verificación de calidad de datos.
2. **Análisis de estacionariedad** — prueba ADF para verificar formalmente la presencia
   de raíz unitaria.
3. **Torneo de modelos** — entrenamiento y comparación de tres arquitecturas:
   ARIMA, SARIMA y Holt-Winters, evaluadas con MAE, RMSE y MAPE.
4. **Selección del modelo** — ARIMA(1,1,1) seleccionado por mejor desempeño en las
   tres métricas y balance entre precisión y parsimonia.
5. **Pronóstico a 3 meses** — modelo reentrenado con la totalidad de los datos.
6. **Backtesting walk-forward** — validación sobre 8 ventanas históricas para
   evaluar estabilidad temporal del modelo.

## Resultados principales

| Modelo       | RMSE (%) | MAE (%) | MAPE (%) |
|--------------|----------|---------|----------|
| ARIMA        | 0.26     | 0.25    | 1.56     |
| SARIMA       | 0.30     | 0.29    | 1.81     |
| Holt-Winters | 0.63     | 0.58    | 3.60     |

El modelo ARIMA(1,1,1) proyecta una utilización del cupo de aproximadamente
16.4% para junio, julio y agosto de 2025.

El backtesting walk-forward sobre 8 ventanas históricas arrojó un MAPE promedio
de 11.96%, confirmando que el desempeño del modelo depende del contexto temporal
y justificando monitoreo periódico en producción.

## Estructura del repositorio
```
pronostico-riesgo-liquidez/
├── datos/
│   └── TarjetaPlus.xlsx
├── notebooks/
│   └── pronostico_riesgo_liquidez.ipynb
├── entregables/
│   └── Prueba_Teorica.pdf
├── enunciado/
│   └── Prueba_conocimientos_pasantes_2026.pdf
└── README.md
```

## Requisitos
```
pandas
numpy
matplotlib
statsmodels
scikit-learn
openpyxl
```

## Reproducibilidad

Clonar el repositorio, instalar dependencias y ejecutar el notebook en orden
secuencial. La ruta del archivo de datos debe actualizarse en la celda de carga
según el entorno local.

## Autor

Juan Ángel Gámez  
Ingeniero Físico  
Especialización en Data Science — Alura Latam