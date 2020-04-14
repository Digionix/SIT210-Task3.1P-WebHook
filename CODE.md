# SIT210-Task3.1P-WebHook
The code for my light sensing webhook task

```
int led = D7; 

int photoresistor = A0;


void setup() {

  pinMode(led, OUTPUT);
  pinMode(photoresistor, INPUT);
}


void loop() {

    digitalWrite(led, HIGH);
    
    
    
    String light = String(analogRead(photoresistor));
    
    Particle.publish("light", light, PRIVATE);
    delay(30000);
 
}
```
