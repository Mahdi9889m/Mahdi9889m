- 👋 Hi, I’m @Mahdi9889m
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Mahdi9889m/Mahdi9889m is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
const int buzzerPin = 12;
const int flamePin = 11;
int Flame = HIGH;
 
void setup() 
{
  pinMode(buzzerPin, OUTPUT);
  pinMode(flamePin, INPUT);
  Serial.begin(9600);
}
 
void loop() 
{
  Flame = digitalRead(flamePin);
  if (Flame== LOW)
  {
    Serial.println("Fire!!!");
    digitalWrite(buzzerPin, HIGH);
  }
  else
  {
    Serial.println("No worries");
    digitalWrite(buzzerPin, LOW);
  }
}
