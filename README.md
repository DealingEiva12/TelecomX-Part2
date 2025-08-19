# 📊 Análisis Predictivo de Cancelación de Clientes – TelecomX

## 🧠 Objetivo del Proyecto

Este proyecto tiene como propósito identificar los factores que más influyen en la cancelación de clientes (churn) en una empresa de telecomunicaciones. A través de técnicas de análisis exploratorio, preprocesamiento de datos y modelos de machine learning, se busca generar recomendaciones estratégicas para mejorar la retención de clientes.

---

## 📁 Estructura del Proyecto

- `TelecomX.csv`: Dataset original con información de clientes.
- `scripts/`: Contiene scripts de limpieza, codificación, balanceo y modelado.
- `visualizaciones/`: Gráficas generadas para análisis exploratorio y explicativo.
- `README.md`: Documento explicativo del proyecto.

---

## ⚙️ Proceso de Análisis

### 1. Limpieza de Datos
- Eliminación de columnas irrelevantes (`customerID`).
- Conversión de variables categóricas a formato numérico (`get_dummies`).
- Verificación y tratamiento de valores nulos.

### 2. Análisis Exploratorio
- Distribución de cancelaciones (`Churn`) mediante gráficos de barras y pie charts.
- Matriz de correlación para identificar variables numéricas relevantes.
- Visualización de relaciones clave:
  - `tenure × Churn`
  - `TotalCharges × Churn`

### 3. Balanceo de Clases
- Evaluación de desbalance entre clases.
- Aplicación de técnicas:
  - `RandomUnderSampler`
  - `RandomOverSampler`
  - `SMOTE`

### 4. División de Datos
- Separación en conjunto de entrenamiento (70%) y prueba (30%) con estratificación.

---

## 🤖 Modelos Implementados

| Modelo                | Requiere Normalización | Métrica Principal | Accuracy Aproximado |
|----------------------|------------------------|-------------------|---------------------|
| Regresión Logística  | ✅ Sí                  | Coeficientes      | 78–82%              |
| KNN                  | ✅ Sí                  | Permutación       | 75–80%              |
| Random Forest        | ❌ No                  | Impureza          | 85–88%              |
| SVM (lineal)         | ✅ Sí                  | Coeficientes      | 80–83%              |
| XGBoost              | ❌ No                  | Ganancia Relativa | 86–89%              |

---

## 🔍 Variables Más Relevantes

- `tenure`: Clientes con menor antigüedad tienen mayor probabilidad de cancelar.
- `TotalCharges`: Bajo gasto acumulado se asocia con mayor churn.
- `MonthlyCharges`: Cargos elevados sin beneficios claros generan insatisfacción.
- `Contract`: Contratos mensuales presentan mayor tasa de cancelación.
- `TechSupport` e `InternetService`: La ausencia de servicios adicionales aumenta el riesgo de abandono.

---

## 📈 Visualización de Importancia de Variables

Cada modelo fue acompañado por una gráfica distinta para resaltar su enfoque:

- Regresión Logística → Barplot horizontal
- KNN → Scatter plot
- Random Forest → Pie chart
- SVM → Line plot
- XGBoost → Heatmap individual

---

## 🛡️ Estrategias de Retención Recomendadas

- **Fidelización temprana**: Beneficios exclusivos para clientes nuevos.
- **Migración de contratos**: Incentivos para pasar de mensual a anual.
- **Optimización de precios**: Revisión de cargos mensuales.
- **Valor agregado**: Promoción de servicios como soporte técnico.
- **Alertas proactivas**: Activación de campañas automatizadas para clientes en riesgo.

---

## 📌 Conclusión

El análisis permitió identificar patrones robustos en la cancelación de clientes. La variable `tenure` se posiciona como el principal indicador de riesgo, seguida por el tipo de contrato y el gasto mensual. Las estrategias de retención deben enfocarse en mejorar la experiencia inicial del cliente, ofrecer valor tangible y anticiparse al abandono mediante modelos predictivos.

---

## 🧠 Autor

**Edgar**  
Analista de datos y Ingeniero en Testeo de Software
