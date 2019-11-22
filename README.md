Documento Completo en: https://github.com/ricnef2121/ceneval/blob/master/Estudio/Proyecto_Ceneval.pdf

## Saturdays.IA

# CENEVAL Approval Prediction

## Predicción de Aprobación del Examen CENEVAL-EGEL

###### Sepúlveda-García Stephany, Gatica-Martínez Jessica, García-Dueñas Pamela Zoe, Mejía-Blanco Erick & Lazcano-Calixto Ricardo Neftali

#### Eje Vertical: Educación

#### Líder del proyecto técnico: Hernandez-Mota, Rodrigo

## Resumen

En el presente documento se muestra el modelo de Machine Learning, Random forest para determinar cuáles variables influyen en que un estudiante apruebe el Examen para el Egreso de la Licenciatura EGEL, así como la probabilidad de que el alumno apruebe el examen. Se encontró que las variables más importantes son: centro universitario, el tipo de examen y el promedio, la edad, cantidad de libros que tienen, la escolaridad de sus padres, cuántos cuartos y cuántas personas viven en su casa, hasta cual es el nivel de estudios al que los padres del estudiante deseaban que este llegara, además del conjunto de variables relacionadas con la vida laboral del estudiante. De los cuatro modelos probados Random Forest fue el más eficiente, ya que puede predecir correctamente el 71.4% de los casos, si un estudiante aprobará o no el examen con un 95% de confianza.

## Planteamiento del problema

Una de las dificultades que enfrentan las universidades es la titulación de los estudiantes, existe una brecha entre el periodo de egreso de los alumnos y la adquisición del grado de los mismos, ya que actualmente no es necesario contar con un título universitario para ejercer como profesionista. Rodríguez Betanzos (2014) señala que los universitarios titulados son personas que cuentan con mejores oportunidades para incursionar de manera más estable en el campo laboral. Así mismo señala que la eficiencia terminal y el índice de titulación permiten observar los niveles de deficiencia que tienen las universidades.Además expone que la rigidez de los mecanismos de titulación provoca que los estudiantes se desincentiven para titularse (López, Salvo y García, 1989).

De acuerdo con la Asociación Nacional de Universidades e Instituciones de Educación Superior (ANUIES), del total de jóvenes que ingresan a la educación superior en México, sólo el 50% logra titularse. El bajo índice de titulación es un tema de de interés para las universidades en México, pues omitir el proceso de titulación al egresar de un programa educativo no permite a las instituciones evaluar integralmente al egresado, ni a éste concluir con su formación académica (Martínez, 2015), (Vargas Pureko & Rivera Michelena 2006).

Otro de los factores a considerar es la calidad de la educación media superior, en esta incertidumbre es en la que surge CENEVAL (Gago, 2000), ya que es un organismo dedicado al diseño y aplicación de instrumentos de evaluación de conocimientos, habilidades y competencias de los estudiantes de las Instituciones de Educación Superior (IES) en México (CENEVAL, 2019).

La dificultad de los procesos de titulación aunado a un organismo dedicado a la evaluación de la educación externo a las universidades provocó que aprobar el examen CENEVAL-EGEL se haya convertido en una de las opciones de titulación en los centros educativos de la Universidad de Guadalajara. Los alumnos que optan por esta modalidad tienen un 50% de probabilidad de acreditar el examen.

Sin embargo, CENEVAL mide únicamente los conocimientos, habilidades y capacidades de los estudiantes, no obstante, que un estudiante se titule, no sólo depende de factores académicos, sino de factores intrínsecos al estudiante y su entorno, como su contexto social, familiar y económico. También se deben a otros factores que tienen que ver con la institución y todos los componentes del proceso educativo durante la trayectoria académica de alumno.

Encontrar las causas de este bajo rendimiento en la titulación nos podría ayudar a plantear estrategias que permitan el incremento en la acreditación del examen CENEVAL-EGEL

Problemática: Identificación de las variables de factores académicos, personales y socioeconómicos que influyen para que un alumno acredite el examen CENEVAL- EGEL mediante la aplicación de machine learning. Los resultados ayudarán a diseñar estrategias que incrementen la acreditación, por tanto, la titulación de los alumnos.

## Descripción de la solución a la problemática detectada.

Se determinará el patrón de características que tiene un estudiante que aprueba el examen y se establecerá el grado de incidencia en que cada una de las variables independientes influyen y explican la acreditación de este.

## Hipótesis

El contexto socioeconómico del alumno tiene relación con la acreditación del examen CENEVAL-EGEL.

## Marco Teórico

La calidad de la educación es un tema primordial para cualquier institución educativa. Las universidades buscan acreditar sus programas académicos y que sus estudiantes alcancen estándares nacionales e internacionales de conocimientos. Existen diversas instituciones evaluadoras y acreditadoras en el país y una de ellas es el Centro Nacional de Evaluación para la Educación Superior (CENEVAL). CENEVAL es una asociación que realiza exámenes para evaluar los conocimientos de los egresados de todas las Universidades públicas del país, y de hecho otorga reconocimientos a las universidades en las cuales la mayoría de sus alumnos obtienen un resultado satisfactorio en el examen. Los estudiantes de licenciatura de México realizan el Examen General de Egreso de la Licenciatura EGEL, en la mayoría de los casos para obtener su titulación, debido a que este es un requisito para titularse o una forma para hacerlo.

Dichos exámenes son elaborados por profesores de todo el país y forman un excelente referente de los conocimientos de los estudiantes, aunque para poder tener una calificación aprobatoria en el mismo los conocimientos teóricos no son suficientes. Además, existen una serie de variables que influyen en que un alumno logre alcanzar un testimonio satisfactorio, como género, estado laboral, entre otras (Tinto, V., 1992).

En el año 2017 (Gonzalez-Marron, D., Enciso-Gonzalez, A., Hernandez-Gonzalez,.., A., 2017) realizaron un estudio “Evaluación de parámetros de encuesta de ingreso del CENEVAL para alumnos candidatos a ingresar al nivel superior, caso de estudio ITP”, en el cual evalúan las variables socioeconómicas del examen de Ceneval EXANI-II, analizaron los datos para los aspirantes a las licenciaturas de arquitectura, administración e ingenierías, estandarizaron los datos comunes en todas las encuestas, encontraron 23 atributos, los pasos que usaron el proyecto fue una reducción de dimensiones con PCA y como modelos de clasificación de datos nominales y regresión de datos numéricos, encontraron tres variables que determinan el desempeño de un estudiante; el promedio de bachillerato, el número de libros en casa, cantidad de horas de trabajo y la escolaridad del padre y de la madre.

En 2012 (Vera, C. M., Morales, C. R., & Soto, S. V., 2012) realizaron un estudio llamado “Predicción del Fracaso Escolar mediante Técnicas de Minería de Datos” en dicho estudio los autores pretenden encontrar los componentes socioeconómicos que influyen en el fracaso escolar de los estudiantes, suspendan o abandonen la escuela, realizaron una reducción de dimensiones con 10 algoritmos distintos, para quedarse con 15 atributos determinantes para su modelo, y utilizaron algoritmos de clasificación como árboles de decisión, encontraron que los árboles de decisión Prism permiten conocer a los alumnos que tienen mayor probabilidad de abandonar la escuela con un 99.8% de confianza.

Documento completo en: https://github.com/ricnef2121/ceneval/blob/master/Estudio/Proyecto_Ceneval.pdf
