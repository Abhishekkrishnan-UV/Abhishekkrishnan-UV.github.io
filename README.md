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
### Result.
Successfully made the LED chase.

### Output Video.
![Output Video](https://user-images.githubusercontent.com/86780435/146666923-e93c43e9-1c18-448f-a20e-49e67ed208a0.mp4)






## Experiment 4: Button Controlled LED

> An experiment to light an LED using a Push Button.

### Components Required 

##### Arduino Uno
##### Button switch*1
##### Red M5 LED*1
##### 220ΩResistor*1
##### 10KΩ Resistor*1
##### Breadboard*1
##### Breadboard Jumper Wire*6
##### USB cable*1

### Circuit Diagrams




![circuit diagram 4 1](https://user-images.githubusercontent.com/86780435/150274912-f3bc9710-5294-431a-9c00-a135d5d2d5d8.png)




![circuit diagram 4 2](https://user-images.githubusercontent.com/86780435/150274951-1a3cba2f-5b93-4e4f-b919-e21be70f4fc8.png)





![circuit diagram 4 3](https://user-images.githubusercontent.com/86780435/150274973-98dc4784-7e3b-45aa-85e4-493f6e1f8913.png)

### Code



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

### Result.
Successfully light the LED using a Push Button.


### Output

> When the push button is pressed the LED is turned on otherwise it is off.













