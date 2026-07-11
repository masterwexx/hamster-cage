# hamster-cage

go into code visualization to read the readme

ill be using the arduino IDE;
first of all you are gonna need an esp32 and a GC9A01 round display.

in the User_Setups/Setup43_GC9A01.h check the parameters:
#define TFT_MOSI 23
#define TFT_SCLK 18
#define TFT_CS   5
#define TFT_DC   2
#define TFT_RST  4
#define TFT_BL   -1
#include <User_Setups/Setup_GC9A01_ESP32.h>

Display	ESP32	
  VCC    3V3	
  GND	   GND	
  SCL  	 D18	SPI Clock
  SDA	   D23	SPI MOSI
  CS     D5	  Chip Select
  DC	   D2	  Data/Command
  RST	   D4   reset

now you need to convert your .gif file into different .bin files and add them in a "data" folder inside the main folder (the one with the .ino file)
you should now have a folder looking like this:
Project:
      -file.ino
      -data:
            0.bin
            1.bin
            2.bin
            ...

download the jar file from https://github.com/lorol/arduino-esp32fs-plugin and add it to C:\Users\<your_name>\Documents\Arduino\tools\ESP32FS\tool\esp32fs.jar
open arduino IDE and go to Tools → ESP32 Data Upload

boot the file on the esp32 and you should be ready to go
