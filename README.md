# IOT<br>
**1.Led**<br>
https://wokwi.com/projects/333797681637884499<br>
**2.RGB Led**<br>
https://wokwi.com/projects/333806304312164946<br>
**3.LCD**<br>
https://wokwi.com/projects/333806812650275412<br>
**4.Working mechanisum of sensors.**<br>
1. TEMPERATURE AND HUMIDITY SENSOR(DHT 11 OR 22)<br>
  https://wokwi.com/projects/334344603757970004<br>
**5.LED FADE**<br>
https://wokwi.com/projects/334432276838351443<br>
**6.LED BUTTON**<br>
https://wokwi.com/projects/334432996451942995<br>
**7.MOTION SENSOR**<br>
https://wokwi.com/projects/334433368049451603<br>
**8.MOTION SENSOR LED**<br>
https://wokwi.com/projects/334433905259053652<br>
**9.MOTION SENSOR BUZZER**<br>
https://wokwi.com/projects/334434209121698387<br>
**10.ULTRASONIC SENSOR BUZZER**<br>
https://wokwi.com/projects/334434683419886163<br>
**11.ULTRASONIC SENSOR LED**<br>
https://wokwi.com/projects/334435063403905619<br>
**12.SERVO MOTOR**<br>
https://wokwi.com/projects/334975755701191250<br>
**13.POTENTIOMETER**<BR>
https://wokwi.com/projects/334976640674169428<br>
**14.BUTTON SERVO MOTOR**<br>
https://wokwi.com/projects/334977594216677971<br>
**15.ULTRASONIC SENSOR SERVO**<br>
https://wokwi.com/projects/334979742549672530<br>
**16.BUZZER BEEP**<br>
https://wokwi.com/projects/335609032411710035<br>
**17.BUZZER BEEP USING PUSHBUTTON**<br>
https://wokwi.com/projects/335610024201028179<br>
**18.BUZZER BEEP USING ULTRASONIC SENSOR**<br>
https://wokwi.com/projects/335610780015657556<br>
**19.BUZZER BEEP USING ULTRASONIC SENSOR AND LED**<br>
https://wokwi.com/projects/335610780015657556<br>
**20.ULTRASONIC SENSOR**<br>
https://wokwi.com/projects/335699322789167698<br>
**21.POTENTIOMETER**<br>
https://wokwi.com/projects/335700904365785682<br>
**22.POTENIOMETER FADE LED**<br>
https://wokwi.com/projects/335703475977454163<br>
**23.LED IN ESP32**<br>
https://wokwi.com/projects/336968090979926612<br>
**24.LED WITH BUZZER**<br>
https://wokwi.com/projects/337602112497123922<br>
**25. LED with PUSH BUTTON**<br>
https://wokwi.com/projects/334431214876230226<br>
**26.DHT 22 sensor<br>**
https://wokwi.com/projects/337603663792964179<br>
**27. relay with arduino ie Servo motor with BUTTON**<br>
https://wokwi.com/projects/337603967810798163<br>
**28. LCD DHT 22**<br>
https://wokwi.com/projects/337605922532622930<br>
**29.RGB**<br>
int red = D1;<br>
 int green = D6;<br>
 int blue = D7;<br>
 //GROUND IS CONNECTED TO 3V <br>
 void setup() {<br>
   pinMode(red, OUTPUT);<br>
   pinMode(green, OUTPUT);<br>
   pinMode(blue, OUTPUT);<br>

 }<br>

 void loop() {<br>
   displayColor(0b100); //RED<br>
   delay(1000);<br>
   displayColor(0b010); //GREEN<br>
   delay(1000);<br>
   displayColor(0b001); //BLUE<br>
   delay(1000);<br>
   displayColor(0b101); //MAGENTA<br>
   delay(1000);<br>
   displayColor(0b011); //CYAN<br>
   delay(1000);<br>
   displayColor(0b110); //YELLOW<br>
   delay(1000);<br>
   displayColor(0b111); //WHITE<br>
   delay(1000);<br>
 }<br>

 void displayColor(byte color) {<br>
   digitalWrite(red, !bitRead(color, 2));<br>
   digitalWrite(green, !bitRead(color, 1));<br>
   digitalWrite(blue, !bitRead(color, 0));<br>
 }<br>
<br>
<br>
**30.IR LED**<br>
int ir=D7;<br>
 int led=D5;<br>
 void setup() {<br>
   // put your setup code here, to run once:<br>
   pinMode(ir,INPUT);<br>
     pinMode(led,OUTPUT);<br>
     Serial.begin(9600);<br>

 }<br>

 void loop() {<br>
   // put your main code here, to run repeatedly:<br>
   int irvalue=digitalRead(ir);<br>
   if(irvalue==LOW)<br>
   {<br>
     Serial.println("LOW");<br>
     digitalWrite(led,HIGH);<br>
   }<br>
   else<br>
   {<br>
     Serial.println("HIGH");<br>
     digitalWrite(led,LOW);<br>
   }<br>
 delay(100);<br>
 }<br>
     LDR<br>
     const int ldrPin=A0;<br>
     void setup() {<br>
       Serial.begin(9600);<br>
       pinMode(ldrPin,INPUT);<br>
     }<br>
     void loop() {<br>
       int rawData = analogRead(ldrPin);   <br>
       Serial.println(rawData);<br>
       delay(1000);<br>
     }<br>
     <br>
     <br>
**31.LDR LED**<br>
int ldr=A0;//Set A0(Analog Input) for LDR.<br>
 int value=0;<br>
 int led=D1;<br>
 void setup() {<br>
 Serial.begin(9600);<br>
 pinMode(led,OUTPUT);<br>
 }<br>

 void loop() {<br>
 value=analogRead(ldr);//Reads the Value of LDR(light).<br>
 Serial.println("LDR value is :");//Prints the value of LDR to Serial Monitor.<br>
 Serial.println(value);<br>
 if(value<50)<br>
   {<br>
     digitalWrite(led,HIGH);//Makes the LED glow in Dark.<br>
   }<br>
   else<br>
   {<br>
     digitalWrite(led,LOW);//Turns the LED OFF in Light.<br>
   }<br>
   delay(1000);<br>
 }\<br>
<br>
<br>
**32.LED CHASER**<br>
 int pinsCount=6;                        // declaring the integer variable pinsCount<br>
int pins[] = {D0,D1,D7,D5,D3,D2};          // declaring the array pins[]<br>
void setup() { <br>
  for (int i=0; i<pinsCount; i=i+1){    // counting the variable i from 0 to 9<br>
    pinMode(pins[i], OUTPUT);            // initialising the pin at index i of the array of pins as OUTPUT<br>
  }<br>
}<br>

void loop() {<br>
  for (int i=0; i<pinsCount; i=i+1){    // chasing right<br>
    digitalWrite(pins[i], HIGH);         // switching the LED at index i on<br>
    delay(100);                          // stopping the program for 100 milliseconds<br>
    digitalWrite(pins[i], LOW);          // switching the LED at index i off<br>
  }<br>
  for (int i=pinsCount-1; i>0; i=i-1){   // chasing left (except the outer leds)<br>
   digitalWrite(pins[i], HIGH);         // switching the LED at index i on<br>
    delay(100);                          // stopping the program for 100 milliseconds<br>
    digitalWrite(pins[i], LOW);          // switching the LED at index i off<br>
}<br>
}<br>
<br>
<br>
**33.LIQUID CRYSTAL**<br>
https://wokwi.com/projects/340779306417390164<br>
**34.Seven segment LED display**<br>
https://wokwi.com/projects/libraries/SevSeg/SevSeg_Counter<br>
**35.Analog Joystick with two axes (horizontal/vertical) and an integrated push button.**<br>
https://wokwi.com/projects/296234816685212169<br>
**36.DHT22 on the ESP32 **<br>
https://wokwi.com/projects/322410731508073042<br>
**37.Display distance on LCD screen with buzzer and LED Reference 1:- **<br>







 
  
  

  

  
  
  

  


