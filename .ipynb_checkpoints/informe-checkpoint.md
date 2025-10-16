# Informe del Taller MLOps – QSAR Biodegradation

## 1. Descripción del Dataset
El dataset **QSAR Biodegradation** contiene características químicas de distintas moléculas y una variable objetivo binaria (`class`) que indica biodegradabilidad.  
- Número de filas: 1050  
- Número de columnas: 42 (41 features + 1 target)  
- Objetivo: clasificación binaria (1 = biodegradable, 2 = no biodegradable)

## 2. Resultados de los Modelos

### Regresión Logística
- Métrica principal: Accuracy promedio ~0.864
- Folds:
  - Fold 1: 0.8759
  - Fold 2: 0.8577
  - Fold 3: 0.8683
- Artefactos: matriz de confusión, gráficos de curva por fold, descripción.txt

### Red Neuronal (TensorFlow/Keras)
- Accuracy: 0.912
- Precision: 0.923
- Recall: 0.946
- Artefactos: modelo `.h5`, TensorBoard logs, summary.txt

## 3. Interpretación con Ollama
**Pregunta:** ¿Qué significa obtener un F1-score de 0.88?  
**Respuesta:** Un F1-score combina precisión y recall como media armónica. Valor de 0.88 indica buen equilibrio entre detección de positivos y exactitud de predicciones.

**Pregunta:** ¿Por qué una red neuronal podría tener mejor recall que una regresión logística?  
**Respuesta:** Las redes neuronales capturan relaciones no lineales y patrones complejos, mejorando la detección de positivos, mientras que la regresión logística tiene capacidad más limitada.

**Pregunta:** ¿Qué podría mejorar el rendimiento de los modelos en este dataset?  
**Respuesta:** Mejorar preprocesamiento, ajustar hiperparámetros, aumentar dataset, regularización, early stopping, ensemble methods, ingeniería de features.

## 4. Observaciones Finales
- La red neuronal superó a la regresión logística en todas las métricas principales.
- Los folds de la regresión logística permiten evaluar estabilidad del modelo.
- Los artefactos generados permiten reproducibilidad y análisis posterior.
