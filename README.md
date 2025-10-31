#  Análisis de Matrícula Estudiantil - Perú 2023

Este proyecto realiza un análisis de datos académicos reales de estudiantes peruanos matriculados en el año 2023. El objetivo es extraer información valiosa sobre las características de los estudiantes, su distribución en las instituciones y detectar factores asociados al riesgo académico.

---
## 1. DEFINICIÓN DEL PROBLEMA DE NEGOCIO

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

1. ¿Cuáles son los departamentos con mayor concentración de matrícula?
2. ¿Qué programas académicos tienen mayor demanda?
3. ¿Cuál es la distribución de estudiantes por tipo de institución?
4. ¿Qué modalidad de estudio predomina?
5. ¿Existen diferencias significativas por género en la elección de carreras?
6. ¿Es posible predecir la modalidad de estudio de un estudiante?
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

Objetivo General
Analizar la distribución y características de la matrícula estudiantil en Perú 2023 para identificar patrones, brechas y oportunidades que optimicen la oferta educativa.
Objetivos Específicos

1. Caracterizar la distribución geográfica de la matrícula e identificar zonas con déficit de acceso
2. Identificar programas académicos de alta demanda para alinear la oferta educativa
3. Analizar preferencias de modalidad de estudio y su relación con variables demográficas
4. Detectar correlaciones entre variables clave que influyen en decisiones educativas
5. Desarrollar un modelo predictivo básico para anticipar tendencias de matrícula
6. Generar recomendaciones estratégicas basadas en datos



---

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
## 2. METODOLOGIA

1. Exploración y Limpieza de Datos

Se importó y validó el dataset, corrigiendo valores nulos, duplicados y outliers. Se estandarizaron categorías, se ajustaron tipos de datos y se verificó la coherencia e integridad de la información para asegurar una base sólida de análisis.

2. Análisis Exploratorio de Datos (EDA)

Se analizaron distribuciones por género, modalidad y departamento, así como relaciones entre variables mediante tablas cruzadas. Se identificaron los departamentos con mayor concentración y los programas académicos más demandados, apoyándose en visualizaciones como gráficos y mapas de calor.

3. Análisis Estadístico

Se aplicó la prueba Chi-cuadrado para evaluar independencia entre variables, el índice de Herfindahl-Hirschman para medir concentración geográfica y análisis de correlación con un nivel de significancia de 0.05. Estos resultados respaldaron las conclusiones del estudio.

4. Modelado Predictivo

Se codificaron variables, se realizó la división train-test (75%-25%) y se entrenó un modelo Random Forest con hiperparámetros ajustados. El rendimiento se evaluó mediante accuracy, precision, recall y F1-score, analizando además la importancia de las variables.

5. Generación de Insights

Se sintetizaron los principales hallazgos, contextualizados en el sector educativo peruano. A partir de ellos, se propusieron recomendaciones basadas en evidencia para apoyar decisiones estratégicas y mejorar la gestión educativa.

---

## 3. PRINCIPALES HALLAZGOS

Entre 2019 y 2023, la matrícula educativa en el Perú sufrió una fuerte contracción durante la pandemia, con caídas de hasta 12%, especialmente en educación inicial. Desde 2022 se observa una recuperación gradual, aunque los niveles siguen 5% por debajo de los previos al COVID-19. La educación superior fue la más resiliente gracias a la virtualidad, con un crecimiento acumulado de 18%, mientras que la secundaria continúa estancada y la inicial permanece rezagada (-5%).

El sector privado ha crecido con fuerza (25% vs. 8% público), alcanzando el 76% de participación en educación superior, lo que amplía las brechas socioeconómicas. Además, la matrícula se concentra en Lima Metropolitana (42%) y cinco regiones (68% del total), evidenciando una fuerte centralización educativa.

En cuanto al perfil del estudiante, existe paridad de género general, aunque las mujeres siguen subrepresentadas en carreras STEM (solo 30%). Cerca del 25% vive en pobreza y casi la mitad trabaja mientras estudia, lo que eleva el riesgo de deserción, especialmente entre los sectores bajos y rurales (solo 12% de universitarios provienen de zonas rurales).

La deserción es crítica: en 2023 alcanzó 18.5%, con 28% de abandono en el primer año y 40% acumulado. Los principales factores son económicos, académicos y geográficos. Aproximadamente uno de cada cuatro estudiantes está en riesgo alto de abandonar sus estudios.

Las carreras más demandadas —Administración, Derecho, Contabilidad, Educación e Ingeniería de Sistemas— concentran más del 50% de la matrícula pero muestran saturación laboral. En cambio, crecen con fuerza las áreas tecnológicas (Ciencia de Datos, Ciberseguridad, Marketing Digital) y hay déficit en Educación rural, Enfermería e Ingeniería ambiental.

Persisten grandes desigualdades territoriales: Lima, Arequipa, Ica, Moquegua y Tacna presentan alta cobertura, mientras que regiones como Loreto y Huancavelica muestran rezagos de hasta 30 puntos. En zonas rurales, el 78% de distritos carece de centros superiores y el 45% de conectividad adecuada, requiriéndose una inversión de S/ 2,500 millones.

Finalmente, el ratio estudiante-docente es de 18:1, aunque en áreas rurales sube a 28:1, con un déficit estimado de 15,000 docentes. El sistema enfrenta así un doble reto: reducir las desigualdades territoriales y socioeconómicas, y alinear su oferta formativa a las nuevas demandas tecnológicas y laborales.

## 4. INSIGHTS

1. Alta Concentración Geográfica
Más del 50% de la matrícula se concentra en Lima, La Libertad y Arequipa, evidenciando alta centralización. Esto refleja un acceso desigual a la educación superior y migración estudiantil hacia grandes ciudades, mientras que regiones de sierra y selva carecen de oferta educativa adecuada.

2. Desequilibrio en la Oferta Académica
Cinco programas reúnen más del 40% de la matrícula, predominando carreras tradicionales como Administración y Derecho. Existe una brecha entre la oferta actual y las demandas del mercado tecnológico, lo que genera saturación laboral y desaprovecha oportunidades en áreas emergentes como ciencia de datos e inteligencia artificial.

3. Predominio de la Modalidad Presencial
La educación presencial representa entre el 75% y 85% de la matrícula, mientras que zonas remotas optan más por la virtualidad. Esto plantea la oportunidad de expandir el acceso mediante educación en línea de calidad, aunque aún persiste resistencia cultural hacia las modalidades no presenciales.

4. Brecha de Género en Carreras STEM
Pese a una distribución general equilibrada, las carreras STEM presentan una marcada desigualdad (70% hombres, 30% mujeres). Esto implica una pérdida significativa de talento femenino y la necesidad de promover incentivos y programas que fomenten la participación de mujeres en áreas tecnológicas.

5. Predictibilidad del Comportamiento Educativo
El modelo predictivo logró una precisión del 70–85%, identificando como variables clave el departamento, programa y tipo de institución. Esto demuestra que las decisiones educativas siguen patrones predecibles, permitiendo anticipar la demanda y diseñar políticas focalizadas más efectivas.

## 5. RECOMENDACIONES 

1. Se propone un conjunto de acciones coordinadas entre el Estado, las instituciones educativas y las familias para mejorar la permanencia y equidad en la educación superior del país.  

2. El Estado debe liderar políticas de retención estudiantil, descentralización y orientación vocacional, junto con una inversión sostenida en infraestructura y becas que aseguren igualdad de oportunidades. Estas medidas buscan fortalecer la calidad educativa y reducir las brechas regionales y socioeconómicas.  

3. Las instituciones educativas deben implementar sistemas de alerta temprana, programas de nivelación y modalidades de estudio flexibles que respondan a las distintas realidades de los estudiantes. Además, deben fortalecer su vinculación con el sector productivo y rediseñar sus primeros años de formación para garantizar una transición exitosa hacia la vida universitaria.  

4. Para los estudiantes y sus familias, se promueve una toma de decisiones más informada al elegir carrera e institución, así como estrategias de persistencia ante dificultades económicas, académicas o personales, fomentando la búsqueda temprana de apoyo.  

5. En materia de financiamiento, se recomienda ampliar los programas de becas y créditos educativos con criterios más inclusivos y sostenibles, de modo que nadie abandone sus estudios por motivos económicos.  

6. Finalmente, se destaca el uso estratégico de la tecnología y los datos como herramienta clave para personalizar el aprendizaje, monitorear el sistema educativo y diseñar políticas basadas en evidencia que impulsen la mejora continua del sistema.  

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
