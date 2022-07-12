# Kerala-IoT-Challenge

# Experiment 1 -  Hello World LED Program Using Blynk App

> A basic Program similar to printing "*Hello World* " in any programming language. The Aim is to controll (On/Off) an LED using **Esp 32** and **Blynk App**

> ESP32 is a series of low-cost, low-power system on a chip microcontrollers with integrated Wi-Fi and dual-mode Bluetooth.
[click here to know more about Esp 32](https://en.wikipedia.org/wiki/ESP32) 

## Components Required  
* ESP 32 Development Board 
* USB Cable 
* LED (Any Color) x 1 Nos
* Breadboard 
* Jumper Wires (Male to Male ) X 2 Nos


## Circuit Diagram

![image](https://user-images.githubusercontent.com/49371247/152683254-d48f2a72-1b8d-48e6-92ed-5a02a308c243.png)

## Code

```
// Fill-in information from your Blynk Template here
#define BLYNK_TEMPLATE_ID "TMPL72W3EGw5" // This has to be changed using your Template ID.
#define BLYNK_DEVICE_NAME "project1" // This has to be changed using your Device Name.

#define BLYNK_FIRMWARE_VERSION        

#define BLYNK_PRINT Serial
//#define BLYNK_DEBUG

#define APP_DEBUG

// Uncomment your board, or configure a custom board in Settings.h
//#define USE_WROVER_BOARD
//#define USE_TTGO_T7
//#define USE_ESP32C3_DEV_MODULE
//#define USE_ESP32S2_DEV_KIT

#include "BlynkEdgent.h"
BLYNK_WRITE(V0)
{
  int pinValue = param.asInt();
  digitalWrite(15,pinValue); 
}
      
void setup()
{
  pinMode(15,OUTPUT);
  Serial.begin(115200);
  delay(100);

  BlynkEdgent.begin();
}

void loop() {
  BlynkEdgent.run();
}

```

## Procedure

* First connect the LED to ESP32 using breadboard and other components.
* LED positive pin is connected to ESP32 pin no 15.
* LED negative pin is connected to ESP32 GND pin.
* Program the ESP32.  
* Create Templates in BLynk IoT webapp and mobile app. [(Resources)](https://docs.blynk.io/en/t) 
* Connect the ESP32 to wifi network.
* Controll the LED using  BLynk IoT webapp and mobile app.

## Output
![gif](https://github.com/basheerbk/Kerala-IoT-Challenge/blob/main/image/lvl2/20220206_203611.gif?raw=true)

----------------------------------------------------------------------------------------


# Experiment 2 -  LED Control Using Arduino IoT Cloud

> A basic Program similar to printing "*Hello World* " in any programming language. The Aim is to controll (On/Off) an LED using **Esp 32** and **Ardunio IoT Cloud**
> ESP32 is a series of low-cost, low-power system on a chip microcontrollers with integrated Wi-Fi and dual-mode Bluetooth.
[click here to know more about Esp 32](https://en.wikipedia.org/wiki/ESP32) 
> Arduino IoT cloud is a online platform that makes it easy for you to create, deploy and monitor IoT projects.
[click here to know more about Arduino IoT cloud](https://docs.arduino.cc/cloud/iot-cloud)

## Components Required  
* ESP 32 Development Board 
* USB Cable 
* LED (Any Color) x 1 Nos
* Breadboard 
* Jumper Wires (Male to Male ) X 2 Nos


## Circuit Diagram

![image](https://user-images.githubusercontent.com/49371247/152683254-d48f2a72-1b8d-48e6-92ed-5a02a308c243.png)

## Code

```
#include "thingProperties.h"

void setup() {
  // Initialize serial and wait for port to open:
  Serial.begin(9600);
  pinMode(2, OUTPUT);
  // This delay gives the chance to wait for a Serial Monitor without blocking if none is found
  delay(1500);

  // Defined in thingProperties.h
  initProperties();

  // Connect to Arduino IoT Cloud
  ArduinoCloud.begin(ArduinoIoTPreferredConnection);

  /*
     The following function allows you to obtain more information
     related to the state of network and IoT Cloud connection and errors
     the higher number the more granular information you’ll get.
     The default is 0 (only errors).
     Maximum is 4
  */
  setDebugMessageLevel(2);
  ArduinoCloud.printDebugInfo();
}

void loop() {
  ArduinoCloud.update();
  
}

/*
  Since LED is READ_WRITE variable, onLEDChange() is
  executed every time a new value is received from IoT Cloud.
*/
void onLEDChange()  {
  if (LED == 1)
  {
    digitalWrite(2, HIGH);
  }
  else
  {
    digitalWrite(2, LOW);
  }
}

```

## Procedure

* First connect the LED to ESP32 using breadboard and other components.
* LED positive pin is connected to ESP32 pin no 15.
* LED negative pin is connected to ESP32 GND pin.
* Program the ESP32.  
* Create Templates in BLynk IoT webapp and mobile app. [(Resources)](https://docs.blynk.io/en/t) 
* Connect the ESP32 to wifi network.
* Controll the LED using  BLynk IoT webapp and mobile app.

## Output
![gif](https://github.com/basheerbk/Kerala-IoT-Challenge/blob/main/image/lvl2/20220206_203611.gif?raw=true)


