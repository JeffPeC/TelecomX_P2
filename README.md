# TelecomX_P1-2
Segundo Challenge TelecomX
# TelecomX_P2LATAM: Análisis y Predicción de Evasión de Clientes (Churn)

## Descripción del Proyecto

Este proyecto se centra en el análisis y la predicción de la evasión de clientes (Churn) para Telecom X, una compañía de telecomunicaciones ficticia en América Latina. El objetivo principal es identificar los factores clave que impulsan a los clientes a cancelar sus servicios y desarrollar modelos predictivos que permitan a la empresa anticipar y mitigar el Churn.

El análisis abarca desde la extracción y limpieza de datos hasta la exploración de patrones, el modelado predictivo utilizando diferentes algoritmos de Machine Learning, y la interpretación de los resultados para ofrecer recomendaciones estratégicas.

## Objetivo

El objetivo de este proyecto es:

*   Comprender los factores que contribuyen a la evasión de clientes en Telecom X.
*   Construir y evaluar modelos de Machine Learning para predecir qué clientes tienen una alta probabilidad de cancelar su servicio.
*   Proporcionar insights accionables y recomendaciones estratégicas para reducir la tasa de Churn y mejorar la retención de clientes.

## Fuentes de Datos

Los datos utilizados en este análisis provienen de una fuente JSON pública, que contiene información detallada sobre los clientes, sus servicios contratados y su estado de evasión.

*   **Datos de Clientes:** Información demográfica, si son adultos mayores, si tienen pareja o dependientes, y su antigüedad (tenure).
*   **Servicios Contratados:** Detalles sobre servicios telefónicos (líneas múltiples) y servicios de internet (tipo de servicio, seguridad online, respaldo, protección de dispositivo, soporte técnico, streaming de TV y películas).
*   **Información de Cuenta:** Tipo de contrato, facturación electrónica, método de pago y cargos mensuales/totales.
*   **Variable Objetivo (Churn):** Indica si el cliente canceló o no el servicio.

## Etapas del Análisis

El proyecto se desarrolló siguiendo las siguientes etapas principales:

1.  **Extracción:** Carga de los datos directamente desde la API JSON.
2.  **Transformación y Limpieza de Datos:**
    *   Exploración inicial del dataset y comprensión de las columnas.
    *   Identificación y manejo de inconsistencias (valores vacíos, duplicados).
    *   Creación de nuevas variables (como el costo diario).
    *   Normalización y estandarización de variables categóricas y numéricas.
3.  **Análisis Exploratorio de Datos (EDA):**
    *   Análisis descriptivo de variables numéricas y categóricas.
    *   Visualización de la distribución de la evasión.
    *   Recuento y visualización de la evasión por variables categóricas clave (tipo de contrato, método de pago, etc.).
    *   Análisis de la distribución de variables numéricas (antigüedad, cargos) en relación con la evasión.
    *   Análisis de correlación entre variables, incluyendo la relación entre costo diario, cantidad de servicios y evasión.
4.  **Preparación de los Datos para Modelado:**
    *   Eliminación de columnas irrelevantes (como el ID del cliente).
    *   Aplicación de técnicas de Encoding (One-Hot Encoding) a variables categóricas.
    *   Verificación del desbalance de clases y aplicación opcional de técnicas de balanceo (SMOTE).
    *   Normalización/Estandarización de los datos, según los requisitos de los modelos.
5.  **Modelado Predictivo:**
    *   Separación del conjunto de datos en entrenamiento y prueba.
    *   Creación y entrenamiento de múltiples modelos de clasificación (Regresión Logística, Random Forest, SVM, Red Neuronal).
6.  **Evaluación de los Modelos:**
    *   Evaluación del rendimiento de cada modelo utilizando métricas como Exactitud, Precisión, Recall, F1-score y Matriz de Confusión.
    *   Análisis de posibles problemas de overfitting o underfitting.
7.  **Interpretación y Conclusiones:**
    *   Análisis de la importancia de las variables para cada modelo.
    *   Resumen de los hallazgos clave sobre los factores que más influyen en la evasión.
    *   Elaboración de un informe final con conclusiones detalladas y recomendaciones estratégicas.

## Resultados Clave e Insights

Los principales hallazgos del análisis incluyen:

*   Los clientes con **contratos de "Mes a Mes"** y aquellos que pagan con **"Cheque Electrónico"** muestran una tasa de evasión significativamente más alta.
*   La **antigüedad del cliente** es un fuerte predictor de la retención; los clientes nuevos son más propensos a cancelar.
*   Los **cargos mensuales elevados**, especialmente asociados a servicios de alto costo como la fibra óptica, están relacionados con una mayor probabilidad de evasión.
*   Existe una relación no lineal entre la **cantidad de servicios contratados** y la evasión, con picos en clientes con muy pocos o demasiados servicios.
*   El **Random Forest** mostró el mejor rendimiento general en la predicción de la evasión, aunque con signos de overfitting que podrían requerir ajuste de hiperparámetros.

## Recomendaciones Estratégicas

Con base en los resultados obtenidos, se proponen las siguientes recomendaciones para Telecom X:

*   **Incentivar Contratos a Largo Plazo:** Ofrecer descuentos y beneficios a clientes de "Mes a Mes" para migrar a contratos anuales.
*   **Mejorar el Onboarding de Nuevos Clientes:** Implementar un programa de bienvenida y seguimiento proactivo en los primeros meses.
*   **Promover Métodos de Pago Automáticos:** Incentivar el cambio a domiciliación bancaria o tarjeta de crédito mediante pequeños beneficios.
*   **Optimizar la Oferta de Servicios:** Analizar el perfil de consumo para ofrecer paquetes personalizados que equilibren valor y costo.
*   **Desarrollar un Sistema de Alerta Temprana:** Identificar a clientes de alto riesgo basándose en los factores clave para intervenciones proactivas.

## Cómo Ejecutar el Código

Para replicar este análisis, sigue los pasos detallados en el notebook de Google Colab. Asegúrate de tener las librerías necesarias instaladas (pandas, numpy, sklearn, seaborn, matplotlib, imblearn).
