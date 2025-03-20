# Modelado ARIMA para el PIB de Colombia (1960 - 2023)

## Descripción del Proyecto
Este proyecto analiza la serie temporal del Producto Interno Bruto (PIB) de Colombia desde 1960 hasta 2023 utilizando modelos ARIMA. Se lleva a cabo una transformación logarítmica y diferenciación para lograr estacionariedad, y se comparan diferentes modelos para encontrar el que mejor se ajuste a la serie.

## Fuentes de Datos
Los datos han sido extraídos del Banco Mundial y están expresados en dólares constantes de 2015. Esto permite eliminar los efectos de la inflación y realizar comparaciones precisas a lo largo del tiempo.

## Metodología
1. **Carga y exploración de datos**: Lectura y preprocesamiento de la serie temporal.
2. **Análisis exploratorio**: Visualización de tendencias, identificación de posibles anomalías y evaluación de estacionariedad.
3. **Transformaciones y pruebas estadísticas**:
   - Aplicación de logaritmos y diferenciación.
   - Prueba de Dickey-Fuller para evaluar estacionariedad.
   - ACF y PACF para determinar orden.
4. **Modelado ARIMA**:
   - Comparación entre modelos ARIMA(1,1,1) y ARIMA óptimo identificado con `auto.arima()`.
   - Inclusión de un regresor externo para capturar el impacto de la pandemia.
5. **Evaluación del modelo**:
   - Comparación de criterios AIC y BIC.
   - Evaluación de métricas de error (MAE, SMAE, MAPE).
   - Análisis de residuos (normalidad, homocedasticidad y autocorrelación).
6. **Predicciones**: Proyección de la serie utilizando el modelo final seleccionado.

## Estructura del Repositorio
```
Modelado_ARIMA_PIB_Colombia/
├── README.md           # Documentación del proyecto
├── data/               # Datos originales y procesados
│   ├── API_NY.GDP.MKTP.KD_DS2_es_csv_v2_8100.csv
│   ├── Metadata_Country_API_NY.GDP.MKTP.KD_DS2_es_csv_v2_8100.csv
    ├── Metadata_Indicator_API_NY.GDP.MKTP.KD_DS2_es_csv_v2_8100.csv
├── notebooks/          # Análisis y código en R
│   ├── Analisis_PIB_Colombia.Rmd
├── informe_final
├── requirements.txt    # Librerías necesarias en R

```

## Requisitos
Para ejecutar el análisis en R, se requieren las siguientes librerías:
```r
install.packages(c("forecast", "TSA", "FinTS", "tseries", "dplyr", "lmtest", "MASS", "ggplot2", "readr"))
```

## Ejecución del Proyecto
1. Clonar el repositorio:
   ```bash
   git clone https://github.com/tu_usuario/Modelado_ARIMA_PIB_Colombia.git
   ```
2. Abrir el archivo `Analisis_PIB_Colombia.Rmd` en RStudio y ejecutar las celdas secuencialmente.
3. Generar predicciones y visualizar resultados.

## Conclusiones
- El modelo ARIMA(1,1,1) con un regresor externo capturó mejor la dinámica del PIB.
- Se evidenció una fuerte persistencia temporal y un impacto significativo de la pandemia en la serie.
- Los residuos cumplen con los supuestos estadísticos requeridos, validando la idoneidad del modelo.

## Autor
Autor: Juan Andrés Torres Contreras  
Fecha: 17 de marzo de 2025


