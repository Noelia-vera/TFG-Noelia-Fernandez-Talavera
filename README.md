# TFG Noelia Fernández Talavera

## _"Sistema de navegación autónomo en entornos reales y simulados para situaciones de emergencia"_

### Ingeniería de Tecnologías Industriales (Universidad Rey Juan Carlos)

***

#### DOCUMENTACIÓN DEL PROYECTO EN LA PESTAÑA 'WIKI':

[https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/wiki](https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/wiki)

</p>

***

#### ORGANIZACIÓN DE CARPETAS:

* **Códigos de Arduino:** Códigos para subir a la placa Arduino que controla el movimiento del robot y la toma de datos de los sensores.

* **Códigos de Python para la Raspberry Pi:**  Códigos para ejectar en la Raspberry de manejo del robot y subida de datos a la BBDD.

* **Códigos para la simulación de Unity:** códigos para ejecutar en Unity para el movimiento manual, automático y evacuación del robot.
* **Imágenes:** Diseño en AutoCAD de todos los componentes para la simulación del robot en Unity, imágenes del robot real y de las partes de la torre de bomberos para la simulación (primera planta y sótano).
* **Planos:** Planos de las cotas y las vistas de los componentes del robot para la simulación del robot en Unity.

***

#### RESUMEN

En este Trabajo de Fin de Grado se ha desarrollado e implementando un modelo de agente autónomo terrestre, controlado de forma remota por un bombero gracias a un teclado, e incorporando la tecnología de localización para interiores ‘*UWB’* que proporcionan unas balizas comerciales, pudiendo así identificar la posición exacta de cada amenaza. Además, el robot podrá esquivar obstáculos y crear una ruta de evacuación alternativa hacia la salida para posibles víctimas.

En segundo lugar, se incorporarán sensores de monitorización del entorno que recogen datos de interés medioambiental como temperatura, CO2, % de humedad relativa, concentración bruta de H2, compuestos volátiles orgánicos y etanol. Estos serán almacenados en una base de datos y posteriormente representados en una plataforma visual para su interpretación, evaluando así el nivel de riesgo para la salud humana que existe en la intervención y las posibles opciones de afrontar la situación.

Por último, se creará una simulación tanto del robot como del entorno de intervención, que presenta las mismas características que el escenario real. Una vez diseñado todo, por un lado, se programa la conducta del entorno incorporando fuego, obstáculos y personas, y por otro lado se programa el comportamiento del robot creando un modo manual controlado por teclado, un modo automático haciendo un recorrido similar al que realizaría el robot en el entorno real con las balizas de localización, y un modo de evacuación donde el autómata calcula la ruta más segura y rápida hacia la salida. Su finalidad es estimar tiempos de intervención y crear recorridos alternativos más seguros identificando las zonas más peligrosas del espacio.

***

#### 1. ROBOT REAL



***

#### 2. ROBOT SIMULADO

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Componentes_robot_simulacion/robot_montado.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Componentes_robot_simulacion/Robot_montado2.PNG">
</p>





#### 3. UNITY





***

#### 4. BASE DE DATOS





***

