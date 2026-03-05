# LAB-2-Instrumentación | Monitoreo del Nivel de Estrés Mediante Respuesta Galvánica Cutánea (GSR)

## Introducción: 

La actividad electrodérmica (EDA, Electrodermal Activity) comprende los fenómenos eléctricos que ocurren en la piel relacionados con la variación de su conductancia. Esta propiedad cambia principalmente debido a la actividad del sistema nervioso simpático, el cual regula la sudoración. Cuando una persona experimenta estrés, emoción o esfuerzo cognitivo, aumenta la actividad de las glándulas sudoríparas, generando un incremento en la conductancia cutánea.

La respuesta galvánica cutánea (GSR, Galvanic Skin Response) se compone de dos elementos principales:

-Componente tónica (SCL – Skin Conductance Level): nivel basal de conductancia.

-Componente fásica (SCR – Skin Conductance Response): incrementos transitorios ante estímulos.

<img width="981" height="548" alt="image" src="https://github.com/user-attachments/assets/12233de7-40d1-49ad-a3ec-99a2523b97e8" />


Esta señal ha sido ampliamente utilizada en estudios de psicofisiología para evaluar estrés, carga cognitiva y respuestas emocionales. Sin embargo, aunque es un buen indicador autonómico, presenta limitaciones y no puede considerarse un método diagnóstico por sí solo.

## Objetivos

# Objetivo General

Diseñar, construir y validar un sistema vestible capaz de estimar cuantitativamente el nivel de estrés en un individuo sano mediante la medición continua de la respuesta galvánica cutánea (GSR).

# Objetivos Especificos

-Identificar y diferenciar las componentes estacionaria (SCL) y transitoria (SCR) de la señal de respuesta galvánica cutánea.

-Diseñar un sistema electrónico seguro que garantice que la corriente que atraviesa la piel del usuario sea menor a 1 mA bajo condiciones extremas.

-Implementar un sistema de adquisición, visualización y transmisión inalámbrica que permita clasificar el nivel de estrés durante la ejecución de tareas cognitivas.

## Marco teórico: 

La actividad electrodérmica (EDA, Electrodermal Activity) constituye una manifestación periférica directa de la activación del sistema nervioso autónomo, específicamente de su rama simpática. Desde finales del siglo XIX, estudios pioneros como los de Charles Féré y posteriormente Ivan Pavlov evidenciaron que los estados emocionales y los estímulos sensoriales generan modificaciones medibles en la conductancia eléctrica de la piel. Estas variaciones se deben principalmente a cambios en la actividad de las glándulas sudoríparas ecrinas, las cuales están densamente distribuidas en regiones como los dedos y la palma de la mano.

Desde el punto de vista fisiológico, la piel puede modelarse como un sistema eléctrico compuesto por resistencias y capacitancias distribuidas. La capa córnea actúa como un elemento resistivo dominante, mientras que el tejido subyacente y el contenido hídrico contribuyen a la conducción iónica. Cuando aumenta la actividad simpática, se incrementa la secreción de sudor, lo que reduce la resistencia cutánea y aumenta la conductancia (medida en microsiemens, µS). Este fenómeno es cuantificable mediante la Respuesta Galvánica Cutánea (GSR, Galvanic Skin Response).

La señal de GSR presenta dos componentes fundamentales:

-Componente tónica (SCL – Skin Conductance Level): representa el nivel basal de conductancia en ausencia de estímulos discretos. Refleja el estado general de activación autonómica del individuo.

-Componente fásica (SCR – Skin Conductance Response): corresponde a incrementos transitorios asociados a estímulos específicos o a eventos cognitivos y emocionales. Estas respuestas suelen presentar latencias entre 1 y 3 segundos posteriores al estímulo.

Desde la perspectiva bioeléctrica, la medición de GSR se realiza aplicando una corriente muy pequeña y controlada a través de la piel y registrando la variación de voltaje resultante, o bien utilizando un divisor resistivo que permita inferir cambios de conductancia. Para garantizar la seguridad del usuario, los niveles de corriente deben mantenerse por debajo de los umbrales establecidos por normas internacionales como la International Electrotechnical Commission, específicamente en la norma IEC 60479, la cual describe los efectos fisiológicos de la corriente eléctrica en el cuerpo humano.

En términos de procesamiento de señal, la GSR es una señal lenta, con contenido espectral predominante por debajo de 1 Hz. Por ello, su análisis requiere filtrado pasa-banda de baja frecuencia para eliminar deriva térmica y ruido de alta frecuencia. Además, la separación entre SCL y SCR puede abordarse mediante métodos de filtrado digital, modelado exponencial o técnicas de descomposición basadas en convolución.

Desde un enfoque psicofisiológico, la GSR es considerada un biomarcador indirecto de estrés y carga cognitiva. El estrés activa el eje hipotálamo–hipófisis–adrenal y simultáneamente incrementa la actividad simpática, produciendo respuestas sudomotoras detectables en la piel. Sin embargo, es fundamental reconocer que la GSR no discrimina entre tipos de emoción (miedo, ansiedad, sorpresa o excitación), sino que refleja únicamente el nivel de activación autonómica. Por tanto, su interpretación debe contextualizarse dentro del entorno experimental y, de ser posible, complementarse con otros indicadores fisiológicos como frecuencia cardíaca o variabilidad de la frecuencia cardíaca.

Finalmente, desde la perspectiva de la instrumentación biomédica, la medición de GSR implica la integración de principios de fisiología, bioelectricidad, electrónica analógica y procesamiento digital de señales. La correcta selección de electrodos, el control de impedancia de contacto, la limitación de corriente y el diseño de filtros determinan la calidad y confiabilidad de la señal obtenida. En consecuencia, el análisis de la respuesta galvánica cutánea constituye un ejercicio interdisciplinario que articula fundamentos biológicos con criterios de diseño electrónico seguro y robusto.
