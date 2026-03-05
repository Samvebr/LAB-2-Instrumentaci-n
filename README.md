# LAB-2-Instrumentación | Monitoreo del Nivel de Estrés Mediante Respuesta Galvánica Cutánea (GSR)

- Daniel Espinosa
- Samuel Velandia
  
## Introducción: 

La actividad electrodérmica (EDA, Electrodermal Activity) comprende los fenómenos eléctricos que ocurren en la piel relacionados con la variación de su conductancia. Esta propiedad cambia principalmente debido a la actividad del sistema nervioso simpático, el cual regula la sudoración. Cuando una persona experimenta estrés, emoción o esfuerzo cognitivo, aumenta la actividad de las glándulas sudoríparas, generando un incremento en la conductancia cutánea.

La respuesta galvánica cutánea (GSR, Galvanic Skin Response) se compone de dos elementos principales:

-Componente tónica (SCL – Skin Conductance Level): nivel basal de conductancia.

-Componente fásica (SCR – Skin Conductance Response): incrementos transitorios ante estímulos.

<img width="981" height="548" alt="image" src="https://github.com/user-attachments/assets/12233de7-40d1-49ad-a3ec-99a2523b97e8" />


Esta señal ha sido ampliamente utilizada en estudios de psicofisiología para evaluar estrés, carga cognitiva y respuestas emocionales. Sin embargo, aunque es un buen indicador autonómico, presenta limitaciones y no puede considerarse un método diagnóstico por sí solo.

# Objetivos

##  Objetivo General

Diseñar, construir y validar un sistema vestible capaz de estimar cuantitativamente el nivel de estrés en un individuo sano mediante la medición continua de la respuesta galvánica cutánea (GSR).

## Objetivos Especificos

- Identificar y diferenciar las componentes estacionaria (SCL) y transitoria (SCR) de la señal de respuesta galvánica cutánea.

- Diseñar un sistema electrónico seguro que garantice que la corriente que atraviesa la piel del usuario sea menor a 1 mA bajo condiciones extremas.

- Implementar un sistema de adquisición, visualización y transmisión inalámbrica que permita clasificar el nivel de estrés durante la ejecución de tareas cognitivas.

# Materiales  y procedimiento 

## Materiales: 
- Generador de señales biológicas

- Osciloscopio digital

- Fuente de voltaje DC

- Computador con acceso a Internet

- MATLAB

- Arduino UNO o Arduino Nano

- Regleta de Proto-Board

- Cables UTP

- Resistencia de 68 kΩ

- Condensador de 1 µF

- 2 Electrodos Ag-AgCl o placas metálicas inertes

- Cintas de velcro

## Procedimiento: 

- Parte A
  
En la primera etapa de la práctica se realiza una revisión de la literatura científica relacionada con la actividad electrodérmica (EDA) y la respuesta galvánica cutánea (GSR), con el fin de comprender los fundamentos fisiológicos y eléctricos que permiten utilizar esta señal como indicador de activación del sistema nervioso autónomo. Paralelamente, se investigan los efectos fisiológicos de las corrientes eléctricas directas y alternas sobre el cuerpo humano, tomando como referencia los lineamientos establecidos por la International Electrotechnical Commission en la norma IEC 60479.

Posteriormente, se realizan los cálculos necesarios para garantizar la seguridad del usuario. Para ello se considera un rango de alimentación entre 3.3 V y 5 V y se analiza el caso extremo en el que la resistencia de la piel es equivalente a un cortocircuito (R_skin = 0 Ω). A partir de estas condiciones se dimensionan los componentes del circuito, especialmente la resistencia limitadora, de forma que la corriente máxima que atraviese la piel sea inferior a 1 mA. Finalmente, con base en estos cálculos se diseña el circuito del dispositivo vestible encargado de capturar las variaciones de la GSR y transmitirlas de manera alámbrica a un computador. En esta etapa también se define la región anatómica donde se ubicarán los electrodos, procurando seleccionar zonas con alta densidad de glándulas sudoríparas y mínima interferencia por movimiento, como los dedos de la mano.

- Parte B
  
En la segunda etapa se procede a la construcción física del sistema diseñado, utilizando una plataforma de prototipado electrónico y un microcontrolador para la adquisición de la señal. Una vez ensamblado el circuito y conectados los electrodos al sujeto de prueba, se realiza la captura de la señal GSR en tiempo real y se visualiza su comportamiento mediante el computador. Durante esta fase se evalúa la estabilidad del sistema frente a diferentes condiciones de movimiento del sujeto, como caminar, escribir o mover las manos, con el objetivo de identificar posibles fuentes de ruido o interferencia.

Posteriormente se realiza una prueba fisiológica controlada en la que el sujeto permanece sentado y en reposo. En este estado se le solicita realizar una inspiración profunda seguida de una exhalación lenta. Durante este proceso se registra la variación de la conductancia cutánea, la cual normalmente presenta un incremento notable seguido de un retorno gradual al nivel basal. Con base en los valores máximo y mínimo obtenidos durante estas mediciones se establecen umbrales que permitan clasificar el nivel de estrés percibido en categorías como bajo, moderado o elevado. Finalmente, se realizan las modificaciones necesarias en el sistema para permitir la transmisión inalámbrica de la información hacia un computador o dispositivo móvil, de manera que el sistema pueda emitir alertas o mensajes indicando el nivel estimado de estrés del usuario.

- Parte C
  
En la etapa final de la práctica se utiliza el dispositivo desarrollado para monitorear el nivel de estrés de un sujeto mientras realiza actividades que requieren concentración y esfuerzo mental. Para ello, el sujeto de prueba utiliza el dispositivo vestible mientras resuelve un conjunto breve de problemas o un examen corto. Durante la realización de esta tarea se registran continuamente las variaciones de la señal GSR y el sistema procesa la información para determinar el nivel de estrés estimado en tiempo real.

Los resultados obtenidos se analizan observando la relación entre el incremento de la actividad cognitiva y los cambios en la conductancia cutánea. Finalmente, se documenta todo el procedimiento experimental, incluyendo el diseño del sistema, los cálculos realizados, la construcción del dispositivo, las pruebas realizadas y los resultados obtenidos. Esta información se organiza en un repositorio en GitHub que incluya el código, las gráficas de la señal adquirida, el análisis de resultados y las conclusiones de la práctica.

## Justifiación Biológica: 

La colocación de un sensor de respuesta galvánica de la piel (SGR) en las palmas de los dedos se justifica biológicamente porque esta zona posee una de las mayores densidades de glándulas sudoríparas ecrinas del cuerpo humano, las cuales están directamente inervadas por el sistema nervioso simpático. A diferencia de otras regiones cutáneas, las palmas presentan una alta actividad sudomotora incluso ante estímulos emocionales o cognitivos leves, lo que genera variaciones detectables en la conductancia eléctrica de la piel. Estas variaciones se producen porque el sudor, al contener electrolitos, modifica la resistencia eléctrica superficial cuando aumenta la activación autonómica. Por ello, al ubicar el SGR en los dedos se obtiene una señal más sensible, rápida y confiable de los cambios fisiológicos asociados al estrés, la atención o la respuesta emocional, lo que convierte a esta región en un sitio anatómicamente óptimo para la medición.

<img width="690" height="431" alt="image" src="https://github.com/user-attachments/assets/aeca7b4a-03e8-490c-acc7-86835d27b24e" />


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

<img width="372" height="241" alt="image" src="https://github.com/user-attachments/assets/d415b7ff-74b3-49b8-a126-d439f5f3faa6" />

## Código de MATLAB 

```bash 
clc;
clear;
close all;


Fs = 100;   % Frecuencia de muestreo [Hz]

answer = inputdlg("Ingrese el tiempo de adquisición (s):", ...
                  "Tiempo de adquisición", 1, {"30"});
if isempty(answer)
    error("Adquisición cancelada");
end

T = str2double(answer{1});
if isnan(T) || T <= 0
    error("Tiempo inválido");
end

N = Fs * T;


% ===== FILTRO GSR PASA-BAJO 1 Hz =====
f_cut = 1;   % Hz
[b,a] = butter(2, f_cut/(Fs/2), 'low');
zf = zeros(max(length(a),length(b))-1,1);
% ======================================


puerto = "COM3";
baud   = 115200;

s = serialport(puerto, baud);
configureTerminator(s,"LF");
flush(s);
pause(2);

disp("Iniciando adquisición...");

resp_raw = zeros(N,1);
resp_f   = zeros(N,1);
t        = (0:N-1)/Fs;

k = 1;


figure;

h1 = animatedline('Color','r','LineWidth',0.8);
h2 = animatedline('Color','b','LineWidth',1.5);

xlabel("Tiempo [s]");
ylabel("Señal GSR [V]");
title("Señal GSR cruda y filtrada (Lowpass 1 Hz)");
legend("Cruda","Filtrada (1 Hz)");
grid on;
xlim([0 T]);


while k <= N

    linea = readline(s);              
    linea = strtrim(linea);           

    nums = regexp(linea, '[-+]?\d*\.?\d+', 'match');

    if isempty(nums)
        continue                      
    end

    y = str2double(nums{1});

    if isnan(y)
        continue
    end

    resp_raw(k) = y;

    [yf, zf] = filter(b, a, y, zf);
    resp_f(k) = yf;

    % ===== IGNORAR VOLTAJES MAYORES A 1V EN LA GRÁFICA =====
    if abs(y) <= 1
        addpoints(h1, t(k), y);
    end

    if abs(yf) <= 1
        addpoints(h2, t(k), yf);
    end
    % ========================================================

    if mod(k,5) == 0
        drawnow limitrate
    end

    k = k + 1;
end

disp("Adquisición finalizada.");
clear s


filename = sprintf("senal_GSR_filtrada_%ds.mat", round(T));
save(filename, "t", "resp_raw", "resp_f", "Fs");

disp("Archivo guardado:");
disp(filename);
```

Con este código de MATLAB pudimos adquirir, filtrar, visualizar y guardar una señal de respuesta galvánica cutánea (GSR) proveniente de un microcontrolador (por ejemplo un Arduino) a través del puerto serial. Al inicio se limpian las variables, la consola y las figuras abiertas (clc, clear, close all). Luego se define la frecuencia de muestreo en 100 Hz y se le pide al usuario ingresar el tiempo de adquisición mediante una ventana de diálogo. Con estos valores se calcula el número total de muestras que se deben capturar (N = Fs*T). Después se diseña un filtro digital Butterworth pasa-bajo de segundo orden con frecuencia de corte de 1 Hz, adecuado para señales GSR porque estas varían lentamente y su contenido espectral está por debajo de esa frecuencia. También se inicializan variables para almacenar la señal cruda, la señal filtrada y el vector de tiempo.

Posteriormente el programa configura la comunicación serial con el dispositivo externo (por ejemplo un Arduino) usando el puerto COM3 y una velocidad de 115200 baudios. Dentro de un ciclo while, el script lee continuamente las líneas que llegan por el puerto serial, extrae el número contenido en cada línea y lo convierte a valor numérico. Cada muestra se almacena como señal cruda y luego se procesa con el filtro digital para obtener la señal filtrada. Ambas señales se van graficando en tiempo real utilizando animatedline, donde la roja representa la señal original y la azul la señal filtrada. Para evitar saturaciones o errores de visualización, el código ignora valores de voltaje mayores a ±1 V al momento de graficar. Finalmente, cuando se completan todas las muestras, el programa cierra la comunicación serial y guarda los datos adquiridos (tiempo, señal cruda, señal filtrada y frecuencia de muestreo) en un archivo .mat para su posterior análisis.

## Gráficas

## Analísis

## Conclusiones 

## Preguntas a discutir
 
 

 - 1. ¿A qué se debe que una inspiración profunda incremente la magnitud de la respuesta galvánica cutánea (GSR)?

Una inspiración profunda genera activación transitoria del sistema nervioso autónomo, particularmente del sistema simpático. Este aumento simpático estimula las glándulas sudoríparas ecrinas, incrementando la secreción de sudor y reduciendo la resistencia cutánea. Como consecuencia, aumenta la conductancia de la piel (SCL) y se produce una respuesta transitoria (SCR). Posteriormente, el sistema retorna gradualmente a su estado basal debido a mecanismos de regulación homeostática.

 - 2. ¿Cuáles serían las ventajas y desventajas de utilizar la GSR como indicador de estrés?
  
  - Ventajas

Método no invasivo.

Fácil implementación electrónica.

Alta sensibilidad a cambios autonómicos.

Bajo costo.

Respuesta rápida ante estímulos emocionales o cognitivos.

  - Desventajas

No discrimina tipo de emoción (miedo, ansiedad, excitación).

Sensible a temperatura ambiental y movimiento.

Alta variabilidad interindividual.

Puede verse afectada por sudoración térmica no relacionada con estrés.

No es una herramienta diagnóstica clínica por sí sola.

## Referencias 


- Boucsein, W. (2012). Electrodermal activity (2nd ed.). Springer. https://doi.org/10.1007/978-1-4614-1126-0

- Dawson, M. E., Schell, A. M., & Filion, D. L. (2017). The electrodermal system. En J. T. Cacioppo, L. G. Tassinary, & G. G. Berntson (Eds.), Handbook of psychophysiology (4th ed., pp. 217–243). Cambridge University Press.

- Benedek, M., & Kaernbach, C. (2010). A continuous measure of phasic electrodermal activity. Journal of Neuroscience Methods, 190(1), 80–91. https://doi.org/10.1016/j.jneumeth.2010.04.028

- Posada-Quintero, H. F., & Chon, K. H. (2020). Innovations in electrodermal activity data collection and signal processing: A systematic review. Sensors, 20(2), 479. https://doi.org/10.3390/s20020479

- International Electrotechnical Commission. (2018). IEC 60479-1: Effects of current on human beings and livestock – Part 1: General aspects. IEC.

- Cacioppo, J. T., Tassinary, L. G., & Berntson, G. G. (2017). Handbook of psychophysiology (4th ed.). Cambridge University Press.

- Critchley, H. D. (2002). Electrodermal responses: What happens in the brain. The Neuroscientist, 8(2), 132–142. https://doi.org/10.1177/107385840200800209
