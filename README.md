# Automatic-Street-Light-Controlling-System
# Abstract
The street lighting is one of the largest energy expenses for a city. An intelligent street lighting system can cut municipal street lighting costs as much as 50%-70%. An intelligent street lighting system is a system that adjusts light output based on usage and occupancy,i.e.,automating classification of pedestrian versus cyclist, versus automotive. An intelligent street light management proposes the installation of the wireless based system to remotely track and control the actual energy consumption of the street lights and take appropriate energy consumption reduction measures through power conditioning and control. The street light controller should be installed on the pole lights which consist of microcontroller along with various sensor and wireless module. The street light controller installed on the street light pole will control LED street lighting depending on traffic flow, communicate data between each street light. The data from the street light controller can be transferred to base station using wireless technology to monitor the system.
# Hardware Components
<ul>
<li> NodeMCU</li>
<li> LDR(Light Dependent Resistor)</li>
<li> LEDs</li>
<li> Breadboard</li>
<li> IR Sensors</li>
<li> Resistors</li>
</ul>

# Software used
<ul>
<li> Arduino IDE</li>
<li> Thingspeak IOT platform</li>
 </ul>

# Working
The LDR sensor is used to detect whether it is daytime or night time. Since LDR sensor generates variable resistance based on the amount of light falling on it, it has to be connected like a potentiometer. One end of the LDR sensor is connected to 5V and other end is connected to fixed resistance which is further connected to ground. NodeMCU has one ADC pin (A0) which is connected to point between fixed resistance and one end of the LDR sensor as shown in the circuit diagram. Since the LDR sensor gives variable resistance therefore variable voltage will be generated at A0 according to the amount of light falling on LDR.
IR sensors are used to detect if someone is crossing the street or not. It detects the obstacle or motion in the surrounding. The transmitter will transmit IR rays which will be reflected back if it falls on some object like person, animal, vehicles, etc. The reflected ray will be received by receiver diode and hence will confirm the presence of object and the corresponding LED will be glowed. This method will save significant amount of electricity as the street light will only turns on if there is someone present in the Street. IR sensor has 3 pins, two of which are VCC and ground and one is output pin. The output of IR sensor gets high if detects presence of some object. This pin is connected to GPIO pin of NodeMCU so whenever the IR sensor detects someone passing through the street it triggers the Street light. In our case one LED will be turned on.
