# 📊 Telecom X – Challenge Parte 2: Predicción de Cancelación (Churn)

## 🚀 Descripción del Proyecto
Este proyecto corresponde a la **segunda parte del Challenge de Telecom X**.  
En la **Parte 1**, se realizó la limpieza y organización del dataset original (`TelecomX_Data.json`).  
En esta **Parte 2**, desarrollamos modelos de Machine Learning para **predecir qué clientes tienen mayor probabilidad de cancelar el servicio (churn)** y generar **estrategias de retención basadas en datos**.

---

## 🎯 Objetivos del Challenge
- Preparar los datos para el modelado (tratamiento, codificación, normalización).
- Realizar análisis de correlación y selección de variables.
- Entrenar al menos **dos modelos de clasificación**:
  - Uno sensible a la escala (ej. Regresión Logística, KNN).
  - Otro insensible a la escala (ej. Random Forest, Decision Tree).
- Evaluar el rendimiento de los modelos con métricas:  
  `Accuracy`, `Precisión`, `Recall`, `F1-score`, `Matriz de confusión`.
- Interpretar los resultados, incluyendo la importancia de las variables.
- Crear conclusiones estratégicas y proponer **estrategias de retención**.

---

## 🗂️ Estructura del Repositorio
├── TelecomX_Parte2_Churn.ipynb # Notebook principal (Parte 2)
├── TelecomX_clean.csv # Dataset limpio generado en Parte 1
├── README.md # Este documento
├── requirements.txt # Librerías necesarias (opcional)
└── report.pdf # (Opcional) Notebook exportado a PDF

markdown
Copiar
Editar

---

## 🛠️ Tecnologías Utilizadas
- **Python 3.9+**
- **Pandas** (manipulación de datos)
- **NumPy** (cálculo numérico)
- **Matplotlib / Seaborn** (visualización)
- **Scikit-learn** (modelado y métricas)

---

## 📈 Metodología
1. **Preprocesamiento**
   - Eliminación de columnas irrelevantes (`customerID`).
   - Codificación de variables categóricas con One-Hot Encoding.
   - Normalización de variables numéricas para modelos sensibles a escala.

2. **Análisis exploratorio**
   - Matriz de correlación.
   - Boxplots y scatter plots de variables clave (`tenure`, `MonthlyCharges`, `TotalCharges`) respecto a `Churn`.

3. **Modelado**
   - **Modelo 1:** Regresión Logística (con normalización).  
   - **Modelo 2:** Random Forest (sin normalización).  

4. **Evaluación**
   - Métricas: Accuracy, Precisión, Recall, F1-score.  
   - Matriz de confusión.  
   - Análisis de overfitting/underfitting.

5. **Interpretación de variables**
   - Coeficientes en Regresión Logística.  
   - Importancia de variables en Random Forest.  

---

## 🔑 Principales Hallazgos
- **Mayor riesgo de churn** en clientes:
  - Con contrato **Month-to-Month**.
  - Con **tenure bajo** (poca antigüedad).
  - Que pagan con **Electronic Check**.
  - Con **cargos mensuales altos**.
- **Menor riesgo de churn** en clientes:
  - Con contratos de **1 o 2 años**.
  - Con métodos de pago automáticos (tarjeta/transferencia).
  - Con **servicios adicionales de valor agregado** (seguridad online, soporte técnico).

---

## 📌 Estrategias de Retención Propuestas
- Incentivar la migración de contratos **Month-to-Month → 1 o 2 años** con descuentos o beneficios.
- Contacto proactivo durante los **primeros 90 días** (tenure bajo).
- Ofrecer **planes optimizados/bundles** a clientes con cargos altos.
- Promover **métodos de pago automáticos** con beneficios.
- Campañas de fidelización basadas en el **score de churn**.
