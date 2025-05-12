
# README - Proyecto de Red Neuronal LSTM para Análisis y Predicción Financiera del S&P 500

## Descripción General
Este proyecto implementa una serie de modelos de redes neuronales recurrentes (LSTM) para predecir y analizar el comportamiento del índice S&P 500, basándose en datos históricos desde 1990 hasta 2024. Está diseñado como una herramienta de investigación y formación avanzada en econofísica y análisis cuantitativo de series temporales financieras.

Se emplean múltiples arquitecturas LSTM para distintas tareas:
- Predicción de un día y varios días en el futuro del S&P 500.
- Cálculo y predicción del índice de Hurst, entropía de Shannon, fractalidad y volatilidad.

## Tecnologías Utilizadas
- **Lenguaje**: Python 3
- **Bibliotecas clave**:
  - `TensorFlow` y `Keras` para modelos LSTM
  - `yfinance` para la descarga de datos bursátiles
  - `NumPy`, `Pandas` y `Matplotlib` para manipulación de datos y visualización
  - `scikit-learn` para escalamiento

## Estructura del Proyecto
1. **Predicción directa del precio del S&P 500:**
   - Modelos con una, dos y tres capas LSTM
   - Entrenamiento en GPU
   - Comparación entre arquitecturas en cuanto a tendencia, detalle y sobreajuste

2. **Predicción multi-horizonte (5 días):**
   - Modelos con salida multivariable para predecir varios días futuros
   - Análisis de la dificultad predictiva por horizonte temporal

3. **Análisis de complejidad del mercado:**
   - Cálculo y predicción del exponente de Hurst (método R/S)
   - Estimación y modelado de la entropía de Shannon
   - Dimensión fractal con método de Higuchi
   - Cálculo de la volatilidad histórica con predicción LSTM

4. **Análisis de regímenes de mercado:**
   - Clasificación de periodos de "Caos" y "Calma" usando umbrales de entropía
   - Visualización codificada por color de los regímenes sobre la serie temporal

## Instrucciones para Ejecutar
1. Instala los requisitos:
```bash
pip install yfinance tensorflow scikit-learn matplotlib
```

2. Ejecuta los scripts en orden o individualmente desde un entorno como Google Colab o Jupyter.

3. Verifica que tu sistema tenga acceso a GPU (opcional pero recomendado).

## Recomendaciones del Analista
- **Para traders intradía**: Las redes LSTM son más útiles si se entrenan con datos de alta frecuencia y se enfocan en ventanas cortas (1-5 días).
- **Para análisis macroeconómico**: Las métricas de econofísica (Hurst, entropía, fractalidad) pueden revelar regímenes de mercado no evidentes con métodos tradicionales.
- **Evitar sobreajuste**: Al usar muchas capas, Dropout es indispensable. Se recomienda usar validación cruzada y early stopping.

## Observaciones Teóricas
- **Eficiencia del mercado**: Una predicción exacta en series financieras se ve limitada por el principio de profecía autocumplida. Esto se aborda parcialmente con el análisis del exponente de Hurst.
- **Predicción vs. Interpretabilidad**: Añadir complejidad al modelo mejora la capacidad de ajuste, pero dificulta la interpretación. Para aplicaciones prácticas se debe balancear.

## Resultados Esperados
- Curvas de predicción vs. valores reales para distintos modelos.
- Curvas temporales de Hurst, entropía y fractalidad.
- Regímenes de mercado identificados mediante color.

## Autor
**Robinson MAnuel Avila Hernandez**  

