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






![circuit diagram 1](https://user-images.githubusercontent.com/86780435/150275220-c1586270-47d5-49af-940b-d59714ae1a15.png)



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


### Output .


![exp 1](https://user-images.githubusercontent.com/86780435/150972954-eabdb4b7-66a6-41eb-a49d-9a10c8b3148c.png)



### Result.

=> Successfully blinked the LED in equal intervals of time.


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





![circuit diagram 2](https://user-images.githubusercontent.com/86780435/150275179-195253f6-8f31-4366-9241-978cd1cdfa34.png)




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


### Output.

![exp2 1](https://user-images.githubusercontent.com/86780435/150973892-25f26955-d516-4d18-ae86-d76712bb294f.png)

![exp2 2](https://user-images.githubusercontent.com/86780435/150973931-7c1e0dc2-cdb4-4186-b5be-3d37c9c15b21.png)



![exp2 3](https://user-images.githubusercontent.com/86780435/150973944-42e9f374-63cf-4d52-bba5-4394fc2f6a74.png)


### Result.

=> Like in the Traffic light scenerio successfully blinked the 3 LED's.


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




![circuit diagram 3](https://user-images.githubusercontent.com/86780435/150275118-49183a1e-4486-4b54-87fd-1ca8653c9f28.png)

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


### Output.





![exp3](https://user-images.githubusercontent.com/86780435/150974403-82f7b4f6-163a-474a-8394-fb909d8ed26a.png)




### Result.
Successfully made the LED chase.





## Experiment 4: Button Controlled LED

=> An experiment to light an LED using a Push Button.

### Components Required 

##### -> Arduino Uno
##### -> Button switch*1
##### -> Red M5 LED*1
##### -> 220ΩResistor*1
##### -> 10KΩ Resistor*1
##### -> Breadboard*1
##### -> Breadboard Jumper Wire*6
##### -> USB cable*1

### Circuit Diagrams




![circuit diagram 4 1](https://user-images.githubusercontent.com/86780435/150274912-f3bc9710-5294-431a-9c00-a135d5d2d5d8.png)




![circuit diagram 4 2](https://user-images.githubusercontent.com/86780435/150274951-1a3cba2f-5b93-4e4f-b919-e21be70f4fc8.png)





![circuit diagram 4 3](https://user-images.githubusercontent.com/86780435/150274973-98dc4784-7e3b-45aa-85e4-493f6e1f8913.png)

### Code

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

### Output.



![exp4](https://user-images.githubusercontent.com/86780435/150974932-3a8aa0ba-4289-4bee-aaf7-a98cb96f7ca8.jpeg)




### Result.
Successfully light the LED using a Push Button.









## Experiment 5 : Buzzer

=> An experiment to understand the working of a buzzer.

### Components Required

#### -> Arduino Uno
#### -> Buzzer*1
#### -> Breadboard*1
#### -> Breadboard Jumper Wire*2
#### -> USB cable*1
### Circuit Diagrams.


![circuit diagram 5 1](https://user-images.githubusercontent.com/86780435/150277393-50ca1028-8ce0-4939-a7e6-fbdbf45c5e7d.png)




![circuit diagram 5 2](https://user-images.githubusercontent.com/86780435/150277401-4590daa8-9c11-4a3a-b37d-d61c0ca4cd42.png)




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

### Output.



![exp5](https://user-images.githubusercontent.com/86780435/150975186-e8d221e7-4093-4cf1-b762-943ab2a6a9a9.jpeg)




### Result.
Successfully made the Buzzer makes beep sound.







## Experiment 6 : RGB LED

=> An experiment to understand the working of a RGB LED.

### Components Required

#### -> Arduino Uno
#### -> USB Cable * 1
#### -> RGB LED * 1
#### -> Resistor *3
#### -> Breadboard jumper wire*5

### Circuit Diagrams

![circuit diagram 6 1](https://user-images.githubusercontent.com/86780435/150277992-330854f9-00e2-4a83-b99e-53a1265bd3d8.png)


![circuit diagram 6 2](https://user-images.githubusercontent.com/86780435/150278007-ef4d2a56-7eb2-41b6-953c-51c62ecbb07d.png)





### Code

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
### Output.


![exp6](https://user-images.githubusercontent.com/86780435/150975373-179f986c-5374-4c4b-b0d2-7d160ca67c4e.jpeg)




### Result.
Successfully blinked the RGB LED.





## Experiment 7 - LDR Light Sensor
### * LDR : Light Dependent Sensor
=> An experiment to understand the working of an LDR light Sensor.



-> Photo Resistor (Photovaristor) is a resistor whose resistance varies from different incident light strength. It's based on the photoelectric effect of semiconductor. If the incident light is intense, its resistance reduces; if the incident light is weak, the resistance increases.



### Components Required

#### -> Arduino Uno Board
#### -> Photo Resistor*1
#### -> Red M5 LED*1
#### -> 10KΩ Resistor*1
#### -> 220Ω Resistor*1
#### -> Breadboard*1
#### -> Breadboard Jumper Wire*7
#### -> USB cable*1

### Circuit Diagrams

![circuitdiag 7 1](https://user-images.githubusercontent.com/86780435/150975766-1bba5ed3-acc3-4999-ad20-7680f401b2d3.png)



![circuitdiag7 2](https://user-images.githubusercontent.com/86780435/150976744-80ce7388-7717-443a-add9-ee83928fb735.png)



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


![exp7](https://user-images.githubusercontent.com/86780435/150976042-2b9673fc-3c36-4782-9957-8a7f96aa4d66.jpeg)


### Result.
Successfully obtained the result.






















## Experiment 8 : Flame Sensor

=> An experiment to understand the working of an Flame sensor.



### Components Required

#### -> Arduino Uno Board*1
#### -> Flame Sensor *1
#### -> Buzzer *1
#### -> 10K Resistor *1
#### -> Breadboard Jumper Wire*6
#### -> USB cable*1

### Circuit Diagrams


![circuit diagram 8 1](https://user-images.githubusercontent.com/86780435/151684550-36a6061e-c25d-4f8b-b269-e2f1b2bf1eba.png)


![circuit diagram 8 2](https://user-images.githubusercontent.com/86780435/151684552-0ae24c40-1c56-4e62-8d48-8c4f0e9bbe42.png)





   ## Code

```

int flame=0;// select analog pin 0 for the sensor
int Beep=9;// select digital pin 9 for the buzzer
int val=0;// initialize variable
 void setup() 
{
  pinMode(Beep,OUTPUT);// set LED pin as “output”
 pinMode(flame,INPUT);// set buzzer pin as “input”
 Serial.begin(9600);// set baud rate at “9600”
 } 
void loop() 
{ 
  val=analogRead(flame);// read the analog value of the sensor 
  Serial.println(val);// output and display the analog value
  if(val>=600)// when the analog value is larger than 600, the buzzer will buzz
  {  
   digitalWrite(Beep,HIGH); 
   }else 
   {  
     digitalWrite(Beep,LOW); 
    }
   delay(500); 
}
```

### Output.

![exp8](https://user-images.githubusercontent.com/86780435/151684779-4d360477-563f-4db5-b22d-fc5954868fd3.jpeg)




### Result.
Successfully sensed flame with the experiment.




## Experiment 9 : LM35 Temperature Sensor

=> An experiment to understand the working of an LM35 Temperature Sensor.

### LM35 Temperature Sensor
LM35 is a widely used temperature sensor with many different package types. At room temperature,
it can achieve the accuracy of ±1/4°C without additional calibration processing.

LM35 temperature sensor can produce different voltage by different temperature
When temperature is 0 ℃, it outputs 0V; if increasing 1 ℃, the output voltage will increase 10 mv.




### Components Required.

#### -> Arduino Uno  Board*1
#### -> LM35*1
#### -> Breadboard*1
#### -> Breadboard Jumper Wire*5
#### -> USB cable*

## Circuit Diagrams.

![circuit diagram 9 1](https://user-images.githubusercontent.com/86780435/151684945-330d9193-af59-419b-bcfa-12ddf2024b0d.png)

![circuit diagram 9 2](https://user-images.githubusercontent.com/86780435/151684949-3dda1394-2fb5-466b-ae53-e48e5415f7a6.png)


## Code

```
int potPin = 0; // initialize analog pin 0 for LM35 temperature sensor
void setup()
{
Serial.begin(9600);// set baud rate at”9600”
}
void loop()
{
int val;// define variable
int dat;// define variable
val=analogRead(0);// read the analog value of the sensor and assign it to val
dat=(125*val)>>8;// temperature calculation formula
Serial.print("Tep");// output and display characters beginning with Tep
Serial.print(dat);// output and display value of dat
Serial.println("C");// display “C” characters
delay(500);// wait for 0.5 second
}
```

## Output.




### Result.
Successfully obtained temperature using LM35.





## Experiment 10:IR Remote Control Using TSOP

=> An experiment to understand the working of IR Remote Control using TSOP.

### Components Required.
#### -> Arduino Uno Board*1
#### -> Infrared Remote Controller(You can use TV Remote or any other remote) *1
#### -> Infrared Receiver *1
#### -> LED *6
#### -> 220ΩResistor *6
#### -> Breadboard Wire *11
#### -> USB cable*1


### Circuit Diagrams.

![circuit diagram 10 1](https://user-images.githubusercontent.com/86780435/151685062-e63425d0-13ae-4591-83e0-bd984d123fe8.png)

![circuit diagram 10 2](https://user-images.githubusercontent.com/86780435/151685063-e2e68b0d-cc57-4dac-a3a9-21c9a547a195.png)


### Code.

```

#include <IRremote.h>
int RECV_PIN = 11;
int LED1 = 2;
int LED2 = 3;
int LED3 = 4;
int LED4 = 5;
int LED5 = 6;
int LED6 = 7;
long on1  = 0x00FF6897;
long off1 = 0x00FF9867;
long on2 = 0x00FFB04F;
long off2 = 0x00FF30CF;
long on3 = 0x00FF18E7;
long off3 = 0x00FF7A85;
long on4 = 0x00FF10EF;
long off4 = 0x00FF38C7;
long on5 = 0x00FF5AA5;
long off5 = 0x00FF42BD;
long on6 = 0x00FF4AB5;
long off6 = 0x00FF52AD;
IRrecv irrecv(RECV_PIN);
decode_results results;
// Dumps out the decode_results structure.
// Call this after IRrecv::decode()
// void * to work around compiler issue
//void dump(void *v) {
//  decode_results *results = (decode_results *)v
void dump(decode_results *results) {
  int count = results->rawlen;
  if (results->decode_type == UNKNOWN) 
    {
     Serial.println("Could not decode message");
    } 
  else 
   {
    if (results->decode_type == NEC) 
      {
       Serial.print("Decoded NEC: ");
      } 
    else if (results->decode_type == SONY) 
      {
       Serial.print("Decoded SONY: ");
      } 
    else if (results->decode_type == RC5) 
      {
       Serial.print("Decoded RC5: ");
      } 
    else if (results->decode_type == RC6) 
      {
       Serial.print("Decoded RC6: ");
      }
     Serial.print(results->value, HEX);
     Serial.print(" (");
     Serial.print(results->bits, DEC);
     Serial.println(" bits)");
   }
     Serial.print("Raw (");
     Serial.print(count, DEC);
     Serial.print("): ");
 for (int i = 0; i < count; i++) 
     {
      if ((i % 2) == 1) {
      Serial.print(results->rawbuf[i]*USECPERTICK, DEC);
     } 
    else  
     {
      Serial.print(-(int)results->rawbuf[i]*USECPERTICK, DEC);
     }
    Serial.print(" ");
     }
      Serial.println("");
     }
void setup()
 {
  pinMode(RECV_PIN, INPUT);   
  pinMode(LED1, OUTPUT);
  pinMode(LED2, OUTPUT);
  pinMode(LED3, OUTPUT);
  pinMode(LED4, OUTPUT);
  pinMode(LED5, OUTPUT);
  pinMode(LED6, OUTPUT);  
  pinMode(13, OUTPUT);
  Serial.begin(9600);
   irrecv.enableIRIn(); // Start the receiver
 }
int on = 0;
unsigned long last = millis();
void loop() 
{
  if (irrecv.decode(&results)) 
   {
    // If it's been at least 1/4 second since the last
    // IR received, toggle the relay
    if (millis() - last > 250) 
      {
       on = !on;
//       digitalWrite(8, on ? HIGH : LOW);
       digitalWrite(13, on ? HIGH : LOW);
       dump(&results);
      }
    if (results.value == on1 )
       digitalWrite(LED1, HIGH);
    if (results.value == off1 )
       digitalWrite(LED1, LOW); 
    if (results.value == on2 )
       digitalWrite(LED2, HIGH);
    if (results.value == off2 )
       digitalWrite(LED2, LOW); 
    if (results.value == on3 )
       digitalWrite(LED3, HIGH);
    if (results.value == off3 )
       digitalWrite(LED3, LOW);
    if (results.value == on4 )
       digitalWrite(LED4, HIGH);
    if (results.value == off4 )
       digitalWrite(LED4, LOW); 
    if (results.value == on5 )
       digitalWrite(LED5, HIGH);
    if (results.value == off5 )
       digitalWrite(LED5, LOW); 
    if (results.value == on6 )
       digitalWrite(LED6, HIGH);
    if (results.value == off6 )
       digitalWrite(LED6, LOW);        
    last = millis();      
irrecv.resume(); // Receive the next value
  }
}

```

### Output.


![exp10](https://user-images.githubusercontent.com/86780435/151685127-ed3ea1ac-c16c-4c8a-ac81-6e00eb1ac1f2.jpeg)




### Result.
Successfully obtained the result.




## Experiment 11 :Potentiometer analog Value Reading.

=> An experiment to understand the working of Potentiometer.

### Components Required

#### -> Arduino Uno Board*1]

#### -> 10K Potentiometer *1

#### -> Breadboard*1

#### -> Breadboard Jumper Wire*3

#### -> USB cable*1



### Circuit Diagrams.
![circuit diagram 11 1](https://user-images.githubusercontent.com/86780435/151685199-0eba6d17-5c7c-45af-8698-54eb034d03c9.png)


![circuit digram 11 2](https://user-images.githubusercontent.com/86780435/151685200-2e907c1b-8067-474d-8e35-388e35e33efe.png)




### Code.

```

int potpin=0;// initialize analog pin 0
int ledpin=13;// initialize digital pin 13
int val=0;// define val, assign initial value 0
void setup()
{
pinMode(ledpin,OUTPUT);// set digital pin as “output”
Serial.begin(9600);// set baud rate at 9600
}
void loop()
{
digitalWrite(ledpin,HIGH);// turn on the LED on pin 13
delay(50);// wait for 0.05 second
digitalWrite(ledpin,LOW);// turn off the LED on pin 13
delay(50);// wait for 0.05 second
val=analogRead(potpin);// read the analog value of analog pin 0, and assign it to val 
Serial.println(val);// display val’s value
}
```

### Output


![exp 11 2](https://user-images.githubusercontent.com/86780435/151685243-4e6d8997-68d8-417d-a6fd-b59f867c9956.jpeg)



![exp11 1](https://user-images.githubusercontent.com/86780435/151685254-be37f6f6-c5bf-4d38-b95e-473f15c78361.jpeg)

### Result.
Successfully obtained the analog value of potentiometer.


## Experiment 12 : 7 Segment Display.
        
=> An experiment to understand the working of 7 Segment Display.

### Components Required.

#### -> Arduino Uno Board*1
#### -> 1-digit LED Segment Display*1
#### -> 220Ω Resistor*8
#### -> Breadboard*1
#### -> Breadboard Jumper Wires *several
#### -> USB cable*1


### Circuit Diagrams.

![circuit diagram 12 1](https://user-images.githubusercontent.com/86780435/151685507-fb81e2eb-7b51-4d1e-9b96-5b65501ba86b.png)
![circuit diagram 12 2](https://user-images.githubusercontent.com/86780435/151685514-4b45b6c8-4538-43f2-a940-80da055083a3.png)




### Code.

```

int a=7;// set digital pin 7 for segment a
int b=6;// set digital pin 6 for segment b
int c=5;// set digital pin 5 for segment c
int d=10;// set digital pin 10 for segment d
int e=11;// set digital pin 11 for segment e
int f=8;// set digital pin 8 for segment f
int g=9;// set digital pin 9 for segment g
int dp=4;// set digital pin 4 for segment dp
void digital_0(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
}
void digital_1(void) // display number 1
{
unsigned char j;
digitalWrite(c,HIGH);// set level as “high” for pin 5, turn on segment c
digitalWrite(b,HIGH);// turn on segment b
for(j=7;j<=11;j++)// turn off other segments
digitalWrite(j,LOW);
digitalWrite(dp,LOW);// turn off segment dp
}
void digital_2(void) // display number 2
{
unsigned char j;
digitalWrite(b,HIGH);
digitalWrite(a,HIGH);
for(j=9;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
digitalWrite(c,LOW);
digitalWrite(f,LOW);
}
void digital_3(void) // display number 3
{digitalWrite(g,HIGH);
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(dp,LOW);
digitalWrite(f,LOW);
digitalWrite(e,LOW);
}
void digital_4(void) // display number 4
{digitalWrite(c,HIGH);
digitalWrite(b,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
digitalWrite(a,LOW);
digitalWrite(e,LOW);
digitalWrite(d,LOW);
}
void digital_5(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b, LOW);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void digital_6(void) // display number 6
{
unsigned char j;
for(j=7;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(c,HIGH);
digitalWrite(dp,LOW);
digitalWrite(b,LOW);
}
void digital_7(void) // display number 7
{
unsigned char j;
for(j=5;j<=7;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
for(j=8;j<=11;j++)
digitalWrite(j,LOW);
}
void digital_8(void) // display number 8
{
unsigned char j;
for(j=5;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
}
void digital_9(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void setup()
{
int i;// set variable
for(i=4;i<=11;i++)
pinMode(i,OUTPUT);// set pin 4-11as “output”
}
void loop()
{
while(1)
{
digital_0();// display number 0
delay(1000);// wait for 1s
digital_1();// display number 1
delay(1000);// wait for 1s
digital_2();// display number 2
delay(1000); // wait for 1s
digital_3();// display number 3
delay(1000); // wait for 1s
digital_4();// display number 4
delay(1000); // wait for 1s
digital_5();// display number 5
delay(1000); // wait for 1s
digital_6();// display number 6
delay(1000); // wait for 1s
digital_7();// display number 7
delay(1000); // wait for 1s
digital_8();// display number 8
delay(1000); // wait for 1s
digital_9();// display number 9
delay(1000); // wait for 1s
}}
```

### Output.
![exp12](https://user-images.githubusercontent.com/86780435/151685619-d882f895-f687-40d2-8bbd-384adbb01427.jpeg)



### Result.
Successfully blinked numbers from 0 to 9.





















