// LED pinini tanımla
const int ledPin = 9;
// Potansiyometre pinini tanımla
const int potPin = A0;

void setup() {
  // LED pinini çıkış olarak ayarla
  pinMode(ledPin, OUTPUT);
}

void loop() {
  // Potansiyometre değerini oku (0-1023 arası)
  int potValue = analogRead(potPin);

  // LED'in parlaklığını potansiyometre değerine göre ayarla
  analogWrite(ledPin, potValue / 4);
  delay(10); // Küçük bir gecikme ekleyerek stabilizasyon sağla
}
