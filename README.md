# Vr
int led = 2;
int RV = A5;
int vRV = 0;
void setup() {
  pinMode(RV,INPUT);
  pinMode(led,OUTPUT);
  Serial.begin(9600);
}

void loop() {
  Serial.println(vRV);
  vRV = analogRead(RV);
  
  digitalWrite(led,HIGH);
  delay(vRV);
  digitalWrite(led,LOW);
  delay(vRV);
}
