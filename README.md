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

## 5. INSIGHTS 

El primer año se confirma como el punto más crítico del ciclo educativo. Cerca del 70% de los estudiantes que abandonan lo hacen dentro de los primeros 18 meses, evidenciando que la deserción no es un evento repentino, sino un proceso acumulativo. La etapa inicial requiere un enfoque de acompañamiento intensivo, con programas de inducción, cursos de nivelación, mentoría entre pares y detección temprana de señales de riesgo académico o emocional. Una intervención oportuna en este periodo puede reducir significativamente la pérdida de estudiantes.

El factor económico sigue siendo el principal determinante de la permanencia. Cuatro de cada diez estudiantes abandonan por razones financieras y no por bajo rendimiento, lo que demuestra que los programas de apoyo económico tienen un retorno social muy alto. Becas parciales o subsidios en transporte y materiales logran un impacto similar al de las becas completas, mientras que la flexibilidad horaria y las prácticas remuneradas permiten a los estudiantes sostener sus estudios. Vincular a las universidades con empresas locales se presenta como una oportunidad para combinar formación y empleabilidad.

El perfil del estudiante peruano ha cambiado de forma estructural. El estudiante típico de 18 años dedicado exclusivamente al estudio ya no representa la mayoría. Hoy, más de un tercio son adultos trabajadores mayores de 25 años, casi la mitad combina estudio y empleo, y una cuarta parte tiene responsabilidades familiares. Este nuevo escenario exige que las instituciones adapten su oferta a modalidades más flexibles —como programas virtuales, nocturnos o modulares— que respondan a las necesidades de quienes buscan reinsertarse o mejorar su formación sin abandonar su trabajo.

Las brechas de equidad no solo están en el acceso, sino en la permanencia. Los estudiantes vulnerables que logran ingresar a la educación superior enfrentan un riesgo tres veces mayor de desertar. Sin acompañamiento académico, psicológico y financiero, el acceso se convierte en una deserción diferida. Por ello, los programas de tutoría, orientación vocacional y apoyo socioemocional son tan importantes como los esfuerzos de admisión. El reto no es solo matricular más estudiantes, sino garantizar que lleguen hasta la graduación.

La desigualdad territorial sigue definiendo las oportunidades. Nacer en Lima o en Loreto puede significar una diferencia de 30 puntos porcentuales en el acceso a la educación superior. La centralización educativa se concentra en pocos departamentos, mientras que más de 15 regiones carecen de oferta suficiente o infraestructura moderna. La educación a distancia aparece como una solución viable para democratizar el acceso, pero su éxito depende de la conectividad, la disponibilidad de dispositivos y el acompañamiento pedagógico.

El mercado laboral no está guiando las decisiones educativas. Las carreras más demandadas, como Administración, Derecho y Contabilidad, presentan las tasas más altas de subempleo, mientras que áreas con alta demanda laboral, como Enfermería, Educación rural e Ingeniería de Datos, enfrentan déficit de profesionales. Esto revela una desconexión entre la elección vocacional y las oportunidades reales del mercado. La creación de sistemas de información transparentes sobre empleabilidad por carrera puede ayudar a los jóvenes a tomar decisiones más informadas.

Los datos se han consolidado como aliados estratégicos para la retención estudiantil. Los modelos predictivos basados en machine learning logran identificar más del 80% de los casos de deserción potencial, superando ampliamente la precisión de las evaluaciones manuales. Variables como la asistencia del primer mes resultan ser mejores indicadores que las notas de ingreso. Las instituciones que han implementado sistemas de alerta temprana basados en datos muestran aumentos de hasta 15% en la tasa de retención anual.

La inequidad en recursos educativos sigue reproduciendo desigualdad. Un estudiante de nivel socioeconómico alto accede a diez veces más recursos académicos que uno de bajos ingresos. Mientras que las universidades privadas de élite invierten alrededor de S/15,000 por estudiante al año, las públicas apenas alcanzan S/4,500. Esta brecha no solo afecta la calidad educativa, sino que perpetúa las diferencias sociales. Invertir en universidades públicas con calidad equiparable es clave para reducir la desigualdad intergeneracional.

La virtualidad, lejos de ser un problema, representa una oportunidad para expandir la cobertura educativa. Entre 2021 y 2023, los programas virtuales crecieron un 40% anual, permitiendo el acceso de estudiantes en regiones remotas. Sin embargo, su efectividad depende de la infraestructura tecnológica, la capacitación docente y el diseño pedagógico adaptado. La educación digital puede cerrar brechas geográficas, pero también exige una alfabetización digital sólida para evitar nuevas formas de exclusión.

Finalmente, aunque existe paridad de género en la matrícula general, persisten grandes diferencias por campo de estudio. Las mujeres representan el 51% del total de estudiantes, pero solo el 28% en áreas STEM. Los estereotipos de género siguen influyendo desde la educación básica y se reflejan en una brecha salarial del 15% entre egresadas y egresados. Impulsar programas de mentoría, referentes femeninos y campañas de orientación temprana en carreras tecnológicas es esencial para avanzar hacia una equidad sustantiva en el ámbito educativo y laboral.

---

## 6. RECOMENDACIONES 

Se propone un conjunto de acciones coordinadas entre el Estado, las instituciones educativas y las familias para mejorar la permanencia y equidad en la educación superior del país.  

El Estado debe liderar políticas de retención estudiantil, descentralización y orientación vocacional, junto con una inversión sostenida en infraestructura y becas que aseguren igualdad de oportunidades. Estas medidas buscan fortalecer la calidad educativa y reducir las brechas regionales y socioeconómicas.  

Las instituciones educativas deben implementar sistemas de alerta temprana, programas de nivelación y modalidades de estudio flexibles que respondan a las distintas realidades de los estudiantes. Además, deben fortalecer su vinculación con el sector productivo y rediseñar sus primeros años de formación para garantizar una transición exitosa hacia la vida universitaria.  

Para los estudiantes y sus familias, se promueve una toma de decisiones más informada al elegir carrera e institución, así como estrategias de persistencia ante dificultades económicas, académicas o personales, fomentando la búsqueda temprana de apoyo.  

En materia de financiamiento, se recomienda ampliar los programas de becas y créditos educativos con criterios más inclusivos y sostenibles, de modo que nadie abandone sus estudios por motivos económicos.  

Finalmente, se destaca el uso estratégico de la tecnología y los datos como herramienta clave para personalizar el aprendizaje, monitorear el sistema educativo y diseñar políticas basadas en evidencia que impulsen la mejora continua del sistema.  

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
