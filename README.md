# Forecasting usando dataset TICKIT

El forecast que se utilizo fue forecasting **Autoregresivo Series Temporales** con Python y Scikit-learn 
El codigo se divide en las siguientes partes:
- Instalación de paqueterias
- Librerias
- Adquisición y preparación de datos
- ForecasterAutoreg
- Predicciones
- Error de las predicciones en el conjunto de test
- Ajuste de hiperparámetros (tuning)
- Modelo Final

El conjunto de datos se modifico a una frecuencia de Semanas (W)

Notas:
- Se propone seguir ajustando los valores en el entrenamiento 
- Modificar la frecuencia de los datos a días 


# ¿Cómo Desplegar?

1. Crear el proyecto en GCP

2. Tomar el  `Forecast.ipynb` del proyecto y añadir en GCP

3. Crear/Añadir el `app.yaml` con la info
```
runtime: python
env: flex
entrypoint: gunicorn -b :$PORT main:app

runtime_config:
  python_version: 3
```
4. Crear/Añadir el `requirements.txt` con la info:

```
Flask==2.0.0
gunicorn==20.0.4
```

5. Una vez creado el proyecto en GCP con los archivos
   - Abrir la consola y ejecutar `gcloud app deploy` Para ejecutar el proyecto
