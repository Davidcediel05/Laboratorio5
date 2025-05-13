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

-	Onda P: Representa la despolarización de las aurículas.
-	Complejo QRS: Representa la despolarización de los ventrículos.
-	Onda Q: Primera deflexión negativa del complejo.
-	Onda R: Primera deflexión positiva del complejo.
-	Onda S: Segunda deflexión negativa del complejo (si existe).
-	Onda T: Representa la repolarización de los ventrículos.

![image](https://github.com/user-attachments/assets/8e3123bd-8bc8-4e75-b14a-fc430fc9a334)

Para el desarrollo de esta prueba medica es necesario tener en cuenta factores como la limpieza de la piel, la colocacion de los electrodos en la ubicacion de las derivaciones a evaluar del corazon y la fijacion del electrodo con un gel conductor.

La frecuencia cardiaca es el número de veces que se contrae el corazón en un minuto, la interacción del sistema existe cuando se afecta la neutralidad del sistema, por ejemplo ante una situación de estrés o peligro afectando la frecuencia cardiaca. Aumentando la frecuencia cardiaca por medio de la liberación de neurotransmisores como la noradrenalina permitiendo un mayor bombeo de sangre y aumentando la fuerza de contracción lo cual mejora el gasto cardiaco. Mientras que en el sistema parasimpatico disminuye la frecuencia cardiaca por medio de la liberacion de acetilcolina reduciendo la frecuencia de contraccion lo cual permite al cuerpo descansar ademas de disminuir la fuerza de contraccion que disminuye la fuerza del corazon.

### Sistema de adquisicion de datos (DAQ)
Es un conjunto de componentes que permite medir un fenomeno electrico o fisico, incluye sensores, convertidores analogo-digitales. Mide señales fisicas del mundo real y las convierte en datos digitales para su analisis. Este sistema es fundamental para capturar la actividad electrica del musculo en tiempo real, utilizando su capacidad para digitalizar las señales analogicas que vienen de los electrodos. garantizando que los datos sean confiables.

### Variabilidad de la frecuencia cardiaca (HRV).
Es un indicador de el equilibrio en el SNA, para medir las fluctuaciones en los tiempos entre latidos consecutivos se pueden realizar por medio de diferentes metodos, como el analisis de tiempo dominante, el cual analiza directamente los intervalos RR, obteniendo informacion valiosa sobre la dinamica cardiaca. otro metodo podria ser el analisis espectral obteniendo informacion de los sistemas nerviosos simpaticos y parasimpaticos sobre la VFC, donde a muy baja frecuencia esta alimentado a 0.04Hz y a una alta frecuencia esta alimentado sobre un rango de 0.2 a 0.5Hz dependiendo de la frecuencia respiratoria. 

### Transformada Wavelet.
La transformada wavelet es una técnica matemática la cual se encarga de descomponer una señal en una serie de funciones básicas llamadas wavelets. A diferencia de la transformada de Fourier, que descompone una señal en componentes sinusoidales de diferentes frecuencias, las wavelets ofrecen una representación más localizada en el tiempo y la frecuencia, lo que las hace particularmente útiles para analizar señales no estacionarias.
Las wavelets son funciones con una duración limitada y un valor promedio cercano a cero. Su forma puede variar, lo que permite adaptar el análisis a diferentes tipos de señales. Al descomponer una señal en wavelets, se obtiene una representación que revela tanto los componentes de baja frecuencia (tendencias a largo plazo) como los de alta frecuencia.
En este laboratorio, hacer uso de la técnica del electrocardiograma (ECG) la wavelet transformada permite descomponer una señal compleja en diferentes frecuencias y localizaciones temporales, lo que facilita la identificación de características específicas y la detección de anomalías. hay diferentes tipos de transformada, como por ejemplo. Wavelet de Haar: Una de las wavelets más simples, útil para detectar discontinuidades y cambios bruscos en la señal. Wavelets de Daubechies: Wavelets con diferentes niveles de regularidad, lo que las hace versátiles para una amplia gama de aplicaciones. Wavelet de Morlet: Wavelet compleja con una forma similar a una onda sinusoidal amortiguada, adecuada para analizar señales con componentes tanto sinusoidales como transitorios. Wavelet de Symlet: Similar a la wavelet de Daubechies, pero con simetría alrededor de cero.	Wavelet de Coiflet: Wavelet con un número de momentos nulos, lo que la hace útil para aproximar funciones suaves.


### Diagrama de flujo






### Analisis de resultados.
<p>
    En la comparacion de la señal original contra la filtrada podemos observar una mejora en la calidad señal ante el filtrado del ruido evitando eliminar componentes importantes del electrocardiograma. ademas las ondas R son mas distinguibles, lo que es eficaz para evitar errores en el analisis de hrv.
    
 ![image](https://github.com/user-attachments/assets/c4a49e5d-e657-43a7-9bf4-ca92611ba2f2).

Para la deteccion de picos R en los primeros 10 segundos cada cruz roja marca la posicion de un pico R detectado por medio de la funcion find_peaks con un umbral ajustado, donde se evidencia un ritmo cardiaco estable. Los picos R fueron detectados de manera correcta a lo largo del tiempo, el algoritmo pudo discriminar los eventos R reales, se logro estimar la frecuencia cardiaca y analizar la Heart Rate Variability (HRV).

![image](https://github.com/user-attachments/assets/b380200e-22da-40d7-8ef5-69bccf4ea78e)

Para analizar la Señal RR interpolada para HRV podemos evidenciar una alta variabilidad en los intervalos RR por la actividad del sistema nervioso autonomo, se reflejan tonos en el sistema simpatico y parasimpatico donde en algunas secciones aumenta o disminuye, ademas esta señal es la base para generar un espectograma usando la transformada wavelet.

![image](https://github.com/user-attachments/assets/52bf0f53-98ba-45f6-ba3c-85cefdd2a7a9)

Por medio de la transformada de Wavelet continua de Morlet, podemos observar variaciones espaectrales indicando fluctuaciones en la modulacion del corazon, se evidencia la energia concentrada en las bandas LF lo que nos indica que hay cambios en la actividad simpatica o la respiracion, ademas esta herramienta nos permite detectar patrones que no se ven en el dominio del tiempo, aplicandose en estudios de estres, fatiga, sueño o ejercicio.

![image](https://github.com/user-attachments/assets/0e602461-ed07-46f5-a14c-761075c0f53f)

#### Diferencias analisis del tiempo y la frecuencia.
En el dominio del tiempo podemos analizar parametros globales como la media de los intervalos RR y la desviacion estandar, por medio de este podemos obtener una vision general del ritmo cardiaco y como varia este, pero no podemos identificar cuando ocurren los cambios mientras que en el domidio tiempo-frecuencia es evidente la variacion de frecuencias especificas a lo largo del tiempo, revelando las transiciones de actividad simpatica y parasimpatica.

#### Efecto de funciones Wavelet.
en las funciones Wavelet como la morlet que fue la utilizada fue buena para la deteccion de componentes sinusoidales ademas fue muy util para el analisis de HRV, al cambiar la wavelet afectaria la nitidez, localizacion y sensibilidad del espectograma, afectando principalmente la interpretacion de la actividad autonoma.

#### Aplicaciones de esta practica.
podemos aplicar esta practica en el monitoreo de varias areas como por ejemplo la cardiologia, psicologia, neurociencia, deporte, tecnologia waerable y investigacion biomedica.

</p>


### Requisitos
<p>

  - Electrodos de superficie para ECG.
  - Sistema de adquisición de datos (DAQ).
  - Software de análisis (Python, NI-DAQmx).
  - Computador con acceso a internet.
  - modulo ECG
    
Para ejecutar el código, es necesario instalar Python e importar las siguientes librerías:

- import librosa
- import numpy as np
- import matplotlib,pyplot as plt
- import pywavelets
- import scipy
  
Tener instalado un compilador, que para este caso se utilizo spyder.  
</p>

### Estructura del proyecto

- tfourier(): Transformada de fourier.
- numpy: permite realizar operaciones matemáticas eficientes en matrices y arreglos.
- matplotlib: biblioteca estándar para crear visualizaciones.
- scipy: funciones para el diseño y aplicación de filtros.


### Ejecución

- Asegúrate de que los archivos de datos están en la misma carpeta que los scripts.
-	Ejecuta Lab5.py para analizar la señal:
- python Lab5.py
  


### Bibliografia

- Frecuencia cardiaca. (s/f). Fundación Española del Corazón. Recuperado el 31 de octubre de 2024, de https://fundaciondelcorazon.com/prevencion/marcadores-de-riesgo/frecuencia-cardiaca.html
- Montoya, JRA (2001). La onda transformada. Revista de la Universidad de Mendoza.
- Electrocardiograma. (s/f). Fundación Española del Corazón. Recuperado el 31 de octubre de 2024, de https://fundaciondelcorazon.com/informacion-para-pacientes/metodos-diagnosticos/electrocardiograma.html
- Martínez, JP, & Olmos, S. Sistema de Detección de Puntos Significativos de la señal ECG basado en la Transformada Wavelet. Dep. de Ingeniería Electrónica y Comunicaciones. Univ. de Zaragoza.
- Peña, J. (2004). Espectrogramas basados en funciones Wavelets. Museo Nacional de Ciencias NaturalesMadrid.
- Riaño-Ruiz, LM, & Riveros-Mestre, JS (2023). Sistema de adquisición de señales electrocardiográficas para visualizar el comportamiento cardíaco en corredores de 100 mt.
Medicus, H. (2024, 22 de junio). Efecto de la estimulación simpática y parasimpática sobre la frecuencia cardíaca. Homo médico. https://homomedicus.com/efecto-de-la-estimulacion-simpatica-y-parasimpatica-sobre-la-frecuencia-cardiaca/



### Licencia

Este proyecto es de uso académico y educativo.

### Contacto
<p>
Si tienes alguna pregunta o sugerencia, no dudes en contactarme:
</p>

- **Nombre:** [Juan David Cediel Farfan][Juan Yael Barriga Roa]
- **Email:** [est.juand.cediel@unimilitar.edu.co][est.juan.barriga@unimilitar.edu.co]
- **GitHub:** [David05Cediel][JuanYBR]

