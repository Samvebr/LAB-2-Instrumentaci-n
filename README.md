# LAB-2-Instrumentación | Monitoreo del Nivel de Estrés Mediante Respuesta Galvánica Cutánea (GSR)

- Daniel Espinosa 5600778
- Samuel Velandia 5600777
  
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

La selección de las palmas de los dedos como sitio anatómico para la medición de la respuesta galvánica de la piel (GSR) se fundamenta en características fisiológicas y neuroanatómicas propias de esta región. Las palmas y las superficies plantares del cuerpo humano presentan una de las mayores concentraciones de glándulas sudoríparas ecrinas, estructuras especializadas en la regulación de la sudoración y estrechamente vinculadas con la actividad del sistema nervioso autónomo. Estas glándulas están principalmente inervadas por fibras del sistema nervioso simpático, lo que permite que respondan de manera rápida ante cambios en el estado fisiológico o emocional del organismo. De acuerdo con investigaciones en fisiología cutánea, “las glándulas sudoríparas ecrinas de las palmas y plantas presentan una densidad significativamente mayor que en otras regiones del cuerpo y están altamente controladas por la actividad simpática” (Boucsein, 2012).

Desde el punto de vista funcional, la sudoración palmar no se relaciona únicamente con procesos termorregulatorios, sino también con respuestas psicofisiológicas asociadas a procesos cognitivos y emocionales. Diversos estudios en psicofisiología han demostrado que estímulos relacionados con la atención, la sorpresa, la carga cognitiva o el estrés generan activación simpática que se manifiesta como un incremento en la secreción sudomotora en estas regiones. En consecuencia, las variaciones en la conductancia eléctrica de la piel se convierten en un indicador fisiológico indirecto de la activación autonómica. Tal como señalan estudios clásicos en psicofisiología, “los cambios en la conductancia cutánea reflejan directamente la actividad del sistema nervioso simpático a través de la modulación de la actividad sudomotora” (Dawson, Schell & Filion, 2017).

Desde una perspectiva bioeléctrica, el sudor secretado por las glándulas ecrinas contiene electrolitos disueltos, principalmente sodio y cloruro, lo que modifica las propiedades eléctricas de la piel. Cuando aumenta la secreción de sudor, disminuye la resistencia eléctrica superficial y aumenta la conductancia cutánea. Este fenómeno permite registrar variaciones en la actividad fisiológica mediante sensores eléctricos colocados sobre la superficie de la piel. En este sentido, se ha establecido que “la presencia de electrolitos en el sudor reduce la impedancia de la piel y facilita la conducción eléctrica a través de la superficie cutánea” (Geddes & Baker, 1989).

Por lo tanto, la ubicación del sensor de GSR en las yemas o superficies palmares de los dedos permite obtener señales de mayor amplitud y sensibilidad en comparación con otras zonas corporales con menor densidad de glándulas sudoríparas. Esta característica convierte a los dedos en un sitio anatómicamente óptimo para la medición de la actividad electrodérmica, especialmente en estudios de instrumentación biomédica y psicofisiología experimental.

<img width="690" height="431" alt="image" src="https://github.com/user-attachments/assets/aeca7b4a-03e8-490c-acc7-86835d27b24e" />


## Marco teórico: 

La actividad electrodérmica (EDA, Electrodermal Activity) constituye una de las manifestaciones periféricas más ampliamente estudiadas de la activación del sistema nervioso autónomo, particularmente de su componente simpático. Desde finales del siglo XIX, investigadores como Charles Féré y posteriormente Ivan Pavlov observaron que los estados emocionales y ciertos estímulos sensoriales provocaban cambios medibles en las propiedades eléctricas de la piel. Estos descubrimientos sentaron las bases de lo que posteriormente se conocería como respuesta galvánica de la piel. En la literatura científica se reconoce que “la actividad electrodérmica representa una medida directa de la actividad simpática asociada a la función de las glándulas sudoríparas ecrinas” (Boucsein, 2012).

Desde una perspectiva fisiológica, la piel puede modelarse como un sistema bioeléctrico complejo que combina elementos resistivos y capacitivos distribuidos en sus diferentes capas. La capa córnea, que corresponde al estrato más externo de la epidermis, actúa como el principal componente resistivo del sistema, mientras que las capas subyacentes y el contenido hídrico de los tejidos contribuyen a la conducción iónica. Cuando se incrementa la actividad simpática, aumenta la secreción de sudor hacia los conductos de las glándulas ecrinas, lo que genera una reducción en la resistencia eléctrica de la piel y, por consiguiente, un aumento en su conductancia. Según estudios de bioinstrumentación, “los cambios en la hidratación de la capa córnea modifican significativamente la impedancia eléctrica de la piel y permiten la detección de respuestas sudomotoras” (Geddes & Baker, 1989).

La señal obtenida mediante la medición de la conductancia cutánea se compone generalmente de dos elementos principales: el componente tónico y el componente fásico. El componente tónico, conocido como Skin Conductance Level (SCL), representa el nivel basal de conductancia de la piel en ausencia de estímulos discretos y se asocia con el estado general de activación autonómica del individuo. Por otro lado, el componente fásico, denominado Skin Conductance Response (SCR), corresponde a cambios transitorios en la conductancia que ocurren en respuesta a estímulos específicos o eventos cognitivos y emocionales. En estudios psicofisiológicos se ha documentado que “las respuestas fásicas de conductancia cutánea presentan típicamente latencias de uno a tres segundos después de la presentación del estímulo” (Dawson et al., 2017).

Desde el punto de vista de la instrumentación biomédica, la medición de la GSR se realiza aplicando una corriente eléctrica de muy baja intensidad a través de la piel y midiendo las variaciones de voltaje o resistencia resultantes. Este proceso puede implementarse mediante circuitos de divisor resistivo, puentes de medición o amplificadores de instrumentación diseñados para detectar pequeñas variaciones de impedancia. Debido a que el cuerpo humano forma parte del circuito eléctrico durante la medición, es fundamental garantizar condiciones seguras de operación. En este contexto, normas internacionales establecen límites de corriente para evitar efectos fisiológicos adversos. Por ejemplo, la norma IEC establece que “los efectos fisiológicos de la corriente eléctrica en el cuerpo humano dependen de la intensidad, duración y trayectoria de la corriente” (International Electrotechnical Commission, 2018).

En cuanto al procesamiento de señal, la actividad electrodérmica presenta características de señal lenta, con la mayor parte de su contenido espectral concentrado en frecuencias inferiores a 1 Hz. Debido a ello, el análisis de esta señal suele requerir técnicas de filtrado digital de baja frecuencia que permitan eliminar ruido de alta frecuencia, interferencias eléctricas o artefactos de movimiento. Investigaciones en procesamiento de señales fisiológicas señalan que “la señal de conductancia cutánea posee componentes de muy baja frecuencia, por lo que es común aplicar filtros pasa-bajo cercanos a 1 Hz para su análisis” (Benedek & Kaernbach, 2010).

Desde la perspectiva de la psicofisiología, la GSR es considerada un biomarcador indirecto del nivel de activación autonómica y de la carga emocional o cognitiva del individuo. Situaciones que generan estrés o alta demanda cognitiva activan el sistema nervioso simpático, lo que produce respuestas sudomotoras detectables en la piel. Sin embargo, es importante señalar que esta señal no discrimina entre tipos específicos de emoción. En otras palabras, la GSR refleja la intensidad de la activación fisiológica, pero no identifica la valencia emocional asociada al estímulo. Por esta razón, se reconoce que “la actividad electrodérmica indica el nivel de activación fisiológica, pero no permite diferenciar entre emociones positivas o negativas” (Dawson et al., 2017).

Finalmente, desde el campo de la instrumentación biomédica, la medición de la respuesta galvánica cutánea representa un ejemplo claro de integración interdisciplinaria entre fisiología humana, bioelectricidad, electrónica analógica y procesamiento digital de señales. Factores como la selección de electrodos, la impedancia de contacto piel-electrodo, la estabilidad del circuito de medición y el diseño de filtros determinan la calidad de la señal obtenida. En consecuencia, el análisis de la actividad electrodérmica no solo permite estudiar fenómenos psicofisiológicos, sino que también constituye un ejercicio práctico en el diseño de sistemas de medición biomédica seguros y confiables.

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

Una inspiración profunda produce una activación transitoria del sistema nervioso autónomo que modifica la actividad de múltiples variables fisiológicas, entre ellas la actividad electrodérmica. Durante una inhalación profunda se genera un estímulo fisiológico que altera momentáneamente el equilibrio entre las ramas simpática y parasimpática del sistema nervioso autónomo. Este cambio se asocia con un incremento en la actividad simpática, lo que provoca una mayor estimulación de las glándulas sudoríparas ecrinas localizadas principalmente en las palmas de las manos y los dedos. Como consecuencia de esta activación sudomotora, aumenta la secreción de sudor hacia la superficie cutánea. Debido a que el sudor contiene electrolitos, su presencia disminuye la resistencia eléctrica de la piel y aumenta su conductancia, fenómeno que se registra como un incremento en la señal de respuesta galvánica cutánea (GSR).

Desde el punto de vista de la actividad electrodérmica, este fenómeno se manifiesta principalmente como una respuesta fásica de conductancia cutánea (SCR) superpuesta al nivel basal de conductancia o Skin Conductance Level (SCL). La inspiración profunda actúa como un estímulo fisiológico que desencadena una respuesta sudomotora breve, generando un aumento transitorio en la conductancia de la piel que suele presentarse con una latencia de aproximadamente 1 a 3 segundos. Posteriormente, cuando la estimulación simpática disminuye y el sistema nervioso autónomo recupera su equilibrio, la secreción sudorípara se reduce progresivamente y la conductancia cutánea retorna gradualmente a su nivel basal. Este comportamiento refleja los mecanismos normales de regulación homeostática del organismo y explica por qué la GSR es sensible tanto a estímulos emocionales como a cambios fisiológicos asociados a la respiración profunda.

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
  
