# Predicción de Diabetes con Regresión Lineal Múltiple

Este proyecto utiliza el dataset **[Predict Diabetes from Medical Records (Kaggle)](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)** para estimar la probabilidad de que un paciente tenga diabetes (`Outcome`) en base a variables clínicas.  

## Dataset y variables

El dataset contiene registros médicos de pacientes, con las siguientes columnas:  

- **Pregnancies** → Número de embarazos previos.  
- **Glucose** → Concentración de glucosa en sangre en 2 horas (mg/dL).  
- **BloodPressure** → Presión sanguínea diastólica (mm Hg).  
- **SkinThickness** → Grosor del pliegue cutáneo del tríceps (mm).  
- **Insulin** → Nivel de insulina sérica (mu U/ml).  
- **BMI** → Índice de masa corporal.  
- **DiabetesPedigreeFunction** → Función de historial hereditario de diabetes.  
- **Age** → Edad del paciente (años).  
- **Outcome** → Diagnóstico de diabetes (0 = No, 1 = Sí).  

---

## Valores clínicos de referencia

- **Glucosa**: normal < 100 mg/dL, prediabetes 100–125, diabetes ≥ 126.  
- **Presión sanguínea**: normal < 80 mmHg (diastólica), hipertensión ≥ 90 mmHg.  
- **IMC**: normal 18.5–24.9, sobrepeso 25–29.9, obesidad ≥ 30.  
- **Edad**: el riesgo aumenta después de los 45 años.  

Estos valores permiten interpretar mejor los resultados obtenidos por el modelo.  

---

## Flujo del proyecto

1. **Carga y exploración del dataset**  
   - Se importan los datos y se renombran las columnas a español.  
   - Se realiza análisis exploratorio con gráficos (`pairplot`, `heatmap`).  

2. **Preprocesamiento**  
   - Normalización de variables numéricas con `StandardScaler`.  

3. **Predicción manual**  
   - El script permite ingresar valores clínicos (ejemplo: glucosa = 140, IMC = 32, edad = 60).  
   - El modelo devuelve la probabilidad estimada de diabetes.  
 

---

## Resultados

- El modelo entrega una probabilidad de diabetes en porcentaje (%).  
- Variables como **glucosa, IMC y edad** aparecen con mayor peso en la predicción.  
- El análisis gráfico muestra claras diferencias en la distribución de **glucosa, presión sanguínea e IMC** entre pacientes diabéticos y no diabéticos.  

---

## Ejecución

- Se ingresan los valores de IMC, glucosa y edad.
- Se ejecuta el programa y se observan los resultados.

### Saludos :)
