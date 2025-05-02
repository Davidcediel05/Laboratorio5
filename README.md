# Laboratorio 5 Procesamiento digital de señales
## Variabilidad de la Frecuencia Cardiaca usando la Transformada Wavelet.
### Descripcion 
<p>
En este proyecto se busca analizar las fluctuaciones en los intervalos RR de el electrocardiograma (ECG) por medio de el procesamiento digital de señales, aplicando la transformada wavelet se permite observar la dinámica espectral y temporal de una señal cardiaca con el fin de evaluar la actividad del sistema nervioso autónomo.

</p>

### Sistema nervioso autonomo (SNA)
Es uin componente fundamental del sistema nervioso encargada de controlar las funciones corporales involuntarias que son escenciales para la supervivencia del ser humano, grstiona los procesos vitales como por ejemplo la frecuencia cardiaca, respiracion, respuesta al estres de forma automatica.
El SNA se divide en dos ramas, el sistema simpatico y el parasimpatico donde el sistema simpatico se encarga de generar una respuesta de lucha o huida ante situaciones de peligro que aumenten la frecuencia cardiaca, mientras que el sistema parasimpatico se encarga de la relajacion para lograr un equilibrio al reducir la frecuencia cardiaca. 

![image](https://github.com/user-attachments/assets/8238ede1-98e0-4284-9066-f04a4ccce4c4)

### Electrocardiografia (ECG)
Es una técnica que tiene el objetivo de registrar la actividad eléctrica del corazón producida en cada latido cardíaco. Esta actividad eléctrica se capta desde la superficie corporal y se grafica en un papel mediante una representación trazada, por medio de esta se observan diferentes ondas que representan los estímulos eléctricos de las aurículas y los ventrículos.
Para el registro de esta tecnica, se hace una segmentación por fases que describen la actividad eléctrica del corazón:

•	Onda P: Representa la despolarización de las aurículas.
•	Complejo QRS: Representa la despolarización de los ventrículos.
•	Onda Q: Primera deflexión negativa del complejo.
•	Onda R: Primera deflexión positiva del complejo.
•	Onda S: Segunda deflexión negativa del complejo (si existe).
•	Onda T: Representa la repolarización de los ventrículos.

![image](https://github.com/user-attachments/assets/8e3123bd-8bc8-4e75-b14a-fc430fc9a334)

Para el desarrollo de esta prueba medica es necesario tener en cuenta factores como la limpieza de la piel, la colocacion de los electrodos en la ubicacion de las derivaciones a evaluar del corazon y la fijacion del electrodo con un gel conductor.

La frecuencia cardiaca es el número de veces que se contrae el corazón en un minuto, la interacción del sistema existe cuando se afecta la neutralidad del sistema, por ejemplo ante una situación de estrés o peligro afectando la frecuencia cardiaca. Aumentando la frecuencia cardiaca por medio de la liberación de neurotransmisores como la noradrenalina permitiendo un mayor bombeo de sangre y aumentando la fuerza de contracción lo cual mejora el gasto cardiaco. Mientras que en el sistema parasimpatico disminuye la frecuencia cardiaca por medio de la liberacion de acetilcolina reduciendo la frecuencia de contraccion lo cual permite al cuerpo descansar ademas de disminuir la fuerza de contraccion que disminuye la fuerza del corazon.

### Sistema de adquisicion de datos (DAQ)
Es un conjunto de componentes que permite medir un fenomeno electrico o fisico, incluye sensores, convertidores analogo-digitales. Mide señales fisicas del mundo real y las convierte en datos digitales para su analisis. Este sistema es fundamental para capturar la actividad electrica del musculo en tiempo real, utilizando su capacidad para digitalizar las señales analogicas que vienen de los electrodos. garantizando que los datos sean confiables.

### Variabilidad de la frecuencia cardiaca (HRV).
Es un indicador de el equilibrio en el SNA, para medir las fluctuaciones en los tiempos entre latidos consecutivos se pueden realizar por medio de diferentes metodos, como el analisis de tiempo dominante, el cual analiza directamente los intervalos RR, obteniendo informacion valiosa sobre la dinamica cardiaca. otro metodo podria ser el analisis espectral obteniendo informacion de los sistemas nerviosos simpaticos y parasimpaticos sobre la VFC, donde a muy baja frecuencia esta alimentado a 0.04Hz y a una alta frecuencia esta alimentado sobre un rango de 0.2 a 0.5Hz dependiendo de la frecuencia respiratoria. 

### Transformada Wavelet.
La transformada wavelet es una técnica matemática que descompone una señal en una serie de funciones básicas llamadas wavelets. A diferencia de la transformada de Fourier, que descompone una señal en componentes sinusoidales de diferentes frecuencias, las wavelets ofrecen una representación más localizada en el tiempo y la frecuencia, lo que las hace particularmente útiles para analizar señales no estacionarias como las biológicas.
Las wavelets son funciones con una duración limitada y un valor promedio cercano a cero. Su forma puede variar, lo que permite adaptar el análisis a diferentes tipos de señales. Al descomponer una señal en wavelets, se obtiene una representación que revela tanto los componentes de baja frecuencia (tendencias a largo plazo) como los de alta frecuencia (detalles locales) [5].
En este laboratorio, hacer uso de la técnica del electrocardiograma (ECG) la wavelet transformada permite descomponer una señal compleja en diferentes frecuencias y localizaciones temporales, lo que facilita la identificación de características específicas y la detección de anomalías.

    
#### Transformada rapida de Fourier.

<P>
Esta transformación es una herramienta crucial para analizar y manipular el contenido espectral del audio, esto es fundamental para aplicaciones como la separación de fuentes.
Aplicación. La Transformada Rápida de Fourier (FFT) procesa una señal de audio en el dominio del tiempo, donde se representa la amplitud de la onda sonora a lo largo del tiempo, y la transforma en el dominio de la frecuencia. Esto permite visualizar la intensidad de cada componente de frecuencia presente en la señal original, es decir, identificar qué frecuencias conforman el sonido. En el caso del laboratorio, donde se analizan dos fuentes con diferentes timbres de voz, la FFT permite reconocer los rangos de frecuencia característicos de cada tipo de voz, donde una voz aguda ocuparia un rango de frecuencia alto, mientras que una voz gruesa ocuparia un rango de frecuencias bajas. 
</p>

#### Transformada de Fourier.
<P>
Una transformacion es una operacion que convierte una señal desde un dominio a otro dominio, la transformada de fourier convierte una señal del dominio del tiempo hacie el dominio de la frecuencia. Lo cual permite analizar las señales en dominios alternativos lo cual permite identificar las caracteristicas como frecuencias.


![image](https://github.com/user-attachments/assets/e99929ac-96c2-49d6-a698-49534e1e54b7)
![image](https://github.com/user-attachments/assets/88e9aaf2-18df-4590-8c21-bdc98815744e)

![image](https://github.com/user-attachments/assets/654d9a8a-8856-4f38-9b46-acaa4eee6157)
![image](https://github.com/user-attachments/assets/ee5c9486-1435-4d9e-8af1-fdb47ac1f634)

![image](https://github.com/user-attachments/assets/ecf733fa-216f-441c-8285-62baba6ab65c)
![image](https://github.com/user-attachments/assets/8a446bea-2efc-49e2-a544-22376ce016fd)

![image](https://github.com/user-attachments/assets/664a0529-c497-4751-be44-00c36b50ba20)
![image](https://github.com/user-attachments/assets/75da7548-4a08-4ae2-9ca9-60fbe488d075)

Podemos observar para la contraccion 1 y 37 de la transformada de furier en la ventana Hamming diferencias clave como la amplitud de la frecuencia, para la contraccion 1 la amplitud del pico principal es mayor a la amplitud de la contraccion 37, 220 es la amplitud en la contraccion 1 y 80 en la 37. Esto nos indica que la contraccion inicial tiene mayor potencia en la frecuencia dominante, Mientras que en la contraccion final la potencia ha disminuido significativamente lo que evidencia los indicios de fatiga muscular. Se obserba que mediante el musculo se fatiga la señal se vuelve mas dispersa en los espectros de potencia.

Si comparamos las ventanas hamming y hanning para las mismas contracciones se evidencia que la ventana Hamming mantiene mejor la energia del pico. Mientras que la ventana Hanning reduce la contamincion espectral. FFT con Hann tiene un pico principal de 75, es mas limpia y con menos ruido fuera del pico, FFT con Hamming tiene el pico ligeramente mayor (80) y tiene mayor presencia de los lobulos laterales.

</p>


### Analisis estadisticos.
<p>
 Por medio de este analisis validaremos los hallasgos fisiologicos, evidenciando que la disminucion de la frecuencia no sea aleatorea, sino que nos muestre su asociacion con la fatiga.
 
![image](https://github.com/user-attachments/assets/6e47d9f0-39ad-4e1a-994f-d8f2018011a9)

En la imagen podemos observar los resultados de un analisis de fatiga muscular basado en una frecuencia dominante, no aprobamos la hipotesis nula debido a la diferencia significativa entre frecuencias iniciales y frecuencias finales, lo que podria evidenciar la presencia de una fatiga muscular puesto a que la frecuencia dominante disminuye mediante aumenta el tiempo, reflejando los cambios en la conduccion neuromuscular y en la unidad motora.

</p>

### Análisis de resultados
<p>
Para el análisis de los resultados proporcionados, podemos evidenciar que la frecuencia de oscilacion es mayor en la contraccion 1 mostrando un patron de oscilaciones densas y uniformes, indicando que el musculo genera impulsos electricos con alta frecuencia, mientras que en la contraccion 37 la frecuencia se reduce de forma considerable, las oscilaciones son irregulares y menos frecuentes, lo que podriamos interpretar como una fatiga muscular donde lla unidad motora disminuye su tasa de disparo y coordinacion.
</p>

### Requisitos
<p>

  - Electrodos de superficie para EMG.
  - Sistema de adquisición de datos (DAQ).
  - Software de análisis (Python, NI-DAQmx).
  - Computador con acceso a internet.
    
Para ejecutar el código, es necesario instalar Python e importar las siguientes librerías:

- import librosa
- import numpy as np
- import matplotlib,pyplot as plt
- from sklearn.descomposition import
- iport scipy
  
Tener instalado un compilador, que para este caso se utilizo spyder.  
</p>

### Estructura del proyecto

- tfourier(): Transformada de fourier.
- numpy: permite realizar operaciones matemáticas eficientes en matrices y arreglos.
- matplotlib: biblioteca estándar para crear visualizaciones.
- scipy: funciones para el diseño y aplicación de filtros.


### Ejecución

- Asegúrate de que los archivos de datos están en la misma carpeta que los scripts.
-	Ejecuta Lab4.py o LAB4final.py para analizar la señal:
- python Lab4.py
  


### Bibliografia

- Heras Rodríguez, MDL (2024). La transformada rápida de Fourier: fundamentos y aplicaciones (Tesis de licenciatura).
- Mena, A. O., Yolanda, G., Cano, V., & Tizayuca-pachuca, F. (2014). Adquisición y procesamiento de una señal electromiográfica para control de una prótesis. Universidad Autónoma Del Estado de Hidalgo, XXIX, 2, 1-8.
- Señales usando ventanas, T. A. F. (s/f). Sistemas y Señales I. Edu.ar. Recuperado el 4 de octubre de 2024, de https://www.fceia.unr.edu.ar/tesys/html/Analisis_Frecuencial_usando_ventanas.pdf


### Licencia

Este proyecto es de uso académico y educativo.

### Contacto
<p>
Si tienes alguna pregunta o sugerencia, no dudes en contactarme:
</p>

- **Nombre:** [Juan David Cediel Farfan][Juan Yael Barriga Roa]
- **Email:** [est.juand.cediel@unimilitar.edu.co][est.juan.barriga@unimilitar.edu.co]
- **GitHub:** [David05Cediel][JuanYBR]

