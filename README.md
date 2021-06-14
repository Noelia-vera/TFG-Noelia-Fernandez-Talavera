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

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/Robot_alzado.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/Robot_perfil%20(2).jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/Robot_alzadot.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/Robot_perfil.jpg">
</p>
<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/Robot_perspectiva%20(2).jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/Robot_perspectiva%20(3).jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/Robot_perspectiva%20(4).jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/Robot_perspectiva.jpg">
</p>


##### 	1.1 NIVEL 0

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/N0detalle.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/N0detalle%20(2).jpg">
</p>


##### 	1.2 NIVEL 1

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/N1planta.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/N1perfil.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/N1detalle.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/N1detalle%20(2).jpg">
</p>


##### 	1.3 NIVEL 2

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/N2tapa.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/N2planta.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/N2perfil%20(2).jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/N2detalle.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/N2despejado.jpg">
</p>


##### 	1.4 Nivel 3

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/N3perfil%20(3).jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/N3perfil%20(2).jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/N3perfil.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/N3detalle.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot_real/Small/N3frente.jpg">
</p>



***

#### 2. ROBOT SIMULADO

#####		2.1 NIVELES

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Componentes_robot_simulacion/Small/robot_montado.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Componentes_robot_simulacion/Small/Robot_montado2.PNG">
     <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Componentes_robot_simulacion/Small/Chasis.PNG">   
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Componentes_robot_simulacion/Small/Nivel%200_1.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Componentes_robot_simulacion/Small/Nivel2.PNG">
</p>

##### 	2.2 COMPONENTES

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Componentes_robot_simulacion/Small/Arduino.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Componentes_robot_simulacion/Small/Pozyx.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Componentes_robot_simulacion/Small/Pozyx_Arduino.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Componentes_robot_simulacion/Small/Raspberry.PNG">
     <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Componentes_robot_simulacion/Small/Sensor_gas.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Componentes_robot_simulacion/Small/Temperatura.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Componentes_robot_simulacion/Small/Ultrasonidos_soporte.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Componentes_robot_simulacion/Small/Protoboard.PNG">
</p>

***




#### 3. UNITY





***

#### 4. BASE DE DATOS

##### 	4.1 PRUEBA 1, SÓTANO

 <p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/BBDD_Resultados/Prueba1_aire.png">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/BBDD_Resultados/Prueba1_ambiental.png">
</p>

***

