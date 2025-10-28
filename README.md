#  Análisis de Matrícula Estudiantil - Perú 2023

Este proyecto realiza un análisis de datos académicos reales de estudiantes peruanos matriculados en el año 2023. El objetivo es extraer información valiosa sobre las características de los estudiantes, su distribución en las instituciones y detectar factores asociados al riesgo académico.

---
## 💡 2. DEFINICIÓN DEL PROBLEMA DE NEGOCIO

En el sistema educativo peruano, uno de los principales desafíos es comprender los factores que influyen en la matrícula y permanencia de los estudiantes. A pesar de los avances en cobertura, aún existen diferencias notables entre zonas urbanas y rurales, tipos de institución y niveles educativos. Esta situación genera desigualdades en el acceso, la retención y las oportunidades de aprendizaje, lo que afecta la equidad del sistema educativo.

El problema central radica en la falta de información integrada y analizada que permita identificar patrones y causas relacionadas con la deserción, concentración de matrícula o brechas de acceso. El análisis de la matrícula estudiantil de 2023 busca aportar evidencia para orientar decisiones y políticas públicas basadas en datos.

---

### Preguntas de negocio

1. ¿Cómo se distribuye la matrícula estudiantil según edad, género, nivel educativo y tipo de institución en el Perú durante 2023?  
2. ¿Existen diferencias significativas entre la matrícula en instituciones públicas y privadas a nivel nacional y regional?  
3. ¿Qué regiones o departamentos presentan mayores niveles de desigualdad educativa o menor cobertura escolar?  
4. ¿Cuáles son los factores más asociados a la deserción estudiantil y cómo pueden anticiparse?  
5. ¿Qué tendencias se observan en la demanda por áreas académicas o programas educativos en los distintos niveles?  
6. ¿Qué estrategias podrían aplicarse para mejorar la retención y reducir las brechas educativas?

---

### Objetivo general

Identificar los patrones, tendencias y determinantes de la matrícula estudiantil en el sistema educativo peruano durante el año 2023, con el fin de comprender los factores que influyen en la permanencia, deserción y acceso equitativo a la educación, y así generar información útil para la toma de decisiones y políticas educativas.

---

### Objetivos específicos

1. Analizar la distribución de la matrícula por edad, género, nivel educativo, tipo de institución y ubicación geográfica.  
2. Detectar las brechas de acceso y desigualdades entre zonas urbanas y rurales, así como entre regiones del país.  
3. Evaluar la evolución de la matrícula en instituciones públicas y privadas y su impacto en la cobertura educativa.  
4. Identificar los factores que influyen en la deserción estudiantil utilizando herramientas analíticas o predictivas.  
5. Examinar la relación entre la matrícula y la demanda de áreas académicas en función del contexto socioeconómico.  
6. Proponer estrategias y recomendaciones orientadas a fortalecer la cobertura, equidad y retención en el sistema educativo.

---

📘 **Resumen General:**  
El análisis busca ofrecer una visión integral del sistema educativo peruano, combinando estadísticas, segmentación y modelado predictivo para **comprender la dinámica de matrícula, detectar brechas estructurales** y **proponer estrategias basadas en evidencia** que fortalezcan la equidad y la eficiencia educativa en el país.

##  Dataset

- **Fuente**: [Kaggle - Peru Student Enrollment Data 2023](https://www.kaggle.com/datasets/miguelmallqui17/peru-student-enrollment-data-2023)
- **Formato**: CSV (`;` delimitado)
- **Registros**: +80,000
- **Columnas importantes**:
  - `GENDER`, `AGE RANGE`, `SHIFT/SCHEDULE`, `FACULTY`, `PROGRAM/MAJOR`
  - `TUITION PAYMENT MARCH 2022` y `2023`
  - `NUMBER OF ENROLLED COURSES`, `AT-RISK COURSE`

---
## Tecnologías utilizadas

- Python 3.12
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn (RandomForestClassifier)
- VS Code / Jupyter Notebook

---

##  Fases del Proyecto

### 1. **Carga y Limpieza de Datos**
- Conversión de variables numéricas (pagos, cursos)
- Relleno de valores nulos
- Extracción de edad promedio desde rangos (`EDAD_MEDIA`)
- Codificación de variables categóricas (`get_dummies`)

### 2. **Análisis Exploratorio (EDA)**
- Distribución por género
- Facultades con más matrícula
- Porcentaje de estudiantes con riesgo académico
- Relación entre número de cursos y riesgo

### 3. **Visualización**
Se generan y guardan estos gráficos:
- `facultades_top10.png`: Top 10 de facultades con más alumnos
- `genero_piechart.png`: Distribución por género
- `riesgo_cursos.png`: Comparación de cursos vs riesgo académico

### 4. **Modelo Predictivo**
- Modelo: `RandomForestClassifier`
- Variables predictoras: género, edad, turno, modalidad, beneficios, institución
- Métricas generadas: matriz de confusión, precisión, recall, F1-score

---

##  Resultados esperados

- Identificación de grupos estudiantiles con mayor riesgo
- Base de conocimiento para planes de intervención educativa
- Primer paso hacia sistemas de alerta temprana

---

##  Ejecución del proyecto

### 1. Clonar el repositorio
```bash
git clone https://github.com/tuusuario/matricula-peru-2023.git
cd matricula-peru-2023
