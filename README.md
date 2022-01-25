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













































