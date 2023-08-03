# SM23-IOT-02
Smart methods 2023 internet of things feild
# Introduction:
The main objective of our task in the Internet of Things path requires you to make two Arduino pieces to communicate with each other with push button and LED connected between them. The LED on the second Arduino will light up when you press the button on the first Arduino piece. A pushbutton LED circuit is a fun and easy project that you can make with an Arduino board, LED light, two resistors, and some wires. 

<img width="726" alt="Screenshot 2023-08-03 221032" src="https://github.com/salman-akak/SM23-IOT-02/assets/139633858/ae084632-3447-41fe-91f4-2eb8dd1cebb6">


# The components:
1. Arduino
2. LED
3. Wires to connect
4. Resistors
5. Pushbutton
6. Arduino board

# simulation test:

https://github.com/salman-akak/SM23-IOT-02/assets/139633858/3405c68e-88a4-40e1-97b5-a66a351c74ff

# First Arduino code:
```
const int OUT_PIN = 4;

int buttonState ;

void setup()
{
  pinMode(OUT_PIN, OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  if(Serial.available() == 1) {
    buttonState = bitRead(Serial.read(), 0);
  }
  digitalWrite(OUT_PIN, buttonState);
  delay(1000);
}
```
# Seconed Arduino code:
```
const int inPin = 5;


void setup()
{
  pinMode(inPin, INPUT);
  Serial.begin(9600);
}

void loop()
{
  Serial.print( digitalRead(inPin));
  delay(1000);
}
```
# Tinkercad Link:

https://www.tinkercad.com/things/cvTL26FAMvB-two-arduino-connected-with-push-button-and-led/editel
