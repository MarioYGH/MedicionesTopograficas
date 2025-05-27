# Mediciones Topográficas (Servicio Social)

El objetivo principal del proyecto fue diseñar e implementar un sistema de monitoreo que permita registrar con precisión el desplazamiento de una pared. Para ello, se utiliza una caja de instrumentación equipada con sensores de desplazamiento basados en potenciómetros lineales. Los datos adquiridos se almacenan en una tarjeta SD y se transmiten mediante tecnología LoRa a una unidad de monitoreo remoto. Adicionalmente, el sistema está diseñado para operar de manera autónoma en entornos exteriores y garantizar un monitoreo continuo.
Descripción del Sistema
Sensores y Adquisición de Datos
Se emplearon tres potenciómetros lineales para medir el desplazamiento de puntos clave en la pared. La conversión de voltaje a distancia se realizó mediante una caracterización detallada de los sensores, ajustando los valores de salida con un polinomio de regresión para garantizar la precisión de las mediciones. Los coeficientes de ajuste fueron determinados a partir de mediciones experimentales, asegurando la conversión precisa de voltaje a milímetros.
Para garantizar la confiabilidad de las mediciones, se realizaron pruebas de calibración en distintos entornos y condiciones de temperatura, evaluando la estabilidad de los sensores y su respuesta ante variaciones en la humedad y el ambiente.
Electrónica y PCB
El circuito de adquisición de datos fue diseñado y fabricado en una PCB mediante el método de planchado. Se tomaron en cuenta normas de diseño para garantizar la confiabilidad del sistema, tales como el uso de pistas de cobre de ancho adecuado para la transmisión de señales de baja impedancia y la inclusión de filtros para reducir el ruido eléctrico.
El dispositivo cuenta con un ESP32 como unidad de procesamiento, encargado de la adquisición de datos, almacenamiento en una tarjeta SD y transmisión de la información vía LoRa. Se optimizó el código para minimizar el consumo energético y garantizar una transmisión eficiente de los datos.

Caja de Instrumentación
Para alojar los componentes electrónicos y los sensores, se diseñó una caja en SolidWorks, la cual fue impresa en 3D utilizando ABS. Este material fue seleccionado por su resistencia a la exposición solar y su durabilidad en entornos exteriores. La caja permite la instalación segura de los sensores y facilita el mantenimiento del sistema.
La caja también fue diseñada con compartimentos específicos para cada componente, asegurando la organización del cableado y evitando interferencias electromagnéticas. Además, se implementaron sellos de silicona para evitar la filtración de humedad en el interior del dispositivo.

Comunicación y Almacenamiento de Datos
La información recopilada por los sensores es procesada por el ESP32, la cual es almacenada en una tarjeta SD y transmitida vía LoRa a una estación de monitoreo. Para el registro temporal de los datos, se integró un RTC (reloj en tiempo real), asegurando que cada medición cuente con una referencia temporal precisa.
El protocolo LoRa permite la transmisión eficiente de datos a largas distancias con bajo consumo energético, lo que resulta ideal para el monitoreo remoto en zonas donde no hay acceso a redes WiFi o celulares. Se realizaron pruebas de transmisión para verificar el alcance del sistema en diferentes entornos, logrando una cobertura de hasta 2 km en condiciones óptimas.
Resultados y Conclusiones
La caja de instrumentación permite la recopilación precisa de datos sobre el desplazamiento de la pared, facilitando su monitoreo en el tiempo. La implementación de la PCB y el diseño de la caja en ABS garantizan la durabilidad del sistema en condiciones adversas. La transmisión vía LoRa asegura la disponibilidad remota de los datos, contribuyendo al análisis de la estabilidad estructural del sitio monitoreado.
Se realizaron pruebas de funcionamiento para verificar la precisión de los datos adquiridos, comparándolos con mediciones manuales de referencia. Los resultados mostraron una alta correlación entre las mediciones, validando la efectividad del sistema.
