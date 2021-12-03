int trigPin=12; // ECHO pini tanımlıyoruz. int echoPin-11;

void setup()

// TRIG pini dijital çıkış olarak tanımlıyoruz. pinMode(trigPin, OUTPUT); // ECHO pini dijital giriş olarak tanımlıyoruz. Serial.begin(9600);

pinMode (echoPin, INPUT); // Seri haberleşmeyi başlatıyoruz.

}

void loop()

{

// sure ve uzaklık değişkenlerini tanımlıyoruz. int sure, uzaklik;

digitalWrite(trigPin, HIGH);

delayMicroseconds (1000); digitalWrite(trigPin, LOW);

sure = pulseIn(echopin, HIGH);

uzaklik = (sure/58);

Serial.print("Uzaklik (cm)= "); Serial.println(uzaklik);

// Her 500 ms aralıklarla mesafe değerini okuyoruz.

}
