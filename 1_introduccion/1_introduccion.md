# **Análisis Exploratorio de Datos - Predicción de Reingresos**

## **1. Introducción a la Base de Datos**

**Nombre del dataset:** `diabetic_data.csv`  
**Número de instancias:** 101,766  
**Número de variables:** 47  

### **1.1 Contexto del Dataset**  

El conjunto de datos abarca diez años (1999–2008) de atención clínica en 130 hospitales y redes de prestación de servicios en EE. UU. Cada fila representa un registro hospitalario de pacientes diagnosticados con diabetes, que fueron sometidos a pruebas de laboratorio, tratamientos médicos y hospitalización por hasta 14 días.

---

## **2. Contexto y Diseño del EDA**

### 📘 **Contexto del Problema**

La diabetes es una de las enfermedades crónicas más prevalentes en el mundo y representa un desafío importante para los sistemas de salud debido a su alta tasa de hospitalización y reingresos.  
El análisis de este dataset busca **comprender los factores que influyen en la readmisión hospitalaria** de pacientes con diagnóstico de diabetes, con el propósito de generar información útil para mejorar la gestión clínica y las estrategias preventivas.

---

###  **Objetivos del EDA**

**Objetivo General:**  
Analizar de forma exploratoria los datos de pacientes diabéticos para identificar patrones, relaciones y variables relevantes asociadas con la readmisión hospitalaria.

**Objetivos Específicos:**  
- Examinar la estructura, calidad y consistencia del dataset (`diabetic_data.csv`).
- Describir el perfil demográfico y clínico de los pacientes hospitalizados.  
- Analizar la frecuencia y características de los reingresos (`readmitted`).  
- Explorar posibles asociaciones entre variables clínicas, de tratamiento y la probabilidad de readmisión.
---

###  **Hipótesis de Trabajo**

- **H₀:** No existe relación significativa entre las variables clínicas (como `A1Cresult`, `num_lab_procedures`, `insulin`) y la readmisión hospitalaria.  
- **H₁:** Algunas variables clínicas o de tratamiento sí se asocian significativamente con la readmisión hospitalaria (<30 días o >30 días).

---

###  **Unidad de Análisis**

Cada fila del dataset representa **un encuentro hospitalario individual** de un paciente con diagnóstico de diabetes.  
Un mismo paciente (`patient_nbr`) puede tener múltiples registros (`encounter_id`) si fue atendido en más de una ocasión durante el período de estudio.

---


## **3. ¿Qué encontrarás en este libro?**

- Una descripción general y análisis del dataset.  
- El proceso de limpieza y preparación de los datos.  
- Visualizaciones univariadas y multivariadas.  
- Discusión de hallazgos clave y variables relevantes.  
- Modelados Benchmark, con optimizacion, tuning y mejoras.  

---

## **4. Autoría y Contexto**

- **Autoras:** Guirlessa De la Hoz, Juan Aguirre,  Mariangel Mercado  
- **Curso:** Machine Learning 
- **Fecha:** Octubre de 2025

```{tableofcontents}

