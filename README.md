#Análisis de Evasión de Clientes (Churn) - Telecom X

Este proyecto forma parte de un desafío de Data Science enfocado en identificar los factores que influyen en la pérdida de clientes de una empresa de telecomunicaciones. El análisis abarca desde la limpieza de datos JSON anidados hasta la creación de un perfil de riesgo para la toma de decisiones estratégicas.

##Tecnologías Utilizadas
* **Python** (Core del análisis)
* **Pandas**: Limpieza y manipulación de datos.
* **Matplotlib & Seaborn**: Visualización estadística y descriptiva.
* **JSON**: Procesamiento de estructuras de datos anidadas.

##Proceso del Proyecto

### 1. Limpieza y Preparación de Datos
* **Normalización:** Se aplanaron las estructuras JSON (`customer`, `phone`, `internet`, `account`) para crear un DataFrame plano.
* **Manejo de Nulos:** Se identificaron y eliminaron 213 registros inconsistentes en la variable objetivo (`Churn`).
* **Transformación:** Conversión de variables categóricas (Yes/No) a formato binario (1/0) y normalización de textos.
* **Feature Engineering:** Creación de la métrica `Cuentas_Diarias` para evaluar el impacto del costo diario en el usuario.

### 2. Hallazgos Principales (Insights)
* **Factor Económico:** Los clientes que cancelan el servicio tienen un gasto mensual promedio más alto (~$74) que los leales (~$61).
* **Ventana de Riesgo:** El Churn se concentra en clientes nuevos, con un promedio de permanencia de solo **18 meses**, frente a los **37 meses** de los clientes leales.
* **Variables Críticas:** El tipo de contrato **"Month-to-Month"** y los métodos de pago manuales son los principales predictores de abandono.

##Estructura del Repositorio
* `TelecomX_Data.json`: Dataset original.
* `Analisis_Descriptivo.ipynb`: Notebook con la limpieza y visualizaciones de la Parte 1.
* `Modelado_Prediccion.ipynb`: Procesamiento de variables y matriz de correlación (Parte 2).
* `telecom_limpio.csv`: Archivo exportado con los datos procesados.

##  Conclusiones
Para reducir la evasión, se recomienda incentivar la migración de contratos mensuales a anuales y fortalecer los programas de fidelización durante los primeros 18 meses de vida del cliente.

---
Proyecto desarrollado por ] como parte del curso de Alura Latam.
