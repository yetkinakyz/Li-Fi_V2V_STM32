# STM32 Based V2V Wireless Serial Communication with Li-Fi Technology
This project aims serial communication between two vehicles by using visible light spectrum. It is still in progress.

I used two STM32F103C8T6 based development boards for communication.

The transmitter side has 5 buttons and a 16x2 LCD screen. Each button controls one different messege. The LCD shows the selected message before it is sent.
In order to see and select a message, push a button once. Then push the same button again in order to send the message. If you push a different button, you see and select a different message. 

The receiver side has a 16x2 LCD screen and a buzzer. When a message is received to the receiver side, the buzzer sounds and the message is printed on the LCD.
The buzzer sounds until the message is received and showed on the LCD.

The transmitter transmits a single character corresponding to a message on the receiver side. For example, the transmitter sends "_".
When the character is transmitted to the receiver, the receiver prints the message corresponding to that character. For example, the receiver prints "SLOW!".

The LCDs communicate with the boards over I2C. You should check the slave addresses in I2C LCD libraries because these addresses depend on your LCD I2C drivers.
You should add a zero bit to your slave address when you change it. For example, if your slave address is 0x27, you should write it as 0x4E.

I used a 5W power led as the transmitter's light source, and I used BPW34, a photodiode, in order to capture signals. In order to communciate over visible light, I used OOK (On-Off Keying) modulation. For serial communication, I used UART protocol.

In this project, communication is provided at 115200 baud rate in line with the owned resources. It does not work adaptively yet. In other words, communication can be achieved at a certain light intensity or distance. An AGC can solve this problem.

If you have a suggestion or a question, or just want to say hi, please contact me!

- Website: https://yetkinakyuz.com
- Mail: contact@yetkinakyuz.com
