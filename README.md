# Basecam-BGC3.0-Clone-Setup

This is a short documentation on how to burn an Arduino bootloader to the BGC3.0 clone to use it for anything but the original gimbal application.

Connect +5V, GND, Reset, SCK, MISO & MOSI between BGC and Arduino, i used the following pins:

RESET = 53

SCK   = 52

MOSI  = 51

MISO  = 50


Select 'ArduinoISP' from File -> Examples -> 11.ArduinoISP
Define chosen pins in the script
Select currently used Arduino board and port under Tools
Choose 'AVRISP mkII' as programmer under Tools
Verify and upload sketch to Arduino

Wire a 100uF capacitor between the pins 5V and Reset on your Arduino  
Select 'Arduino Pro or Pro Mini' as board, 'ATmega328P (5V, 16MhZ)' as processor and choose correct port
Select 'Arduino as ISP' as Programmer, then press 'Burn Bootloader' under Tools

Upload your sketches to the BGC by selecting 'Arduino as ISP' as Programmer and choosing Sketch -> Upload Using Programmer

Atmega328P pinout: https://preview.redd.it/bggdd9srui351.png?auto=webp&s=921ec4b761b0465685a39ff3ee45230ead62f877

BGC3.0 Clone pinout: 

![alt text](https://github.com/p-rott/Basecam-BGC3.0-Clone-Setup/blob/main/Basecam%20Clone%20Pinout.png?raw=true)
