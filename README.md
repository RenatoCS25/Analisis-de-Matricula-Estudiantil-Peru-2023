#  Análisis de Matrícula Estudiantil - Perú 2023

Este proyecto realiza un análisis de datos académicos reales de estudiantes peruanos matriculados en el año 2023. El objetivo es extraer información valiosa sobre las características de los estudiantes, su distribución en las instituciones y detectar factores asociados al riesgo académico.

---
##  2. OBJETIVOS DEL ANÁLISIS

### 2.1 Objetivo General
Analizar los patrones, tendencias y determinantes de la matrícula estudiantil en el sistema educativo peruano durante 2023, identificando factores de riesgo de deserción y proponiendo estrategias basadas en evidencia para mejorar el acceso, la retención y el éxito estudiantil.

---

### 2.2 Objetivos Específicos

 1.Caracterización de la Matrícula  
- Describir la distribución de estudiantes por nivel educativo, edad, género y ubicación.  
- Identificar tendencias de crecimiento/decrecimiento y concentración geográfica.  

2. Análisis de Brechas y Equidad**  
- Cuantificar brechas de género, ubicación y nivel socioeconómico.  
- Detectar desigualdades urbano-rurales y déficit educativo por departamento.  

3. Gestión Pública vs Privada  
- Comparar matrícula, recursos y capacidad instalada entre instituciones públicas y privadas.  
- Analizar migración y tendencias de preferencia por tipo de gestión.  

4. Predicción de Deserción  
- Identificar variables predictoras del abandono escolar.  
- Construir un modelo de clasificación de riesgo y segmentar estudiantes por nivel de vulnerabilidad.  

5. Demanda por Carreras  
- Analizar carreras con mayor o menor demanda y su alineación con el mercado laboral.  
- Detectar áreas saturadas y campos emergentes (tecnología, salud, sostenibilidad).  

6. Recomendaciones Estratégicas  
- Proponer políticas diferenciadas de retención y cobertura.  
- Sugerir sistemas de alerta temprana y optimización de recursos institucionales.  

---

##  3. PREGUNTAS DE INVESTIGACIÓN

¿Cómo ha evolucionado la matrícula en Perú entre 2019 y 2023, y cuáles son las proyecciones para 2024-2025?  
- Impacto de la pandemia (2020-2021) y recuperación posterior.  
- Niveles educativos y regiones con mayor dinamismo.
  
¿Cuáles son las características demográficas y socioeconómicas de los estudiantes?  
- Distribución por género, edad, zona urbana/rural y nivel socioeconómico.  
- Proporción de estudiantes que trabajan o pertenecen a sectores vulnerables.

¿Existen desigualdades significativas en el acceso educativo?  
- Brechas de género, ubicación y nivel socioeconómico.  
- Departamentos con menor cobertura o población no atendida.

¿Cómo se distribuye la matrícula entre instituciones públicas y privadas?  
- Factores asociados a la elección de gestión.  
- Diferencias en retención, cobertura y desempeño.

¿Qué factores predicen la deserción estudiantil y qué proporción de alumnos está en riesgo?  
- Perfil del estudiante vulnerable.  
- Variaciones por nivel educativo y tipo de institución.

¿Cuáles son las carreras más y menos demandadas, y cómo se alinean con la empleabilidad?  
- Carreras emergentes vs saturadas.  
- Ajustes necesarios en la oferta académica.

¿Cómo se distribuye la matrícula en el territorio nacional?  
- Relación entre matrícula y PIB regional.  
- Zonas con déficit de infraestructura y necesidad de inversión.

¿Qué acciones pueden mejorar el acceso, la retención y la equidad educativa?  
- Impacto de programas de becas y apoyo.  
- Políticas efectivas en zonas rurales y en equidad de género (especialmente en STEM).

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
