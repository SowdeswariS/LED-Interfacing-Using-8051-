<img width="717" height="444" alt="Screenshot 2025-11-12 092031" src="https://github.com/user-attachments/assets/5a9503b3-da5c-4faf-ac8f-b9ca77474998" /># LED Interfacing Using 8051  
## Aim:
To interface an LED with the 8051 microcontroller and control its operation.
## Apparatus Required:
1.Laptop with Keil uVision software
<br>2.Proteus Design Suite
## Circuit Diagram Setup in Proteus:
1.	Open Proteus and create a new project.
2.	Add the following components from the library:
<br> 8051 Microcontroller (AT89C51)
<br> LED
<br> Resistor (330Ω)
<br> Ground (GND) connection
3.	Connect the LED's anode to P1.0 of the microcontroller through a 330Ω resistor.
4.	Connect the cathode of the LED to GND.
5.	Save the design and proceed to programming in Keil.
## Algorithm:
1.	Configure P1.0 as an output port.
2.	Set P1.0 HIGH to turn ON the LED.
3.	Introduce a delay.
4.	Set P1.0 LOW to turn OFF the LED.
5.	Introduce a delay.
6.	Repeat the process continuously.
## Program:
#include <reg51.h>
void delay(unsigned int x)
{
int i;
for(i=0;i<x;i++);
}
void main()
{
while(1)
{
P1=~P1;
delay(1000);
}
}
## Output:
<img width="717" height="444" alt="Screenshot 2025-11-12 092031" src="https://github.com/user-attachments/assets/7947aac4-e1ce-4153-91e5-0b1f0a275e81" />

## Result:
The LED interfacing with the 8051 microcontroller has been successfully implemented and simulated using Keil and Proteus.

