# forecast-transformer
Predicción de Ventas Mensuales Futuras por línea de negocio utilizando un modelo Transformer en PyTorch

Propuesta de valor:
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

  
