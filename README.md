The scope of this project can be broken down into to the following parts

 Interfacing with already existing flow rate meters, power analyzers and temperature
sensors using MODBUS RTU protocol (an industrial standard communication
protocol) via RS485 (a communication method utilized to carry signals over two wires)
 Transmitting data wirelessly to a local or cloud based server.
 Creating a real time dashboard for data representation
 Logging data on a periodic basis 

PCB 

 ESP-12E Microcontroller
 LM2596 Adjustable Buck Converter to drop down voltage to 3.3V
 MAX485 module for RS485 communication
 4051N 8 channel analog multiplexer
 4N25 Optocoupler
 1N4001 Diode for reverse polarity protection
 Different values of resistors to limit current, sample 4-20ma currents, pull or pull up
voltage levels. 

All components were soldered and the circuit was installed in three different places of the
factory. One circuit was interfaced with two flow rate meters. These meters were used to
monitor the steam flow into the two Steamer machines. Another two boxes were interfaced
with the power analysers connected to the steamers. An encoder was also made using a
proximity sensor in order to measure the meterage of fabric fed into the steamer machine. The data transmitted over WiFi by the ESP-12E sensors were handled by a locally hosted
MQTT broker. A raspberry pi was used initially as the server for this project. MQTT is a
machine to machine connectivity protocol mainly used in IoT applications. 
24
For the purposes of this project, an open source MQTT broker (an agent that deals with
incoming and outgoing messages) called MOSQUITTO was used. Server side scripting was
done using NodeJS (an open source server framework) along with other node modules. Freely
available charting libraries were used to represent data in an attractive way. By using javascript,
regular logs of sensor data were exported to excel documents and saved on to the server. By
using an SMTP mail server, these logs were automatically sent to a preset mailing address at
the end of the day. The server for this project was created on the cloud, using AWS (Amazon Web Services) which
enabled any authorized person to view the current operating stats of the factory. A sound
knowledge about industrial sensors, electrical circuits, software development and PCB design
was gained by completing this project. 

