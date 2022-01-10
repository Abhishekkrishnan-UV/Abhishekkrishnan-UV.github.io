## Kerala IOT Challenge.

## Kerala IOT Challenge Level-1.
Foxlab Makerspace in association with GTech - Group of Technology Companies in Kerala is launching our prestigious program  “Kerala IoT Challenge 2021”,  with a vision to mould 100 IoT experts in Kerala, hosting on the MuLearn platform. Kerala IoT Challenge is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.

## About Me.
Hi folks! I’m Abhishek krishnan U V , Computer Science Engineering student from College of Engineering ,Aranmula.
# Experiments.
## Experiment 1 - Hello World LED Blinking.
=> A basic Program similar to printing " Hello World " in any programming language. The Aim is to blink an LED using Arduino UNO Board.

### Components Required.
##### -> Arduino Uno Board.
##### -> USB Cable.
##### -> LED (Any Color) x 1 Nos.
##### -> 220 OHM Resistor X 1 Nos.
##### -> Breadboard.
##### -> Jumper Wires (Male to Male ) X 2 Nos.

### Circuit Diagram.
![Circuit diagram](https://user-images.githubusercontent.com/86780435/146665575-00e87a05-0644-42f9-8d55-d888a1b14409.png)

### The Code.

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

### Result.

=> Successfully blinked the LED in equal intervals of time.

### Output Video.


![Output Video](https://user-images.githubusercontent.com/86780435/146666882-c4fa0ac9-71b0-4555-9dce-946b33f04679.mp4)




## Experiment 2 : Traffic Light.

=> In the previous program, we have done the LED blinking experiment with one LED. Now, it’s time to up the stakes and do a bit more complicated experiment-traffic lights. Actually, these two experiments are similar. While in this traffic lights experiment, we use 3 LEDs with different colors rather than 1 LED.

### Components Required.

##### -> Arduino board *1.
##### -> USB cable *1.
##### -> Red M5 LED*1.
##### -> Yellow M5 LED*1.
##### -> Green M5 LED*1.
##### -> 220Ω resistor *3.

### Circuit Diagram.

![Circuit diagram](https://user-images.githubusercontent.com/86780435/146665599-cee2cbcf-75a3-4d4a-9585-c4a91c787144.png)


### The Code.

```
int redled =10; // initialize digital pin 8.
int yellowled =7; // initialize digital pin 7.
int greenled =4; // initialize digital pin 4.
void setup()
{
pinMode(redled, OUTPUT);// set the pin with red LED as “output”
pinMode(yellowled, OUTPUT); // set the pin with yellow LED as “output”
pinMode(greenled, OUTPUT); // set the pin with green LED as “output”
}
void loop()
{
digitalWrite(greenled, HIGH);//// turn on green LED
delay(5000);// wait 5 seconds

digitalWrite(greenled, LOW); // turn off green LED
for(int i=0;i<3;i++)// blinks for 3 times
{
delay(500);// wait 0.5 second
digitalWrite(yellowled, HIGH);// turn on yellow LED
delay(500);// wait 0.5 second
digitalWrite(yellowled, LOW);// turn off yellow LED
} 
delay(500);// wait 0.5 second
digitalWrite(redled, HIGH);// turn on red LED
delay(5000);// wait 5 seconds
digitalWrite(redled, LOW);// turn off red LED
}

```

### Result.

=> Like in the Traffic light scenerio successfully blinked the 3 LED's. The green LED stays on for about 5 second then turnsoff ,Now the yellow LED blinks 3 times with a time interval of 0.5 second , Then the red LED stays on for 5 seconds and goeson

### Output Video.


![Output Video](https://user-images.githubusercontent.com/86780435/146666904-195dbecc-7534-407e-91df-aa085b85cb80.mp4)
## Experiment 3 : LED Chasing Effect.

=> We often see billboards composed of colorful LEDs. They are constantly changing to form various light effects. In this experiment, we compile a program to simulate LED chasing effect. The long lead of LED is the positive side, short lead is negative.

### Components Required.

##### -> Led *6.
##### -> Arduino board *1.
##### -> 220Ω resistor *6.
##### -> Breadboard *1.
##### -> USB cable*1.
##### -> Breadboard wire *13.

## #Circuit Diagram.

![circuit diagram](https://user-images.githubusercontent.com/86780435/146665615-e7b274db-d50d-4f7c-8dde-94124480e44b.png)


### The Code.

```
int BASE = 2 ;  // the I/O pin for the first LED
int NUM = 6;   // number of LEDs
void setup()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     pinMode(i, OUTPUT);   // set I/O pins as output
   }
}
void loop()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, LOW);    // set I/O pins as “low”, turn off LEDs one by one.
     delay(200);        // delay
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);    // set I/O pins as “high”, turn on LEDs one by one
     delay(400);        // delay
   }  
}

```
### Result.
Successfully made the LED chase.

### Output Video.
![Output Video](https://user-images.githubusercontent.com/86780435/146666923-e93c43e9-1c18-448f-a20e-49e67ed208a0.mp4)












# Experiment 4: Button Controlled LED

> An experiment to light an LED using a Push Button.

## Components Required 

* Arduino Uno
* Button switch*1
* Red M5 LED*1
* 220ΩResistor*1
* 10KΩ Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*6
* USB cable*1

## Circuit Diagrams





## Code

```

int ledpin=11;// initialize pin 11
int inpin=7;// initialize pin 7
int val;// define val
void setup()
{
pinMode(ledpin,OUTPUT);// set LED pin as “output”
pinMode(inpin,INPUT);// set button pin as “input”
}
void loop()
{
val=digitalRead(inpin);// read the level value of pin 7 and assign if to val
if(val==LOW)// check if the button is pressed, if yes, turn on the LED
{ digitalWrite(ledpin,LOW);}
else
{ digitalWrite(ledpin,HIGH);}
}

```
## Output

> When the push button is pressed the LED is turned on otherwise it is off.





# Experiment 5 : Buzzer

> An experiment to understand the working of a buzzer.

## Components Required

* Arduino Uno
* Buzzer*1
* Breadboard*1
* Breadboard Jumper Wire*2
* USB cable*1


## Code

```

int buzzer=8;// initialize digital IO pin that controls the buzzer
void setup() 
{ 
  pinMode(buzzer,OUTPUT);// set pin mode as “output”
} 
void loop() 
{
digitalWrite(buzzer, HIGH); // produce sound
}

```

## Output

> The Buzzer makes beep sound.


# Experiment 6 : RGB LED

> An experiment to understand the working of a RGB LED.

## Components Required

* Arduino Uno
* USB Cable * 1
* RGB LED * 1
* Resistor *3
* Breadboard jumper wire*5

## Circuit Diagrams

## Code

```

int redpin = 11; //select the pin for the red LED
int bluepin =10; // select the pin for the blue LED
int greenpin =9;// select the pin for the green LED
int val;
void setup() {
  pinMode(redpin, OUTPUT);
  pinMode(bluepin, OUTPUT);
  pinMode(greenpin, OUTPUT);
  Serial.begin(9600);
}
void loop() 
{
for(val=255; val>0; val--)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
for(val=0; val<255; val++)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
 Serial.println(val, DEC);
}

```

## Output

> The RGB LED blinks.



# Experiment 7 - LDR Light Sensor

> An experiment to understand the working of an LDR light Sensor.

## LDR : Light Dependent Sensor

> Photo Resistor (Photovaristor) is a resistor whose resistance varies from different incident light strength. It's based on the photoelectric effect of semiconductor. If the incident light is intense, its resistance reduces; if the incident light is weak, the resistance increases.



## Components Required

* Arduino Uno Board
* Photo Resistor*1
* Red M5 LED*1
* 10KΩ Resistor*1
* 220Ω Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*7
* USB cable*1

## Circuit Diagrams

## Procedure

* Connect the 3.3v output of the Arduino to the positive rail of the breadboard
* Connect the ground to the negative rail of the breadboard
* Place the LDR on the breadboard
* Attach the 10K resistor to one of the legs of the LDR
* Connect the A0 pin of the Arduino to the same column where the LDR and resistor is connected (Since the LDR gives out an analog voltage, it is connected to the analog input pin on the Arduino. The Arduino, with its built-in ADC (Analog to Digital Converter), then converts the analog voltage from 0-5V into a digital value in the range of 0-1023). - Now connect the other end of the 10K resistor to the negative rail
* And the the second (free) leg of the LDR to the positive rail
Pretty much this is what we need for the light sensing. Basic circuits like this can be done without an Arduino aswell. However, if you want to log the values and use it to create charts, run other logics etc. I will recomend an Arduino or ESP8266 or may be a ESP32 for this.
Now, as we want our circuit to do something in the real world other than just displaying the values on the computer screen we will be attaching a LED to the circuit. The LED will turn on when its dark and will go off when its bright. To achieve this we will:
* Place the LED on the breadboard
* Connect the 220ohm resistor to the long leg (+ve) of the LED
* Then we will connect the other leg of the resistor to pin number 13 (digital pin) of the Arduino
* and the shorter leg of the LED to the negative rail of the breadboard

## Code

```

const int ledPin = 13;
const int ldrPin = A0;
void setup() {
Serial.begin(9600);
pinMode(ledPin, OUTPUT);
pinMode(ldrPin, INPUT);
}

void loop() {
int ldrStatus = analogRead(ldrPin);
if (ldrStatus <= 200) {
digitalWrite(ledPin, HIGH);
Serial.print("Its DARK, Turn on the LED : ");
Serial.println(ldrStatus);
} else {
digitalWrite(ledPin, LOW);
Serial.print("Its BRIGHT, Turn off the LED : ");
Serial.println(ldrStatus);
}
}

```

## Output


# Experiment 8 : Flame Sensor

> An experiment to understand the working of an Flame sensor.

## Flame Sensor

 **Usage**:These types of sensors are used for short range fire detection and can be used to monitor projects or as a safety precaution to cut devices off / on.

 **Range**:I have found this unit is mostly accurate up to about 3 feet.

 **How it works**:The flame sensor is very sensitive to IR wavelength at 760 nm ~ 1100 nm light.

**Analog output (A0)**: Real-time output voltage signal on the thermal resistance.

**Digital output (D0)**: When the temperature reaches a certain threshold, the output high and low signal threshold adjustable via potentiometer.

**Pins:**

* VCC - Positive voltage input: 5v for analog 3.3v for Digital.

* A0 - Analog output

* D0 - Digital output

* GND -  Ground

## Components Required

* Arduino UNO
* Flame Sensor
* LED
* Buzzer
* BreadBoard
* Jumper

## Circuit Diagrams

![1636554036921 1](https://user-images.githubusercontent.com/91405741/141130577-55ec7164-a222-4dac-8e57-ada3298bb18e.jpg)


   ## Code

```

const int buzzerPin = 12;
const int flamePin = 11;
int Flame = HIGH;
int redled = 5;
int greenled = 6;
void setup() 
{
  pinMode(buzzerPin, OUTPUT);
  pinMode(redled, OUTPUT);
  pinMode(greenled, OUTPUT);

  pinMode(flamePin, INPUT);
  Serial.begin(9600);
}

void loop() 
{
  Flame = digitalRead(flamePin);
  if (Flame== LOW)
  {
    digitalWrite(buzzerPin, HIGH);
    digitalWrite(redled, HIGH);
    digitalWrite(greenled, LOW);
  }
  else
  {
    digitalWrite(buzzerPin, LOW);
    digitalWrite(greenled, HIGH);
    digitalWrite(redled, LOW);
  }
}

```

## Output



# Experiment 9 : LM35 Temperature Sensor

> An experiment to understand the working of an LM35 Temperature Sensor.

## LM35 Temperature Sensor
