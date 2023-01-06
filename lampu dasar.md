<h1> contoh program hanya menggunakan lampu </h1>
<h4> lampu kedap-kedip </h4>

```
int pinLed = //input lampu led di pin yang mana
void setup()
{
  pinMode(pinLed, OUTPUT);
}

void loop()
{
  digitalWrite(pinLed, HIGH);
  delay(1000);
  digitalWrite(pinLed, LOW);
}
```
<h4> lampu lalu lintas </h4>

```
int ledMerah = //pin lampu merah
int ledJingga = //pin lampu jingga
int ledHijau = //pin lampu hijau

void setup()
{
  pinMode(ledMerah, OUTPUT);
  pinMode(ledJingga, OUTPUT);
  pinMode(ledHijau, OUTPUT);
}

void loop()
{
  digitalWrite(ledMerah, HIGH);
  digitalWrite(ledJingga, LOW);
  digitalWrite(ledHijau, LOW);
  delay(2000);
  
  digitalWrite(ledMerah, LOW);
  digitalWrite(ledJingga, HIGH);
  digitalWrite(ledHijau, LOW);
  delay(2000);
  
  digitalWrite(ledMerah, LOW);
  digitalWrite(ledJingga, LOW);
  digitalWrite(ledHijau, HIGH);
  delay(2000);
}
```
