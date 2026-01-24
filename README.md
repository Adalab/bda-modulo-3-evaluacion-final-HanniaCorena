# 📊 Proyecto de Análisis de Datos de Clientes y Vuelos

## 🧾 Descripción general
Este proyecto consiste en el análisis de dos conjuntos de datos (CSV) relacionados con un programa de fidelización aérea, datos de y actividad de los clientes. El objetivo principal es responder una serie de preguntas analíticas sobre el comportamiento de los clientes, sus características demográficas y socioeconómicas, y sus patrones de reserva de vuelos.

El trabajo se ha organizado de forma modular y estructurada, utilizando **tres Jupyter Notebooks**, lo que permite una mayor claridad, trazabilidad y reutilización del análisis.


---

## 📊 Conjuntos de datos

### 1️⃣ Dataset de vuelos (CFA)
Contiene información sobre la actividad de vuelos de los clientes:

- Loyalty Number  
- Year  
- Month  
- Flights Booked  
- Flights with Companions  
- Total Flights  
- Distance  
- Points Accumulated  
- Points Redeemed  
- Dollar Cost Points Redeemed  

---

### 2️⃣ Dataset de clientes (CLH)
Incluye características demográficas, geográficas y socioeconómicas:

- Loyalty Number  
- Country  
- Province  
- City  
- Postal Code  
- Gender  
- Education  
- Salary  
- Marital Status  
- Loyalty Card  
- CLV  
- Enrollment Type  
- Enrollment Year  
- Enrollment Month  
- Cancellation Year  
- Cancellation Month  

---

## 📓 Organización del análisis

### 📘 Notebook 1: Análisis de vuelos
**Dataset utilizado:** CFA  

Preguntas respondidas:
1. ¿Cómo se distribuye la cantidad de vuelos reservados por mes durante el año?  
2. ¿Existe una relación entre la distancia de los vuelos y los puntos acumulados por los clientes?

En este notebook se realizó:
- Análisis temporal de vuelos
- Se limpió la columna Points Accumulated, pues estaba en Float
- Visualizaciones (histogramas y scatter plots)
- Análisis de relación entre variables de vuelos
- Se respondieron las preguntas planteadas en el ejercicio.


---

### 📗 Notebook 2: Análisis de clientes
**Dataset utilizado:** CLH  

Preguntas respondidas:
3. ¿Cuál es la distribución de los clientes por provincia o estado?  
4. ¿Cómo se compara el salario promedio entre los diferentes niveles educativos de los clientes?  
5. ¿Cuál es la proporción de clientes con diferentes tipos de tarjetas de fidelidad?  
6. ¿Cómo se distribuyen los clientes según su estado civil y género?

En este notebook se realizó:
- Limpieza de datos
- Tratamiento de valores negativos en la variable `Salary`
- Imputación de valores faltantes utilizando la mediana
- Análisis descriptivo y visualizaciones
- Se respondieron las preguntas planteadas en el ejercicio.

---

### 📙 Notebook 3: Merge y análisis final
**Datasets utilizados:** CFA + CLH  

Objetivo:
- Evaluar si existen diferencias significativas en el número de vuelos reservados según el nivel educativo de los clientes.

Proceso:
- Merge de ambos datasets utilizando `Loyalty Number` como clave
- Selección de variables relevantes (`Flights Booked`, `Education`)
- Análisis descriptivo del número de vuelos por nivel educativo
- Se respondió la pregunta planteada en el ejercicio.
- Se añaden los gráficos idóneos para el análisis bivariado de variables categóricas y numéricas, un barplot y un boxplot.
- Los gráficos no los pide el ejercicio pero se añaden para apoyar la conclusión

Este enfoque permitió integrar información de comportamiento de vuelos con variables sociodemográficas.

---

## 🧼 Limpieza y tratamiento de datos relevantes

- Los valores negativos en la variable **Salary** fueron considerados errores de registro.
- Se forzó la conversión de la variable a formato numérico.
- Los valores inválidos y negativos se trataron como valores faltantes.
- Dado que la distribución del salario presenta asimetría positiva, los valores faltantes se imputaron utilizando la **mediana**.
- Se limpió la columna Points Accumulated, pues estaba en Float.

---

## 🛠️ Tecnologías utilizadas

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Jupyter Notebook  


## ✅ Conclusión

El análisis se estructuró de manera modular, permitiendo responder las preguntas planteadas de forma clara y eficiente. Solo fue necesario realizar un merge de los datasets en el análisis final, mientras que el resto de preguntas pudieron resolverse utilizando cada conjunto de datos de forma independiente.

Este enfoque reduce la complejidad innecesaria y mejora la interpretabilidad del análisis.

---

✍️ *Proyecto desarrollado como ejercicio de análisis exploratorio y descriptivo de datos.*


