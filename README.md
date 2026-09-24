<img width="921" height="269" alt="image" src="https://github.com/user-attachments/assets/38e789a9-e7b1-43f6-89c5-bf452d374b52" />

# Modelo Predictivo de Cancelación de Clientes Mediante Algoritmos de Clasificación: Caso Interconnect

## Problema
En la industria de las telecomunicaciones, la retención de usuarios es un factor determinante para garantizar la rentabilidad del negocio. El costo de adquisición de un nuevo cliente supera significativamente el de mantener a uno activo.  
El objetivo de este proyecto es analizar los patrones de abandono (*churn*) en la empresa **Interconnect** y construir un modelo predictivo capaz de anticipar qué clientes tienen alta probabilidad de cancelar sus servicios, permitiendo al equipo de marketing ejecutar estrategias de fidelización preventivas[cite: 1].

---

## Datos
El análisis integró cuatro fuentes de información vinculadas mediante el identificador `customerID` (7,043 registros)[cite: 1]:

- **Contratos:** tipo de contrato, método de pago, cargos mensuales y cargos totales (`contract.csv`)[cite: 1]  
- **Demografía:** género, jubilación, pareja y dependientes (`personal.csv`)[cite: 1]  
- **Internet:** tipo de conexión y servicios de valor agregado (`internet.csv`)[cite: 1]  
- **Telefonía:** uso del servicio telefónico y múltiples líneas (`phone.csv`)[cite: 1]  

---

## Enfoque
El proyecto siguió una metodología estructurada de ciencia de datos y modelado predictivo:

- Preprocesamiento, limpieza e imputación de nulos en `TotalCharges`[cite: 1]  
- Ingeniería de características: cálculo de antigüedad (`tenure_days`) y definición del target `Churn`[cite: 1]  
- Prevención de *data leakage* mediante la eliminación de `customerID` y `EndDate`[cite: 1]  
- Experimentación multiescenario: evaluación en subconjuntos de datos (clientes con internet, sin internet y dataset completo)[cite: 1]  
- Entrenamiento y evaluación de **Regresión Logística**, **Random Forest** y **XGBoost** con validación cruzada y conjunto de prueba independiente[cite: 1]  

---

## Resultados
El modelo **`XGBClassifier` entrenado con el Dataset Completo** ofreció el mejor desempeño general[cite: 1]:

- **AUC-ROC (Test):** 0.9285[cite: 1]  
- **Accuracy (Test):** 89.43%[cite: 1]  
- **Puntuación SP:** 6.0 / 6.0 (Calificación máxima)[cite: 1]  

### Otros resultados clave:
- **Poder discriminativo:** El dataset completo superó de forma consistente a los subconjuntos divididos, demostrando que la interacción entre servicios web, telefonía y antigüedad es determinante para predecir el churn[cite: 1].  
- **Generalización:** Presentó métricas alineadas entre el conjunto de validación (AUC-ROC: 0.9211) y prueba (AUC-ROC: 0.9285), descartando sobreajuste[cite: 1].  

---

## Conclusión
El análisis demostró que los modelos de aprendizaje automático basados en *gradient boosting* permiten identificar proactivamente el riesgo de abandono en el sector de telecomunicaciones[cite: 1]. 

Implementar este modelo en producción proporcionará a Interconnect una herramienta automatizada para segmentar campañas de retención (+89% de precisión), protegiendo el *Customer Lifetime Value* (LTV) e incrementando la estabilidad de los ingresos recurrentes[cite: 1].

---

## Herramientas y Tecnologías
- Python  
- Pandas  
- NumPy  
- Scikit-Learn  
- XGBoost  
- Matplotlib  
- Seaborn  

---

## Conclusión Clave
Este proyecto demuestra la aplicación práctica de clasificación avanzada para resolver un desafío operativo y financiero de alto impacto en telecomunicaciones, conectando la ingeniería de datos con decisiones estratégicas de retención de clientes[cite: 1].

---
---

# Customer Churn Prediction Model Using Classification Algorithms – Interconnect Case Study

## Problem
In the telecommunications industry, customer retention is critical for maintaining profitability. The cost of acquiring a new subscriber significantly exceeds the cost of retaining an existing one.  
The goal of this project is to analyze churn patterns at **Interconnect** and build a machine learning pipeline capable of predicting which customers are at high risk of canceling their services, enabling the marketing team to trigger proactive retention campaigns[cite: 1].

---

## Data
The analysis consolidated four relational data sources linked by `customerID` (7,043 records)[cite: 1]:

- **Contractual data:** contract type, payment method, monthly and total charges (`contract.csv`)[cite: 1]  
- **Demographics:** gender, senior citizen status, partner, and dependents (`personal.csv`)[cite: 1]  
- **Internet services:** connection type and add-on services (`internet.csv`)[cite: 1]  
- **Phone services:** multiple lines and phone feature usage (`phone.csv`)[cite: 1]  

---

## Approach
The project followed a structured data science and predictive modeling workflow:

- Data cleaning and null value imputation in `TotalCharges`[cite: 1]  
- Feature engineering: calculated customer tenure (`tenure_days`) and target variable `Churn`[cite: 1]  
- Data leakage prevention by dropping `customerID` and `EndDate`[cite: 1]  
- Multi-scenario evaluation: model assessment across subset segments (internet users, non-internet users, and full dataset)[cite: 1]  
- Training and evaluation of **Logistic Regression**, **Random Forest**, and **XGBoost** classifiers[cite: 1]  

---

## Results
The **`XGBClassifier` model trained on the Full Dataset** achieved the top performance[cite: 1]:

- **Test AUC-ROC:** 0.9285[cite: 1]  
- **Test Accuracy:** 89.43%[cite: 1]  
- **SP Score:** 6.0 / 6.0 (Maximum score)[cite: 1]  

### Other key results:
- **Discriminative power:** The full dataset consistently outperformed segmented subsets, confirming that churn risk depends on multi-service interaction and tenure[cite: 1].  
- **Generalization:** Validation AUC-ROC (0.9211) closely matched test AUC-ROC (0.9285), demonstrating robust generalization without overfitting[cite: 1].  

---

## Conclusion
Statistical and machine learning modeling confirmed that gradient boosting algorithms effectively anticipate customer churn in telecommunications[cite: 1]. 

Deploying this predictive model equips Interconnect with an automated mechanism to target retention incentives (+89% accuracy), protecting Customer Lifetime Value (LTV) and stabilizing recurring revenue[cite: 1].

---

## Tools and Technologies
- Python  
- Pandas  
- NumPy  
- Scikit-Learn  
- XGBoost  
- Matplotlib  
- Seaborn  

---

## Key Takeaway
This project showcases the application of machine learning classification to address a high-impact business problem, bridging data engineering with proactive customer retention strategy[cite: 1].
