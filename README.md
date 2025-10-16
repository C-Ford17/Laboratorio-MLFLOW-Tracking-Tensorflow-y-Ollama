# Laboratorio MLOps – QSAR Biodegradation

Este proyecto contiene un laboratorio de **MLOps** usando MLflow para seguimiento de experimentos con **Scikit-learn** y **TensorFlow/Keras**.

## Contenido

- `MLFLOW_TRACKING_LABORATORY.ipynb` – Notebook principal con todos los pasos:
  1. Carga y preprocesamiento del dataset.
  2. Experimento de regresión logística con nested CV.
  3. Experimento de red neuronal con autologging.
  4. Interpretación de resultados usando Ollama.
- `requirements.txt` – Dependencias necesarias (sin versiones específicas).
- `informe.md` – Resumen del laboratorio, resultados y reflexiones.
- `captures/` – Carpeta sugerida para capturas de MLflow UI y artefactos.
- `artifacts/` – Carpeta con modelos guardados, gráficos y archivos de resumen.

## Experimentos

- **LogisticRegression_Manual:** Regresión logística con validación cruzada (folds anidados).  
- **RedNeuronal_TF:** Red neuronal entrenada con autologging de MLflow.

## Artefactos Generados

- **Regresión logística:** Matrices de confusión, gráficos de curva, descripción.txt  
- **Red neuronal:** Modelo `.h5`, TensorBoard logs, summary.txt

## Interpretación con Ollama
Se realizaron preguntas sobre métricas y desempeño de los modelos. Las respuestas se guardaron en `artifacts/interpretacion_ollama.txt`.

## Cómo Ejecutar
1. Crear y activar un entorno virtual.
2. Instalar dependencias:

```bash
pip install -r requirements.txt
