# STM32 Based V2V Serial Communication with Li-Fi Technology
This project aims serial communication between two vehicles by using visible light wavelengths. It is still under construction.

I used two STM32F103C8T6 based development boards for communication. The transmitter side has 5 buttons, each button controls one different messege. The receiver side has a 16x8 LCD screen and a buzzer. When a message is received to the receiver side, the buzzer sounds and the message is printed on the LCD.

I used a 5W power led for the transmitter's light source, and BPW34, a photodiode, in order to capture signals. In order to communciate over visible light, I used OOK (On-Off Keying) modulation. For serial communication, I used UART prothocol.

In this project, communication is provided at 115200 baud rate in line with the owned resources. It does not work adaptively yet. In other words, communication can be achieved at a certain light intensity or distance. An AGC can solve this problem.
