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

## 4. PRINCIPALES HALLAZGOS

Entre 2019 y 2023, la matrícula educativa en el Perú mostró una fuerte contracción durante la pandemia, con caídas de entre 8% y 12% en 2020, especialmente en educación inicial, mientras que la educación superior demostró resiliencia gracias a la virtualidad, creciendo cerca del 2% anual. Aunque el sistema ha mostrado recuperación sostenida desde 2022, los niveles actuales aún se mantienen un 5% por debajo de los registrados antes del COVID-19. Este contexto evidencia la necesidad de estrategias de reincorporación y recuperación de aprendizajes para los estudiantes que abandonaron el sistema educativo.

El crecimiento reciente ha sido desigual entre niveles. La educación superior experimentó un incremento de 18%, impulsado por la expansión de universidades privadas y modalidades flexibles, mientras que la educación secundaria permanece estancada, con una caída del 2% producto de la deserción no recuperada. En contraste, la educación primaria registró un leve aumento del 3%, y la educación inicial continúa rezagada, con un descenso del 5% tras la pandemia. Además, el sector privado ha tenido una expansión significativa, con un crecimiento del 25% frente al 8% del sector público, alcanzando el 76% de participación en educación superior, lo que genera preocupación por el aumento de las desigualdades educativas entre distintos estratos socioeconómicos.

La matrícula presenta una fuerte concentración geográfica: Lima Metropolitana concentra el 42% de los estudiantes universitarios, y solo cinco departamentos (Lima, Arequipa, La Libertad, Piura y Cusco) agrupan el 68% de la matrícula total, mientras que los 20 restantes comparten apenas el 32%. Esto refleja una centralización educativa pronunciada y una migración constante de jóvenes hacia las regiones con mayor oferta, generando impactos sociales y económicos en sus lugares de origen.

En cuanto al perfil del estudiante, se observa una leve paridad de género en los niveles básico y superior, aunque persisten brechas marcadas en carreras STEM, donde los hombres representan más del 70% de los matriculados. En contraste, áreas como educación y salud mantienen predominio femenino. Un cuarto de los estudiantes se encuentra en situación de pobreza, casi la mitad trabaja mientras estudia y más del 70% pertenece a niveles socioeconómicos medios o bajos, lo que incrementa hasta tres veces el riesgo de abandono por causas económicas. Asimismo, solo el 12% de los universitarios proviene de zonas rurales, lo que revela una brecha urbano-rural crítica en el acceso a la educación superior.

La deserción continúa siendo un desafío estructural. En 2023, la tasa nacional alcanzó el 18.5%, con un 28% de abandono en el primer año universitario y un total acumulado cercano al 40% de estudiantes que no completan sus estudios. Los principales factores asociados al riesgo de deserción incluyen bajo rendimiento académico en el primer ciclo, dificultades económicas familiares, baja asistencia y procedencia de colegios públicos rurales. Se estima que cerca del 23% de los estudiantes actuales están en riesgo alto de abandono, especialmente quienes trabajan a tiempo completo o pertenecen a los estratos socioeconómicos más bajos.

Respecto a la demanda educativa, las carreras más populares en 2023 fueron Administración, Derecho, Contabilidad, Educación e Ingeniería de Sistemas, que en conjunto concentraron más del 50% de la matrícula total. Sin embargo, estas áreas presentan altos niveles de saturación laboral. Por el contrario, se identifican déficits importantes en Enfermería, Educación rural, Ingeniería de Datos e Inteligencia Artificial, y carreras vinculadas a sostenibilidad ambiental. Además, las carreras tecnológicas y digitales —como Ciencia de Datos, Ciberseguridad, UX/UI y Marketing Digital— muestran crecimientos superiores al 30%, evidenciando un cambio estructural en las preferencias de los estudiantes y en las demandas del mercado laboral.

En el plano territorial, las desigualdades son marcadas. Lima, Arequipa, Ica, Moquegua y Tacna presentan las mayores tasas de cobertura en educación superior, mientras que regiones como Loreto, Ucayali, Apurímac y Huancavelica registran los niveles más bajos, con brechas de hasta 30 puntos porcentuales. La infraestructura educativa sigue siendo insuficiente, especialmente en zonas rurales, donde el 78% de los distritos carece de instituciones de educación superior cercanas y el 45% no dispone de conectividad adecuada. Para cerrar esta brecha, se estima necesaria una inversión de al menos S/ 2,500 millones en los próximos años.

Finalmente, el ratio estudiante-docente promedia 18 por cada profesor, dentro del rango aceptable según estándares internacionales, aunque en zonas rurales asciende a 28:1, lo que refleja un déficit docente estimado en 15,000 profesores. Estas evidencias confirman que el sistema educativo peruano enfrenta un doble desafío: mejorar la equidad territorial y socioeconómica, y adaptar su oferta formativa a las transformaciones tecnológicas y laborales emergentes.

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
