# Kerala-IoT-Challenge

> [**Foxlab Makerspace**](https://www.facebook.com/foxlabmakerspace/) in association with [**GTech - Group of Technology Companies**](https://atfg.gtechindia.org/) in Kerala is launching our prestigious program **“Kerala IoT Challenge 2021”**, with a vision to mould 100 IoT experts in Kerala, hosting on the µLearn platform. **Kerala IoT Challenge** is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, any learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.

<br>

### About Me
> _Hello Folks!_  I'm Muhammed Basheer. I'm a B.voc Automobile (Auto Electrical & Electronic) Student at _[**Farook college (autonomous)**](https://www.farookcollege.ac.in/),_ calicut. Always Interested in electronics & mechanics and to make DIY projects.

# Experiment 1 - Hello World LED Blinking

> A basic Program similar to printing "*Hello World* " in any programming language. The Aim is to blink an LED using **Arduino Uno Board**.

> Arduino Uno is an open-source microcontroller board developed by Arduino.cc. It has several advantages over the conventional microcontrollers. It comes with a pre-tested software and hardware libraries and has its own integrated development environment (IDE). Also it is less expensive & beginner friendly.

## Components Required  
* Arduino Uno Board 
* USB Cable 
* LED (Any Color) x 1 Nos
* 220 OHM Resistor X 1 Nos
* Breadboard 
* Jumper Wires (Male to Male ) X 2 Nos

## Circuit Diagram

![img1](https://github.com/basheerbk/Kerala-IoT-Challenge/blob/main/image/Screenshot%20(405).png?raw=true)

## Code

```

int ledPin = 10; // define digital pin 10.
void setup()
{
pinMode(ledPin, OUTPUT);// define pin with LED connected as output.
}
void loop()
{
digitalWrite(ledPin, HIGH); // set the LED on.
delay(1000); // wait for a second.
digitalWrite(ledPin, LOW); // set the LED off.
delay(1000); // wait for a second
}

```

## Output

> The LED is blinked with a time interval of 1 second
> ![img2](https://github.com/basheerbk/Kerala-IoT-Challenge/blob/main/image/20211104_155722.gif?raw=true)
 
