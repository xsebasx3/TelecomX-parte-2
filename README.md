# 📊 Análisis de Evasión de Clientes – TelecomX

Este proyecto analiza datos de clientes de una empresa de telecomunicaciones con el objetivo de identificar **patrones asociados a la cancelación del servicio (Churn)** y proponer estrategias de retención basadas en evidencia.

---

## 📌 Objetivos

- Analizar la distribución de clientes que cancelan vs. los que permanecen.
- Identificar características demográficas, contractuales y de consumo asociadas al Churn.
- Entrenar modelos de Machine Learning para predecir la evasión de clientes.
- Evaluar el rendimiento de los modelos y determinar los factores más influyentes.
- Proponer acciones estratégicas para reducir la cancelación.

---

## 🗂️ Estructura del proyecto

telecomx-parte2/
├── telecomx_2parte.ipynb     # Notebook principal con análisis y modelos
├── TelecomX_clean.csv        # Dataset limpio utilizado en el análisis
├── README.md                 # Documentación del proyecto
└── LICENSE                   # Licencia del repositorio

---

## 🛠️ Instalación y requisitos

Este proyecto utiliza Python 3.x y las siguientes librerías:
- **pandas**
- **numpy**
- **matplotlib**
- **seaborn**
- **scikit-learn**
- **imbalanced-learn**

Para instalar las dependencias, ejecuta:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
```

---

## ▶️ Ejecución

1. Clona este repositorio:

```bash
git clone https://github.com/tu-usuario/telecomx-parte2.git
cd telecomx-parte2
```
 o descarga los archivos.
 
3. Abre el notebook TelecomX_LATAM.ipynb en Jupyter Notebook o Google Colab [![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/?hl=es-ES 
)
4. Ejecuta todas las celdas en orden para:
   - Cargar y limpiar los datos.
   - Realizar análisis exploratorio.
   - Entrenar y evaluar modelos predictivos.
   - Obtener conclusiones y estrategias de retención.

---

## 📊 Metodología
El análisis se realizó en varias etapas:
  1. Preparacion de Datos
     - Eliminación de columnas irrelevantes (customerID).
     - Codificación de variables categóricas (One-Hot Encoding).
     - Balanceo de clases con SMOTE.
  2. Analisis Exploratorio:
     - Distribución de cancelaciones.
     - Relación entre tipo de contrato, gasto total, cuentas diarias y churn.
     - Matriz de correlación.
  3. Modelado Predictivo
      - Modelos entrenados:
          - Regresión Logística
          - Random Forest
      - Evaluación con métricas: accuracy, precision, recall, F1-score.
      - Visualización de matrices de confusión.
  4. Interpretación y conclusiones
     - Identificación de variables más influyentes.
     - Recomendaciones de retención.

---

## 📌 Resultados destacados
- Regresión Logística: Accuracy ≈ 0.83, buen equilibrio entre precisión y recall.
- Random Forest: Accuracy ≈ 0.84, mejor recall para clientes que cancelan → útil para retención.
- Factores clave en la cancelación:
      - Antigüedad baja (tenure) → mayor probabilidad de cancelar.
      - Método de pago: Electronic Check → fuerte asociación con churn.
      - Contratos mensuales → mayor tasa de bajas.
      - Internet por Fibra Óptica y servicios de streaming correlacionan con mayor churn.
      - Mayor gasto mensual aumenta la probabilidad de cancelación.

---

## 💡 Estrategias de retención propuestas
- Acciones inmediatas
    - Monitoreo y onboarding especial en clientes nuevos.
    - Incentivos para cambiar de Electronic Check a pagos automáticos.
    - Comunicación clara y planes flexibles para evitar cancelaciones por facturación.
- Acciones tácticas (mediano plazo)
    - Promociones y bundles para clientes con contrato mensual.
    - Mejorar experiencia en servicios de Fibra Óptica y streaming.
- Acciones analíticas (largo plazo)
    - Implementar un modelo de score de churn en producción.
    - Probar intervenciones personalizadas y medir impacto con campañas A/B.
---

## 📜 Licencia

Este proyecto se distribuye bajo licencia MIT.

Eres libre de usarlo, modificarlo y distribuirlo.



