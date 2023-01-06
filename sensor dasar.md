<h1> contoh penggunaan sensor: </h1>
<h4> sensor garis </h4>

```
int pinSensor = ; // sensor terhubung di pin yang mana?
int pinLed = ; // lampu terhubung di pin yang mana?
int nilaiSensor = ; // deklarasi nilai awal 

void setup()
{
  pinMode(pinSensor, INPUT);
  pinMode(pinLed, OUTPUT);
  Serial.begin (9600); //Arduino UNO
}

void loop()
{
  nilaiSensor = digitalRead (pinSensor);
  
  if(nilaiSensor == HIGH)
  {
    digitalWrite(pinLed, HIGH);
    delay(10);
  }
  else
  {
    digitalWrite(pinLed, LOW);
    delay(10);
  }
}
```

<h4> sensor </h4>
