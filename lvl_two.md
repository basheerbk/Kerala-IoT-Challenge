# Kerala-IoT-Challenge

# Experiment 1 -  Hello World LED Program Using Blynk App

> A basic Program similar to printing "*Hello World* " in any programming language. The Aim is to blink an LED using **Esp 32** and **Blynk App**

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
#define BLYNK_TEMPLATE_ID "TMPL72W3EGw5" // This has to be changed using your data
#define BLYNK_DEVICE_NAME "project1" // This has to be changed using your data

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
