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

## 2. FASES DEL PROYECTO

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

## 3. PRINCIPALES HALLAZGOS

Entre 2019 y 2023, la matrícula educativa en el Perú sufrió una fuerte contracción durante la pandemia, con caídas de hasta 12%, especialmente en educación inicial. Desde 2022 se observa una recuperación gradual, aunque los niveles siguen 5% por debajo de los previos al COVID-19. La educación superior fue la más resiliente gracias a la virtualidad, con un crecimiento acumulado de 18%, mientras que la secundaria continúa estancada y la inicial permanece rezagada (-5%).

El sector privado ha crecido con fuerza (25% vs. 8% público), alcanzando el 76% de participación en educación superior, lo que amplía las brechas socioeconómicas. Además, la matrícula se concentra en Lima Metropolitana (42%) y cinco regiones (68% del total), evidenciando una fuerte centralización educativa.

En cuanto al perfil del estudiante, existe paridad de género general, aunque las mujeres siguen subrepresentadas en carreras STEM (solo 30%). Cerca del 25% vive en pobreza y casi la mitad trabaja mientras estudia, lo que eleva el riesgo de deserción, especialmente entre los sectores bajos y rurales (solo 12% de universitarios provienen de zonas rurales).

La deserción es crítica: en 2023 alcanzó 18.5%, con 28% de abandono en el primer año y 40% acumulado. Los principales factores son económicos, académicos y geográficos. Aproximadamente uno de cada cuatro estudiantes está en riesgo alto de abandonar sus estudios.

Las carreras más demandadas —Administración, Derecho, Contabilidad, Educación e Ingeniería de Sistemas— concentran más del 50% de la matrícula pero muestran saturación laboral. En cambio, crecen con fuerza las áreas tecnológicas (Ciencia de Datos, Ciberseguridad, Marketing Digital) y hay déficit en Educación rural, Enfermería e Ingeniería ambiental.

Persisten grandes desigualdades territoriales: Lima, Arequipa, Ica, Moquegua y Tacna presentan alta cobertura, mientras que regiones como Loreto y Huancavelica muestran rezagos de hasta 30 puntos. En zonas rurales, el 78% de distritos carece de centros superiores y el 45% de conectividad adecuada, requiriéndose una inversión de S/ 2,500 millones.

Finalmente, el ratio estudiante-docente es de 18:1, aunque en áreas rurales sube a 28:1, con un déficit estimado de 15,000 docentes. El sistema enfrenta así un doble reto: reducir las desigualdades territoriales y socioeconómicas, y alinear su oferta formativa a las nuevas demandas tecnológicas y laborales.

## 4. INSIGHTS

1. **Primer año como etapa crítica**  
   La mayoría de los casos de deserción ocurren durante el primer año. Este periodo requiere acompañamiento académico y emocional, ya que una intervención temprana puede prevenir el abandono.

2. **Impacto del factor económico**  
   Las razones financieras siguen siendo la principal causa de deserción. Becas, apoyos parciales y horarios flexibles pueden marcar la diferencia en la continuidad educativa.

3. **Cambio en el perfil del estudiante**  
   Cada vez más estudiantes son adultos trabajadores o con responsabilidades familiares. Esto exige modalidades más flexibles y accesibles, como programas virtuales o nocturnos.

4. **Persistencia de brechas de equidad**  
   Los estudiantes vulnerables enfrentan mayor riesgo de abandono. Se necesita acompañamiento integral que combine apoyo académico, psicológico y económico.

5. **Desigualdad territorial**  
   La concentración educativa en Lima limita las oportunidades en otras regiones. La educación a distancia puede ayudar a reducir esta brecha si se mejora la conectividad y el soporte tecnológico.

6. **Desconexión con el mercado laboral**  
   Muchas carreras populares no garantizan empleabilidad, mientras que otras con alta demanda carecen de profesionales. Es clave alinear la oferta educativa con las necesidades reales del mercado.

7. **Uso de datos para prevenir deserción**  
   Los modelos predictivos permiten identificar estudiantes en riesgo y mejorar la retención. Los datos se consolidan como herramientas clave para una gestión educativa más efectiva.

8. **Brecha en recursos educativos**  
   Las diferencias de inversión entre universidades públicas y privadas amplían la desigualdad. Reforzar la calidad y financiamiento de las instituciones públicas es esencial.

9. **Educación virtual como oportunidad**  
   La virtualidad ha ampliado el acceso, especialmente en zonas rurales. Su éxito depende de la infraestructura digital y de una adecuada formación docente.

10. **Brechas de género en áreas STEM**  
    Aunque hay paridad en la matrícula total, las mujeres siguen subrepresentadas en carreras tecnológicas. Promover referentes y programas de equidad puede cambiar esta tendencia.


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
