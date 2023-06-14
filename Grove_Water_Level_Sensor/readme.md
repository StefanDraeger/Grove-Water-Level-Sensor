

## Grove Water Level Library
This tiny library is for read the current level from Grove Water Level Sensor.
Please note that the code behind this library is from [Seeed Studio - Grove Water Level Sensor](https://wiki.seeedstudio.com/Grove-Water-Level-Sensor/). I've only put the code into a library to reduce code in my Arduino project, and now I like to share this with you.

<p align="center" width="100%">
    <img width="33%" src="https://github.com/StefanDraeger/Grove-Water-Level-Sensor/blob/main/Grove_Water_Level_Sensor/documentation/Grove_Water_Level_Sensor.png">
</p>

###  Example

Here is an example, with initialize an Object of type WaterLevelSensor and call function with readPercentage.

    #include <waterlevelsensor.h>
    
    WaterLevelSensor sensor = WaterLevelSensor();
    
    void setup() {
      Serial.begin(9600);
    }
    
    void loop() {
      //lesen des Grove Wasser Level Sensors
      int waterLevel = sensor.readPercentage();
    
      //Ausgeben des ermittelten Wertes
      Serial.print(waterLevel);
      Serial.println("%");
      
      delay(25);
    }

The output is like the original one, with only the percentage of fill of cup.

<p align="center" width="100%">
    <img width="33%" src="https://github.com/StefanDraeger/Grove-Water-Level-Sensor/blob/main/Grove_Water_Level_Sensor/documentation/Output_Arduino_IDE_Water_Level_Sensor.png">
</p>

### Example with Grove LED Bar v2
At my blogpost [Arduino UNO R3 & Grove LED Bar v2](https://draeger-it.blog/arduino-uno-r3-grove-led-bar-v2/) you can find a example with the Grove LED Bar v2 device.

