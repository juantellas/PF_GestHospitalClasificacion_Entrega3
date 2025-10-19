# **Descripción de Variables**

A continuación se describen las variables presentes en el dataset `diabetic_data.csv`, organizadas por categorías y con sus respectivas unidades o escalas de medición.

---

## 🔐 Variables de Identificación

| Variable       | Tipo       | Unidad / Escala | Descripción |
|----------------|------------|------------------|-------------|
| `encounter_id` | Numérica   | — | Identificador único del encuentro hospitalario (visita). |
| `patient_nbr`  | Numérica   | — | Identificador único del paciente. |

---

## 👤 Datos Demográficos y de Ingreso

| Variable               | Tipo        | Unidad / Escala | Descripción |
|------------------------|-------------|------------------|-------------|
| `race`                 | Categórica  | — | Raza del paciente. Valores: Caucasian, Asian, African American, Hispanic, Other. |
| `gender`               | Categórica  | — | Género del paciente. Valores: male, female, unknown/invalid. |
| `age`                  | Categórica  | Años (rangos de 10 años) | Edad agrupada en intervalos de 10 años (ej. [50-60)). |
| `weight`               | Categórica  | Libras (lbs) | Peso del paciente (en libras). Muchos valores faltantes. |
| `admission_type_id`    | Categórica (codificada) | — | Tipo de admisión (1=Emergency, 2=Urgent, 3=Elective, etc.). |
| `discharge_disposition_id` | Categórica (codificada) | — | Disposición al alta. Indica el destino del paciente al ser dado de alta. |
| `admission_source_id`  | Categórica (codificada) | — | Fuente de admisión (referencia médica, urgencias, etc.). |
| `time_in_hospital`     | Numérica    | Días | Días de estancia en el hospital. |

---

## 🔬 Pruebas y Procedimientos

| Variable             | Tipo     | Unidad / Escala | Descripción |
|----------------------|----------|------------------|-------------|
| `num_lab_procedures` | Numérica | Conteo | Número de pruebas de laboratorio realizadas. |
| `num_procedures`     | Numérica | Conteo | Número de procedimientos distintos realizados (excluye laboratorios). |
| `num_medications`    | Numérica | Conteo | Número de medicamentos diferentes administrados. |
| `number_outpatient`  | Numérica | Conteo | Número de visitas ambulatorias previas. |
| `number_emergency`   | Numérica | Conteo | Número de visitas a urgencias previas. |
| `number_inpatient`   | Numérica | Conteo | Número de ingresos hospitalarios previos. |
| `number_diagnoses`   | Numérica | Conteo | Número de diagnósticos registrados. |

---

## 🏥 Diagnósticos Principales

| Variable | Tipo     | Unidad / Escala | Descripción |
|----------|----------|------------------|-------------|
| `diag_1` | Categórica | Código ICD9 | Diagnóstico principal (código ICD9, 3 dígitos). |
| `diag_2` | Categórica | Código ICD9 | Diagnóstico secundario. |
| `diag_3` | Categórica | Código ICD9 | Diagnóstico adicional. |

---

## 💉 Resultados de Laboratorio

| Variable       | Tipo       | Unidad / Escala | Descripción |
|----------------|------------|------------------|-------------|
| `max_glu_serum`| Categórica | mg/dL (implícita) | Resultado máximo de glucosa en suero. Valores: >200, >300, normal, none. |
| `A1Cresult`    | Categórica | % (hemoglobina glicosilada) | Resultado de hemoglobina A1C. Valores: >8, >7, normal, none. |

---

## 💊 Medicamentos Administrados

Cada una de las siguientes variables indica si el medicamento fue administrado y si hubo cambio de dosis.  
**Valores posibles:** `up`, `down`, `steady`, `no`.

**Variables:**

`metformin`, `repaglinide`, `nateglinide`, `chlorpropamide`, `glimepiride`, `acetohexamide`, `glipizide`, `glyburide`, `tolbutamide`, `pioglitazone`, `rosiglitazone`, `acarbose`, `miglitol`, `troglitazone`, `tolazamide`, `examide`, `citoglipton`, `insulin`, `glyburide-metformin`, `glipizide-metformin`, `glimepiride-pioglitazone`, `metformin-rosiglitazone`, `metformin-pioglitazone`.

---

## ⚙️ Control del Tratamiento

| Variable      | Tipo       | Unidad / Escala | Descripción |
|---------------|------------|------------------|-------------|
| `change`      | Categórica | — | Indica si hubo algún cambio en los medicamentos para la diabetes durante la estancia (`change`, `no change`). |
| `diabetesMed` | Categórica | — | Indica si se prescribió algún medicamento para la diabetes (`yes`, `no`). |

---

## 🎯 Variable Objetivo

| Variable     | Tipo       | Unidad / Escala | Descripción |
|--------------|------------|------------------|-------------|
| `readmitted` | Categórica | Días desde el alta | Indica si el paciente fue readmitido y cuándo. Valores: `<30` (antes de 30 días), `>30` (después de 30 días), `No` (sin reingreso). |

---

### 📌 **Notas adicionales**

- Los diagnósticos (`diag_1`, `diag_2`, `diag_3`) usan **códigos ICD-9**, donde, por ejemplo:  
  - `250.xx` → Diabetes mellitus.  
  - `401.xx` → Hipertensión esencial.  
  - `414.xx` → Enfermedad cardíaca isquémica.  
- Las variables `age` y `weight` se presentan en **intervalos discretos** para proteger la privacidad del paciente.  
- Los valores `?` representan **datos faltantes o no registrados**.  
- Los resultados de laboratorio (`max_glu_serum`, `A1Cresult`) son **rangos categóricos** basados en valores clínicos.
---
