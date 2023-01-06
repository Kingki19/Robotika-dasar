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

<h4> sensor ultrasonik </h4>

```
int pinTrigger = ; // letak pin trigger
int pinEcho = ; // letak pin echo
long durasi;
float cm, inch;

void setup()
{
  Serial.begin(9600); // Arduino UNO
  pinMode (pinTrigger, OUTPUT);
  pinMode (pinEcho, INPUT);
}

void loop()
{
  digitalWrite(pinTrigger, LOW);
  delay(0.2);
  digitalWrite(pinTrigger, HIGH);
  delay(0.2);
  digitalWrite(pinTrigger, LOW);
  delay(0.2);
  
  durasi = pulseIn(pinEcho, HIGH);
  cm = (durasi * 0.0343) / 2;
  inch = cm / 2.54;
  Serial.print(cm); Serial.print(" cm\t");
  Serial.print(inch); Serial.println(" Inch");
  delay(50);
}
```
<h4> sensor api </h4>

```
int pinSensor = ; // letak pin sensor api
int bacaSensor = 0; // deklarasi nilai awal variabel

void setup()
{
  pinMode(pinSensor, INPUT);
  Serial.begin(9600); // Arduino UNO
}

void loop()
{
  bacaSensor = digitalRead(pinSensor);
  if(bacaSensor == HIGH)
  {
    Serial.print("Digital value: ")
    serial.println(bacaSensor);
    Serial.println("Ada api coy!");
    delay(1000);
  }
  else
  {
    Serial.print("Digital value: ")
    serial.println(bacaSensor);
    Serial.println("Sans, gada api");
    delay(1000);
  }
}
```
