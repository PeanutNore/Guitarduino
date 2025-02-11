# guitarduino
Update 2025/02/11: In 2020 Microchip introduced the AVR Dx series, including the AVR128DA28 which is available in the same DIP-28 package as the ATMega238.
These new parts include an onboard DAC, 16kb of RAM, and internal 24MHz clock. Rather than add support for these parts to guitarduino, I have created a new
repository for a digital delay project using the AVR128DA28 at github.com/PeanutNore/1985-Delay

Software for running Arduino based guitar effects. Free software licensed under GPL.

guitarduino-mode-switching is the main release intended to run on the matching hardware to take advantage of the mode switches and provide 16 different effect modes.

Supports ATMega 168/328 based Arduinos using onboard ADC and resistor ladder DAC on PORTB. 
The schematic is included for the board used to develop these sketches and can be viewed / edited in Eagle 6 or higher.
This instructable offers a good explanation of the resistor ladder DAC used: http://www.instructables.com/id/Arduino-Audio-Output/
  NOTE: In the instructable PORTD is used for an 8 bit DAC.
        Even with 1% resistors it's impossible to achieve 
        an accurate 8 bit resistor ladder DAC. In this project
        PORTB is used, which offers 6 pins (the 2 highest bits
        are used for the clock crystal on the ATMega chip. It
        is possible to achieve good accuracy for a 6 bit R/2R
        resistor ladder DAC using common 5% resistors, and this
        project is going for simplicity wherever possible.
        

