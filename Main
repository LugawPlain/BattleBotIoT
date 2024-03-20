char receivedChar = 0;

const int MR1 = 3; 
const int MR2 = 5; 
const int ML1 = 6;
const int ML2 = 9;

void setup() {
  Serial.begin(9600);
  pinMode(13,OUTPUT);
  digitalWrite(13,HIGH);
  pinMode(MR1, OUTPUT); 
  pinMode(MR2, OUTPUT);
  pinMode(ML1, OUTPUT);
  pinMode(ML2, OUTPUT);

  Serial.println("initialized");
}

void Forward(){
      digitalWrite(MR1,HIGH);
      digitalWrite(MR2,LOW);
      digitalWrite(ML1,LOW);
      digitalWrite(ML2,HIGH);
      Serial.println("Forward");
}
void Backward(){
      digitalWrite(MR1,LOW);
      digitalWrite(MR2,HIGH);
      digitalWrite(ML1,HIGH);
      digitalWrite(ML2,LOW);
      Serial.println("Backward");
}
void Left(){
      digitalWrite(MR1,HIGH);
      digitalWrite(MR2,LOW);
      digitalWrite(ML1,HIGH);
      digitalWrite(ML2,LOW);
      Serial.println("Left");
}
void Right(){
      digitalWrite(MR1,LOW);
      digitalWrite(MR2,HIGH);
      digitalWrite(ML1,LOW);
      digitalWrite(ML2,HIGH);
      Serial.println("Right");
}
void Stop(){
      digitalWrite(MR1,LOW); 
      digitalWrite(MR2,LOW);
      digitalWrite(ML1,LOW); 
      digitalWrite(ML2,LOW); 
      Serial.println("Stop");
}


void loop() {
  if (Serial.available()) {
    receivedChar = Serial.read();
    Serial.print("Received: ");
    Serial.println(receivedChar);

    if(receivedChar == 'u')
    {
      Forward();
       
    }
    if(receivedChar == 'd')
    {
 
      Backward(); 
    }         
     if(receivedChar == 'l')
    {

      Left();
    }        
    if(receivedChar == 'r')
    {

      Right(); 
    }
    if(receivedChar == '0')
    {
      Stop();
    }
  }
}
