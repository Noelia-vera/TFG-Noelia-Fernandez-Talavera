# TFG Noelia Fernández Talavera

## _"Sistema de navegación autónomo en entornos reales y simulados para situaciones de emergencia"_

### Ingeniería de Tecnologías Industriales (Universidad Rey Juan Carlos)

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
* **Resultados:** Imágenes de los recorridos real y simulados de las pruebas en el CUS, y parámetros ambientales

***

#### RESUMEN

Este Trabajo de Fin de Grado consiste en el desarrollo he implementación de un agente autónomo terrestre, capaz de monitorizar el entorno gracias a la tecnología Ultra -Wide Band para la localización de interiores. Posee tres modos de movimiento: de forma manual controlada por teclado, automática realizando un recorrido definido por el usuario, y evacuación creando una ruta alternativa hacia la salida para posibles víctimas. Además, lleva instalados unos sensores de ultrasonidos para esquivar obstáculos he identificar la posición exacta de cada amenaza. 

También, se han incorporado sensores ambientales para monitorizar el entorno de intervención. Los parámetros selecionados son temperatura, CO2, % de humedad relativa, concentración bruta de H2, compuestos volátiles orgánicos y etanol. Son almacenados en una base de datos y representados en una plataforma visual en tiempo real llamada Grafana. De esta forma se puede evaluar la calidad del aire a lo largo de la intervención para garantizar la seguridad de los equipos de emergencias.

Por último, se ha creado una simulación del agente autónomo y del entorno de intervención, que presentan las mismas características que los real. Por un lado, se ha  programado el entorno incorporando fuego, obstáculos y personas; por otro lado se ha programa el comportamiento del autómata creando un modo manual, un modo automático que hace un recorrido similar al que se realiza en las pruebas y un modo de evacuación para encontrar la ruta más eficiente y rápida hacia la salida. Con ello se obtienen la identificación de las zonas más peligrosas del espacio y los tiempos de intervención.

***

#### 1. [AGENTE AUTÓNOMO REAL](https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/tree/main/Im%C3%A1genes/Robot/Real)

El autómata está dividido en varios niveles para poder insertar nuevo módulos en líneas futuras

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/Robot_alzado.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/Robot_perfil%20(2).jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/Robot_alzadot.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/Robot_perfil.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/Robot_perspectiva%20(2).jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/Robot_perspectiva%20(3).jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/Robot_perspectiva%20(4).jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/Robot_perspectiva.jpg">
</p>


#####	NIVEL 0

Este nivel esta compuesto por el chasIs, dos motores, una batería de litio y tres pilas recargables.

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/N0detalle.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/N0detalle%20(2).jpg">
</p>


##### 	NIVEL 1

Se encuentra el controlador de los motores, una placA Arduino UNO WiFi REV2 y una Raspberry Pi 4.

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/N1planta.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/N1perfil.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/N1detalle.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/N1detalle%20(2).jpg">
</p>


##### 	NIVEL 2

Aquí hay 6 sensores de ultrasonidos, Una placa Arduino UNO WiFi REV2, un sensor de temperatura, % de humedad y un sensor de calidad de aire.

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/N2tapa.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/N2planta.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/N2perfil%20(2).jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/N2detalle.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/N2despejado.jpg">
</p>


##### 	NIVEL 3

Destinado al acoplamiento de nuevo elementos como una UDO, cámara térmica, Pycom, Deep Beacon, etc.

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/N3perfil%20(3).jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/N3perfil%20(2).jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/N3perfil.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/N3detalle.jpg">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Real/Small/N3frente.jpg">
</p>




***

#### 2. AGENTE AUTÓNOMO SIMULADO EN [AUTOCAD](https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/tree/main/Im%C3%A1genes/Robot/Simulado_AutoCAD) Y EN [UNITY](https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/tree/main/Im%C3%A1genes/Robot/Simulado_Unity)

Para la simulación se ha creado el agente autónomo en AutoCAD con todos los componentes y el entorno con Unity, una plataforma para desarrollar videojuegos muy versatil.

#####		2.1 AGENTE AUTÓNOMO Y NIVELES EN [AUTOCAD](https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/tree/main/Im%C3%A1genes/Robot/Simulado_AutoCAD)

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_AutoCAD/Small/robot_montado.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_AutoCAD/Small/Robot_montado2.PNG">
     <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_AutoCAD/Small/Chasis.PNG">   
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_AutoCAD/Small/Nivel%200_1.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_AutoCAD/Small/Nivel2.PNG">
</p>


##### 	2.2 COMPONENTES AUTOCAD

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_AutoCAD/Small/Arduino.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_AutoCAD/Small/Pozyx.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_AutoCAD/Small/Pozyx_Arduino.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_AutoCAD/Small/Raspberry.PNG">
     <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_AutoCAD/Small/Sensor_gas.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_AutoCAD/Small/Temperatura.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_AutoCAD/Small/Ultrasonidos_soporte.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_AutoCAD/Small/Protoboard.PNG">
</p>



##### 2.3 AGENTE AUTÓNOMOY NIVELES EN [UNITY](https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/tree/main/Im%C3%A1genes/Robot/Simulado_Unity)

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_Unity/Small/perfili.png">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_Unity/Small/alzado.png">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_Unity/Small/perfild.png">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_Unity/Small/alzadot.png">
</p>
<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_Unity/Small/persp%20(2).PNG">
	<img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_Unity/Small/persp2.png">
	<img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_Unity/Small/persp%20(4).PNG">
    </p>

<p algin="center">   
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_Unity/Small/detalles1.PNG">
   <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_Unity/Small/N1.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Robot/Simulado_Unity/Small/N2.png">
    </p>


***


#### 3. ENTORNO EN UNITY

##### 3.1 [SÓTANO](https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/tree/main/Im%C3%A1genes/Entorno/Simulado_Unity/Sotano)

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Entorno/Simulado_Unity/Sotano/Small/Sotano_planta.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Entorno/Simulado_Unity/Sotano/Small/sotano1.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Entorno/Simulado_Unity/Sotano/Small/sotano2.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Entorno/Simulado_Unity/Sotano/Small/sotano3.PNG">
        <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Entorno/Simulado_Unity/Sotano/Small/sotano5.PNG">
</p>

##### 3.2 [PRIMERA PLANTA](https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/tree/main/Im%C3%A1genes/Entorno/Simulado_Unity/Primera_planta)

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Entorno/Simulado_Unity/Primera_planta/Small/planta1.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Entorno/Simulado_Unity/Primera_planta/Small/planta14.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Entorno/Simulado_Unity/Primera_planta/Small/planta13.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Entorno/Simulado_Unity/Primera_planta/Small/planta3.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Entorno/Simulado_Unity/Primera_planta/Small/planta4.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Entorno/Simulado_Unity/Primera_planta/Small/planta7.PNG">
     <img src=" https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Entorno/Simulado_Unity/Primera_planta/Small/planta10.PNG.PNG">
     <img src=" https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Entorno/Simulado_Unity/Primera_planta/Small/planta11.PNG.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Im%C3%A1genes/Entorno/Simulado_Unity/Primera_planta/Small/planta8.PNG">
</p>


***

##### 4. EJEMPLOS DE [PLANOS](https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/tree/main/Planos)

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Planos/Small/Plano_cotas_Controlador.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Planos/Small/Plano_dise%C3%B1o_Controlador.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Planos/Small/Plano_cotas_PozyxArduino.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Planos/Small/Plano_dise%C3%B1o_PozyxArduino.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Planos/Small/Plano_cotas_Ultrasonidos_Soporte.PNG">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Planos/Small/Plano_dise%C3%B1o_Ultrasonidos_Soporte.PNG">
</p>


##### 5. RESULTADOS DE LAS PRUEBAS

###### 5.1 SÓTANO [REAL](https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Resultados/recorrido%20elementos.png) VS. [SIMULADO](https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Resultados/sotano%20recorrido.png) (VIDEO)

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Resultados/small/recorrido%20elementos.png">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Resultados/small/sotano%20recorrido.png">
</p>

###### 5.2 PRIMERA PLANTA [REAL](https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Resultados/recorrido%20elementos.png) VS. [SIMULADA](https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Resultados/Planta1trayectoria.png) (VIDEO)

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Resultados/small/primera%20prueba%20sotano.png">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Resultados/small/Planta1trayectoria.png">
</p>

###### 5.3 RESULTADOS AMBIENTALES GRAFANA

[PRIMERA PRUEBA](https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Resultados/primera%20prueba.PNG)

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Resultados/small/primera%20prueba.PNG">
</p>

[SEGUNDA PRUEBA](https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Resultados/segunda%20prueba.PNG)

<p algin="center">
    <img src="https://github.com/Noelia-vera/TFG-Noelia-Fernandez-Talavera/blob/main/Resultados/small/segunda%20prueba.PNG">
</p>
