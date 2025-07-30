<p align="center">
  <img src="https://raw.githubusercontent.com/borre103/forecast-transformer/main/Marca-ITBA-Color-ALTA.png" alt="ITBA Logo" width="200" />
</p>


# **Forecast-Transformer**
Predicción de Ventas Mensuales Futuras por línea de negocio utilizando un modelo Transformer en PyTorch

## **Propuesta de valor**:
En un contexto en el que Coloplast no cuenta con la segmentación de importaciones por grado de producto, este proyecto redefine el enfoque hacia la predicción de ventas mensuales de las dos líneas de negocio disponibles —Ostomy Care (OC) e Intermittent Catheters (IC)— en lugar de productos “premium” solamente. Al aprovechar un modelo Transformer entrenado con los últimos 12 meses de datos y variables exógenas clave (importaciones y tiempos de Lead Days), lo que hice fue:

- **Visibilidad anticipada de la demanda**
    Planificación de importaciones con hasta 60 días de antelación, ajustada a las necesidades reales de OC e IC.
  
- **Reducción de quiebres de stock**
   Pronósticos con un MAPE de ~29 % en OC y ~16 % en IC, muy por debajo de métodos tradicionales.

- **Optimización de inventarios**  
   Equilibrio entre inversión en stock y cobertura de demanda, minimizando costos por exceso o faltantes.

- **Escalabilidad y adaptabilidad** 
   Misma arquitectura de Deep Learning para múltiples líneas de negocio.
  
Con esta solución, el área de Supply Chain y Planificación de Coloplast dispone de una herramienta predictiva confiable que traduce datos históricos de ventas e importaciones en decisiones operativas concretas, asegurando la disponibilidad de productos clave y apoyando el cumplimiento de los objetivos corporativos.

## **Dataset a Utilizar**
- **Periodicidad:** Mensual
- **Alcance:**
  - Ventas en cantidad de las líneas de negocio Ostomía (OC) e Incontinencia (IC).  
  - Desagregado por línea de negocio.
- **Período histórico:** Desde Octubre 2019 hasta Junio 2025 (69 meses). Los reportes de importación empiezan en esa época, por lo que no fue la máxima cantidad de datos que pude conseguir.

- **Datos históricos de importaciones**  
- **Periodicidad:** Mensual  
- **Alcance:**  
  - Importaciones en cantidad de productos para OC e IC.  
  - Desagregado por línea de negocio.  
- **Período histórico:** Desde Octubre 2019 hasta Junio 2025 (69 meses).
- **Uso:** Insumo complementario para evaluar la coherencia entre las predicciones de ventas y las necesidades de importación futuras.

- **Lead Days**  
- **Periodicidad:** Mensual  
- **Alcance:**  
- Tiempo total, en días, desde la orden de compra internacional hasta la disponibilidad en stock nacional.

## **Metodología de trabajo y modelos**
- **Preparación de datos:** Limpieza, conversión de tipos e imputación de Lead_days; creación de lags y promedios móviles.  
- **Escalado y dataset:** Normalización, ventana de 12 meses de entrada y 3 de pronóstico.
- **Modelado:** Entrenamiento de Transformer (y baselines  con PyTorch Lightning, usando early stopping y checkpoints.
- **Comparación:** Evaluación y comparación frente a modelos tradicionales Naive, SMA, ARIMA, y LSTM
- **Evaluación y pronóstico:** Cálculo de MAE, RMSE, MAPE para seleccionar el mejor; predicción desescalada para julio–septiembre 2025.  

