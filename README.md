# 🧪 Predicción de Diabetes con Regresión Lineal Múltiple

Este proyecto utiliza el dataset **[Predict Diabetes from Medical Records (Kaggle)](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)** para estimar la probabilidad de que un paciente tenga diabetes (`Outcome`) en base a variables clínicas.  

El objetivo es aplicar un **modelo de regresión lineal múltiple** (y posteriormente regresión logística) que permita:  
1. Calcular la probabilidad de diabetes en función de variables médicas.  
2. Identificar los factores con mayor influencia en la predicción.  
3. Permitir el ingreso manual de características clínicas para obtener una predicción personalizada.  

---

## 📊 Dataset y variables

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

## ⚕️ Valores clínicos de referencia

- **Glucosa**: normal < 100 mg/dL, prediabetes 100–125, diabetes ≥ 126.  
- **Presión sanguínea**: normal < 80 mmHg (diastólica), hipertensión ≥ 90 mmHg.  
- **IMC**: normal 18.5–24.9, sobrepeso 25–29.9, obesidad ≥ 30.  
- **Edad**: el riesgo aumenta después de los 45 años.  

Estos valores permiten interpretar mejor los resultados obtenidos por el modelo.  

---

## 🔎 Flujo del proyecto

1. **Carga y exploración del dataset**  
   - Se importan los datos y se renombran las columnas a español.  
   - Se realiza análisis exploratorio con gráficos (`pairplot`, `heatmap`).  

2. **Preprocesamiento**  
   - Normalización de variables numéricas con `StandardScaler`.  
   - Eliminación de valores faltantes (si los hubiera).  

3. **Modelado**  
   - Se implementa **Regresión Lineal Múltiple** (`LinearRegression`) para una primera aproximación.  
   - Se recomienda usar **Regresión Logística** (`LogisticRegression`) dado que la salida es categórica (0/1).  

4. **Predicción manual**  
   - El script permite ingresar valores clínicos (ejemplo: glucosa = 140, IMC = 32, edad = 60).  
   - El modelo devuelve la probabilidad estimada de diabetes.  

5. **Interpretación de resultados**  
   - Se analizan los coeficientes del modelo para identificar qué variables tienen mayor peso en la predicción.  
   - Se comparan los valores clínicos ingresados con los rangos de referencia.  

---

## 📈 Resultados

- El modelo entrega una probabilidad de diabetes en porcentaje (%).  
- Variables como **glucosa, IMC y edad** aparecen con mayor peso en la predicción.  
- El análisis gráfico muestra claras diferencias en la distribución de **glucosa, presión sanguínea e IMC** entre pacientes diabéticos y no diabéticos.  

---

## 🚀 Ejecución

1. Clonar el repositorio:  
   ```bash
   git clone https://github.com/tuusuario/regresion-diabetes.git
   cd regresion-diabetes
