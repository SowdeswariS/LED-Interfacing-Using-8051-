# LED Interfacing Using 8051  
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

ORG 0000H      ; Start of program
MOV P1, #00H   ; Set Port 1 as output

MAIN:  SETB P1.0  ; Turn ON LED
       CALL DELAY  ; Call delay function
       CLR P1.0    ; Turn OFF LED
       CALL DELAY  ; Call delay function
       SJMP MAIN   ; Repeat the process

DELAY: MOV R7, #255  ; Outer loop
       MOV R6, #255  ; Inner loop
       DJNZ R6, $    ; Decrement inner loop
       DJNZ R7, $    ; Decrement outer loop
       RET           ; Return from delay

END

## Output:
<img width="1347" height="634" alt="image" src="https://github.com/user-attachments/assets/a7327699-a3b0-4f18-8c68-a0c8c673f437" />

<img width="717" height="444" alt="Screenshot 2025-11-12 092031" src="https://github.com/user-attachments/assets/a55c9119-7012-4f41-b492-f9f39e955d5a" />

## Result:
The LED interfacing with the 8051 microcontroller has been successfully implemented and simulated using Keil and Proteus.

