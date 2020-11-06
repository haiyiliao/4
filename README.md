char Val;
void setup() 
{
  Serial.begin(9600);
}

void loop() 
{
  if (Serial.available() == 0)    
      return;
  Val = Serial.read();
  if (Val == 'A') 
    Serial.println("90-100");
  else if (Val == 'B')
    Serial.println("80-89");
  else if (Val == 'C')
    Serial.println("70-79");
  else if (Val == 'D')
    Serial.println("60-69");
  else if (Val == 'F')
    Serial.println("0-59");
}
